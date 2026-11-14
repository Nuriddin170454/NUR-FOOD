// NUR FOOD — sayt ma'lumotlari. Taom rasmlarini PRODUCTS ichidagi image manzilini almashtirib o'zgartiring.
const PRODUCTS = [
 {id:1,name:"NUR Burger",category:"burger",price:39000,desc:"Shirali kotlet, pishloq va maxsus sous.",badge:"TOP",image:"https://images.unsplash.com/photo-1568901346375-23c9450c58cd?auto=format&fit=crop&w=700&q=85"},
 {id:2,name:"Cheese Burger",category:"burger",price:42000,desc:"Ikki xil pishloq va yumshoq bulochka.",badge:"HIT",image:"https://images.unsplash.com/photo-1550547660-d9450f859349?auto=format&fit=crop&w=700&q=85"},
 {id:3,name:"Maxsus Lavash",category:"lavash",price:35000,desc:"Go‘sht, yangi sabzavot va qayla.",badge:"",image:"https://images.unsplash.com/photo-1529006557810-274b9b2fc783?auto=format&fit=crop&w=700&q=85"},
 {id:4,name:"Pishloqli Pizza",category:"pizza",price:55000,desc:"Mazali pishloq va maxsus xamir.",badge:"YANGI",image:"https://images.unsplash.com/photo-1513104890138-7c749659a591?auto=format&fit=crop&w=700&q=85"},
 {id:5,name:"Crispy Fries",category:"snack",price:18000,desc:"Qarsildoq va tillarang kartoshka.",badge:"",image:"https://images.unsplash.com/photo-1573080496219-bb080dd4f877?auto=format&fit=crop&w=700&q=85"},
 {id:6,name:"Chicken Burger",category:"burger",price:33000,desc:"Qarsildoq tovuq va fresh salat.",badge:"",image:"https://images.unsplash.com/photo-1606755962773-d324e0a13086?auto=format&fit=crop&w=700&q=85"},
 {id:7,name:"Cola",category:"drink",price:10000,desc:"Muzdek, tetiklashtiruvchi ichimlik.",badge:"",image:"https://images.unsplash.com/photo-1554866585-cd94860890b7?auto=format&fit=crop&w=700&q=85"},
 {id:8,name:"Nuggets",category:"snack",price:25000,desc:"Tashqi tomoni qarsildoq, ichi yumshoq.",badge:"",image:"https://images.unsplash.com/photo-1562967914-608f82629710?auto=format&fit=crop&w=700&q=85"}
];
const money = n => new Intl.NumberFormat('uz-UZ').format(n) + " so‘m";
let cart = [];
let activeFilter = "all";
const grid = document.getElementById("productGrid");
const cartDrawer = document.getElementById("cartDrawer");
const overlay = document.getElementById("overlay");
const toast = document.getElementById("toast");

function renderProducts(){
 const term = document.getElementById("menuSearch").value.trim().toLocaleLowerCase("uz");
 const list = PRODUCTS.filter(p => (activeFilter==="all" || p.category===activeFilter) && (p.name.toLocaleLowerCase("uz").includes(term) || p.desc.toLocaleLowerCase("uz").includes(term)));
 grid.innerHTML = list.length ? list.map((p,i)=>`
  <article class="product-card" data-aos="fade-up" style="--delay:${i*55}ms">
   <div class="product-image"><img src="${p.image}" alt="${p.name}" loading="lazy" onerror="this.src='https://images.unsplash.com/photo-1568901346375-23c9450c58cd?auto=format&fit=crop&w=700&q=80'">${p.badge?`<span class="product-badge">${p.badge}</span>`:""}</div>
   <div class="product-info"><h3>${p.name}</h3><p>${p.desc}</p><div class="product-bottom"><strong class="product-price">${money(p.price)}</strong><button class="add-btn" data-add="${p.id}" aria-label="${p.name} savatga qo‘shish">+</button></div></div>
  </article>`).join("") : `<p class="no-results">Bu nomda taom topilmadi. Boshqa nom bilan qidiring.</p>`;
 observeAOS();
}
function renderCart(){
 const count=cart.reduce((s,x)=>s+x.qty,0), total=cart.reduce((s,x)=>s+x.price*x.qty,0);
 document.getElementById("cartCount").textContent=count;
 document.getElementById("cartTotal").textContent=money(total);
 document.getElementById("cartItems").innerHTML=cart.length?cart.map(x=>`
  <div class="cart-row"><img src="${x.image}" alt="${x.name}"><div><b>${x.name}</b><small>${money(x.price)}</small><div class="qty"><button data-qty="${x.id}" data-step="-1">−</button><span>${x.qty}</span><button data-qty="${x.id}" data-step="1">+</button></div></div><strong class="cart-row-price">${money(x.price*x.qty)}</strong></div>`).join(""):`<div class="empty-cart"><span style="font-size:38px">🛍️</span><b>Savatingiz hozircha bo‘sh</b><small>Menyudan mazali taom tanlang.</small></div>`;
}
function showToast(){toast.classList.add("show");clearTimeout(showToast.timer);showToast.timer=setTimeout(()=>toast.classList.remove("show"),1800)}
function openCart(){cartDrawer.classList.add("open");overlay.classList.add("show");document.body.style.overflow="hidden"}
function closeCart(){cartDrawer.classList.remove("open");overlay.classList.remove("show");document.body.style.overflow=""}
grid.addEventListener("click",e=>{const btn=e.target.closest("[data-add]");if(!btn)return;const p=PRODUCTS.find(x=>x.id===Number(btn.dataset.add));const item=cart.find(x=>x.id===p.id);item?item.qty++:cart.push({...p,qty:1});renderCart();showToast()});
document.getElementById("cartItems").addEventListener("click",e=>{const b=e.target.closest("[data-qty]");if(!b)return;const item=cart.find(x=>x.id===Number(b.dataset.qty));item.qty+=Number(b.dataset.step);if(item.qty<=0)cart=cart.filter(x=>x.id!==item.id);renderCart()});
document.getElementById("filters").addEventListener("click",e=>{const b=e.target.closest("[data-filter]");if(!b)return;activeFilter=b.dataset.filter;document.querySelectorAll(".filter").forEach(x=>x.classList.toggle("active",x===b));renderProducts()});
document.getElementById("menuSearch").addEventListener("input",renderProducts);
document.getElementById("cartOpen").addEventListener("click",openCart);
document.getElementById("cartClose").addEventListener("click",closeCart);
overlay.addEventListener("click",closeCart);
document.addEventListener("keydown",e=>{if(e.key==="Escape")closeCart()});
document.getElementById("checkoutBtn").addEventListener("click",()=>{
 if(!cart.length){showToast();return}
 // Quyidagi telefon raqamini o'zingizning WhatsApp raqamingizga almashtiring (998 bilan, + belgisiz).
 const phone="998901234567";
 const lines=cart.map(x=>`${x.name} x${x.qty} — ${money(x.price*x.qty)}`).join("\n");
 const total=cart.reduce((s,x)=>s+x.price*x.qty,0);
 const message=`Assalomu alaykum! NUR FOOD'dan buyurtma bermoqchiman:\n${lines}\n\nJami: ${money(total)}\nIsmim: `;
 window.open(`https://wa.me/${phone}?text=${encodeURIComponent(message)}`,"_blank","noopener");
});
document.getElementById("menuToggle").addEventListener("click",()=>{const nav=document.getElementById("nav"),btn=document.getElementById("menuToggle");nav.classList.toggle("open");btn.setAttribute("aria-expanded",nav.classList.contains("open"))});
document.querySelectorAll(".nav-link").forEach(a=>a.addEventListener("click",()=>{document.getElementById("nav").classList.remove("open");document.getElementById("menuToggle").setAttribute("aria-expanded","false")}));

// Owl Carousel uslubidagi yengil, vanilla JavaScript carousel.
let reviewIndex=0;
function moveReviews(dir){const track=document.getElementById("reviewTrack"),cards=[...track.children];if(!cards.length)return;const visible=innerWidth<=700?1:3;const max=Math.max(0,cards.length-visible);reviewIndex=Math.max(0,Math.min(max,reviewIndex+dir));track.style.transform=`translateX(-${reviewIndex*(cards[0].getBoundingClientRect().width+18)}px)`;}
document.getElementById("reviewPrev").addEventListener("click",()=>moveReviews(-1));
document.getElementById("reviewNext").addEventListener("click",()=>moveReviews(1));
window.addEventListener("resize",()=>{reviewIndex=0;const t=document.getElementById("reviewTrack");t.style.transform="translateX(0)"});

// AOS uslubidagi scroll reveal animatsiyasi — tashqi kutubxonasiz.
let aosObserver;
function observeAOS(){
 if(!("IntersectionObserver" in window)){document.querySelectorAll("[data-aos]").forEach(x=>x.classList.add("aos-visible"));return}
 if(aosObserver)aosObserver.disconnect();
 aosObserver=new IntersectionObserver(entries=>entries.forEach(entry=>{if(entry.isIntersecting){entry.target.classList.add("aos-visible");aosObserver.unobserve(entry.target)}}),{threshold:.12});
 document.querySelectorAll("[data-aos]:not(.aos-visible)").forEach(el=>{el.style.setProperty("--delay",el.style.getPropertyValue("--delay")||"0ms");aosObserver.observe(el)});
}
document.getElementById("year").textContent=new Date().getFullYear();
renderProducts();renderCart();observeAOS();
