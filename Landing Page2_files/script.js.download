let toggleBtn = document.getElementById("toggle-btn");
let body = document.body;
let darkMode = localStorage.getItem("dark-mode");

// استرجاع اسم المستخدم من localStorage
const updateUsernameDisplay = () => {
    const username = localStorage.getItem("username");
    if (username) {
        document
            .querySelectorAll(".header .flex .profile .name")
            .forEach((element) => {
                element.textContent = username; // تحديث جميع العناصر التي تحتوي على الاسم
            });
    }
};

// تحديث اسم المستخدم عند تحميل الصفحة
updateUsernameDisplay();

const enableDarkMode = () => {
    toggleBtn.classList.replace("fa-sun", "fa-moon");
    body.classList.add("dark");
    localStorage.setItem("dark-mode", "enabled");
};

const disableDarkMode = () => {
    toggleBtn.classList.replace("fa-moon", "fa-sun");
    body.classList.remove("dark");
    localStorage.setItem("dark-mode", "disabled");
};

if (darkMode === "enabled") {
    enableDarkMode();
}

toggleBtn.onclick = (e) => {
    darkMode = localStorage.getItem("dark-mode");
    if (darkMode === "disabled") {
        enableDarkMode();
    } else {
        disableDarkMode();
    }
};

let profile = document.querySelector(".header .flex .profile");

document.querySelector("#user-btn").onclick = () => {
    profile.classList.toggle("active");
    search.classList.remove("active");
};

let search = document.querySelector(".header .flex .search-form");

document.querySelector("#search-btn").onclick = () => {
    search.classList.toggle("active");
    profile.classList.remove("active");
};

let sideBar = document.querySelector(".side-bar");

document.querySelector("#menu-btn").onclick = () => {
    sideBar.classList.toggle("active");
    body.classList.toggle("active");
};

document.querySelector("#close-btn").onclick = () => {
    sideBar.classList.remove("active");
    body.classList.remove("active");
};

window.onscroll = () => {
    profile.classList.remove("active");
    search.classList.remove("active");

    if (window.innerWidth < 1200) {
        sideBar.classList.remove("active");
        body.classList.remove("active");
    }
};
document.getElementById("current-year").textContent = new Date().getFullYear();

// Login functionality
document.getElementById("loginForm").addEventListener("submit", function(e) {
    e.preventDefault(); // منع إعادة تحميل الصفحة

    const email = document.getElementById("loginEmail").value;
    const password = document.getElementById("loginPassword").value;

    // استرجاع البيانات من localStorage
    const storedEmail = localStorage.getItem("userEmail");
    const storedPassword = localStorage.getItem("userPassword");

    // مقارنة البيانات
    if (email === storedEmail && password === storedPassword) {
        alert("Login successful!");
        // يمكنك توجيه المستخدم إلى صفحة أخرى بعد تسجيل الدخول الناجح
        window.location.href = "home.html"; // على سبيل المثال
    } else {
        alert("Invalid email or password!");
    }
});
// استرجاع بيانات المستخدم من localStorage

const updateProfileDisplay = () => {
    const username = localStorage.getItem("username");
    const userRole = localStorage.getItem("userRole");
    const userImage = localStorage.getItem("userImage");

    if (username) {
        document.getElementById("userName").textContent = username;
    }
    if (userRole) {
        document.getElementById("userRole").textContent = userRole;
    }
    if (userImage) {
        document.getElementById("userImage").src = userImage;
    }
};

// تحديث واجهة المستخدم عند تحميل الصفحة
document.addEventListener("DOMContentLoaded", updateProfileDisplay);