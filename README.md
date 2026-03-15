<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>SreeDigitals — Creative Digital Downloads</title>
<link href="https://fonts.googleapis.com/css2?family=Playfair+Display:ital,wght@0,400;0,700;0,900;1,400;1,700&family=Outfit:wght@300;400;500;600&family=Caveat:wght@400;600&display=swap" rel="stylesheet">
<style>
:root {
  --cream: #FAF7F2;
  --warm-white: #FFFDF9;
  --ink: #1C1712;
  --terra: #C4622D;
  --terra-light: #E8845A;
  --terra-pale: #F5E6DC;
  --sage: #7A9E7E;
  --sage-light: #D4E8D6;
  --gold: #D4A853;
  --gold-light: #F5E8C8;
  --gray: #7A7068;
  --gray-light: #EDE8E2;
  --border: #E2DAD0;
  --shadow: rgba(28,23,18,0.08);
  --radius: 14px;
  --nav-h: 70px;
}
*{margin:0;padding:0;box-sizing:border-box;}
html{scroll-behavior:smooth;}
body{font-family:'Outfit',sans-serif;background:var(--cream);color:var(--ink);min-height:100vh;overflow-x:hidden;}

/* ─── SCROLLBAR ─── */
::-webkit-scrollbar{width:6px;}
::-webkit-scrollbar-track{background:var(--cream);}
::-webkit-scrollbar-thumb{background:var(--terra-light);border-radius:3px;}

/* ─── NAVBAR ─── */
nav{position:fixed;top:0;left:0;right:0;z-index:500;height:var(--nav-h);background:rgba(250,247,242,0.92);backdrop-filter:blur(12px);border-bottom:1px solid var(--border);display:flex;align-items:center;justify-content:space-between;padding:0 40px;transition:box-shadow .3s;}
nav.scrolled{box-shadow:0 4px 24px var(--shadow);}
.nav-logo{font-family:'Playfair Display',serif;font-size:22px;font-weight:900;color:var(--ink);cursor:pointer;letter-spacing:-0.5px;}
.nav-logo span{color:var(--terra);}
.nav-links{display:flex;gap:32px;align-items:center;}
.nav-links a{font-size:14px;font-weight:500;color:var(--gray);text-decoration:none;cursor:pointer;transition:color .2s;position:relative;}
.nav-links a:hover,.nav-links a.active{color:var(--ink);}
.nav-links a.active::after{content:'';position:absolute;bottom:-4px;left:0;right:0;height:2px;background:var(--terra);border-radius:2px;}
.nav-actions{display:flex;align-items:center;gap:16px;}
.btn-ghost{background:none;border:1.5px solid var(--border);padding:8px 18px;border-radius:100px;font-size:13px;font-weight:500;cursor:pointer;font-family:'Outfit',sans-serif;color:var(--ink);transition:all .2s;}
.btn-ghost:hover{border-color:var(--terra);color:var(--terra);}
.btn-primary{background:var(--terra);border:none;padding:9px 20px;border-radius:100px;font-size:13px;font-weight:600;cursor:pointer;font-family:'Outfit',sans-serif;color:white;transition:all .2s;}
.btn-primary:hover{background:var(--terra-light);transform:translateY(-1px);box-shadow:0 4px 12px rgba(196,98,45,0.3);}
.cart-btn{position:relative;background:var(--terra-pale);border:none;width:40px;height:40px;border-radius:50%;cursor:pointer;font-size:16px;transition:all .2s;display:flex;align-items:center;justify-content:center;}
.cart-btn:hover{background:var(--terra);transform:scale(1.05);}
.cart-btn:hover .cart-icon{filter:invert(1);}
.cart-badge{position:absolute;top:-4px;right:-4px;background:var(--terra);color:white;font-size:9px;font-weight:700;width:18px;height:18px;border-radius:50%;display:flex;align-items:center;justify-content:center;font-family:'Outfit',sans-serif;border:2px solid var(--cream);display:none;}
.cart-badge.show{display:flex;}
.hamburger{display:none;background:none;border:none;cursor:pointer;font-size:22px;color:var(--ink);}

/* ─── PAGES ─── */
.page{display:none;min-height:calc(100vh - var(--nav-h));padding-top:var(--nav-h);}
.page.active{display:block;}

/* ─── HOME PAGE ─── */
.hero{min-height:92vh;display:grid;grid-template-columns:1fr 1fr;align-items:center;padding:60px 40px 40px;gap:40px;position:relative;overflow:hidden;}
.hero::before{content:'';position:absolute;top:-100px;right:-100px;width:600px;height:600px;background:radial-gradient(circle,rgba(212,168,83,0.12) 0%,transparent 70%);pointer-events:none;}
.hero-content{max-width:560px;}
.hero-eyebrow{display:inline-flex;align-items:center;gap:8px;background:var(--gold-light);padding:6px 16px;border-radius:100px;font-size:12px;font-weight:600;color:var(--gold);text-transform:uppercase;letter-spacing:1px;margin-bottom:24px;}
.hero h1{font-family:'Playfair Display',serif;font-size:64px;line-height:1.05;font-weight:900;margin-bottom:20px;letter-spacing:-1px;}
.hero h1 em{font-style:italic;color:var(--terra);}
.hero-sub{font-size:17px;color:var(--gray);line-height:1.7;margin-bottom:36px;max-width:440px;}
.hero-btns{display:flex;gap:14px;flex-wrap:wrap;margin-bottom:48px;}
.btn-lg{padding:14px 32px;border-radius:100px;font-size:15px;font-weight:600;cursor:pointer;font-family:'Outfit',sans-serif;transition:all .25s;border:none;}
.btn-lg-primary{background:var(--terra);color:white;}
.btn-lg-primary:hover{background:var(--terra-light);transform:translateY(-2px);box-shadow:0 8px 24px rgba(196,98,45,0.35);}
.btn-lg-outline{background:transparent;color:var(--ink);border:2px solid var(--border);}
.btn-lg-outline:hover{border-color:var(--terra);color:var(--terra);}
.hero-stats{display:flex;gap:32px;}
.stat{text-align:center;}
.stat-num{font-family:'Playfair Display',serif;font-size:28px;font-weight:700;color:var(--ink);}
.stat-label{font-size:12px;color:var(--gray);font-weight:500;}
.hero-visual{position:relative;display:flex;justify-content:center;align-items:center;}
.hero-grid{display:grid;grid-template-columns:1fr 1fr;gap:16px;transform:rotate(3deg);}
.hero-card{border-radius:16px;overflow:hidden;box-shadow:0 8px 32px var(--shadow);transition:transform .3s;}
.hero-card:hover{transform:scale(1.03) rotate(-2deg);}
.hero-card-img{width:100%;aspect-ratio:3/4;object-fit:cover;display:block;}
.hero-card-img.coloring{background:linear-gradient(135deg,#FFF5E6 0%,#FFE4CC 50%,#FFD4AA 100%);display:flex;align-items:center;justify-content:center;font-size:60px;}
.hero-card-img.planner{background:linear-gradient(135deg,#E8F4E8 0%,#D4EBD4 50%,#BDDCBD 100%);display:flex;align-items:center;justify-content:center;font-size:60px;}
.hero-card-img.poster{background:linear-gradient(135deg,#E8E4F4 0%,#D4CCEB 50%,#C4B8E0 100%);display:flex;align-items:center;justify-content:center;font-size:60px;}
.hero-card-img.instagram{background:linear-gradient(135deg,#FFF0E8 0%,#FFE0D0 50%,#FFCDB8 100%);display:flex;align-items:center;justify-content:center;font-size:60px;}
.hero-card-offset{margin-top:24px;}
.hero-float-tag{position:absolute;background:white;border-radius:12px;padding:10px 16px;box-shadow:0 4px 20px var(--shadow);font-size:12px;font-weight:600;}
.float-tag-1{top:20px;left:-20px;color:var(--sage);}
.float-tag-2{bottom:40px;right:-20px;color:var(--terra);}

/* categories strip */
.categories-strip{padding:48px 40px;background:var(--warm-white);border-top:1px solid var(--border);border-bottom:1px solid var(--border);}
.section-label{font-size:11px;text-transform:uppercase;letter-spacing:2px;color:var(--terra);font-weight:600;margin-bottom:16px;}
.cat-scroll{display:flex;gap:16px;overflow-x:auto;padding-bottom:4px;scrollbar-width:none;}
.cat-scroll::-webkit-scrollbar{display:none;}
.cat-chip{flex-shrink:0;display:flex;align-items:center;gap:10px;padding:14px 22px;background:var(--cream);border:1.5px solid var(--border);border-radius:100px;cursor:pointer;transition:all .2s;font-size:14px;font-weight:500;white-space:nowrap;}
.cat-chip:hover,.cat-chip.active{background:var(--terra);border-color:var(--terra);color:white;}
.cat-chip .cat-icon{font-size:18px;}

/* featured */
.featured-section{padding:72px 40px;}
.section-header{display:flex;justify-content:space-between;align-items:flex-end;margin-bottom:40px;}
.section-title{font-family:'Playfair Display',serif;font-size:38px;font-weight:700;line-height:1.2;}
.section-title span{font-style:italic;color:var(--terra);}
.see-all{font-size:13px;font-weight:600;color:var(--terra);cursor:pointer;text-decoration:none;display:flex;align-items:center;gap:4px;}
.see-all:hover{text-decoration:underline;}
.products-grid{display:grid;grid-template-columns:repeat(auto-fill,minmax(240px,1fr));gap:24px;}

/* ─── PRODUCT CARD ─── */
.product-card{background:white;border-radius:var(--radius);overflow:hidden;border:1px solid var(--border);transition:all .25s;cursor:pointer;position:relative;}
.product-card:hover{transform:translateY(-4px);box-shadow:0 12px 40px var(--shadow);}
.product-card-img{width:100%;aspect-ratio:4/5;display:flex;align-items:center;justify-content:center;font-size:56px;position:relative;overflow:hidden;}
.product-card-badge{position:absolute;top:12px;left:12px;background:var(--terra);color:white;font-size:10px;font-weight:700;padding:4px 10px;border-radius:100px;text-transform:uppercase;letter-spacing:0.5px;}
.product-card-badge.new{background:var(--sage);}
.product-card-badge.sale{background:var(--gold);}
.product-card-wishlist{position:absolute;top:12px;right:12px;width:32px;height:32px;background:white;border-radius:50%;display:flex;align-items:center;justify-content:center;font-size:14px;cursor:pointer;box-shadow:0 2px 8px var(--shadow);transition:all .2s;border:none;}
.product-card-wishlist:hover{transform:scale(1.1);}
.product-card-wishlist.active{background:var(--terra);color:white;}
.product-card-body{padding:16px;}
.product-card-cat{font-size:11px;text-transform:uppercase;letter-spacing:1px;color:var(--terra);font-weight:600;margin-bottom:4px;}
.product-card-name{font-family:'Playfair Display',serif;font-size:16px;font-weight:700;margin-bottom:6px;line-height:1.3;}
.product-card-meta{display:flex;align-items:center;justify-content:space-between;margin-top:12px;}
.product-card-price{font-size:18px;font-weight:700;color:var(--ink);}
.product-card-price .original{font-size:13px;color:var(--gray);text-decoration:line-through;margin-left:6px;font-weight:400;}
.rating{display:flex;align-items:center;gap:4px;font-size:12px;color:var(--gray);}
.rating .stars{color:var(--gold);}
.product-card-add{width:100%;background:var(--terra-pale);border:none;padding:10px;border-radius:0 0 12px 12px;font-size:13px;font-weight:600;color:var(--terra);cursor:pointer;transition:all .2s;font-family:'Outfit',sans-serif;}
.product-card-add:hover{background:var(--terra);color:white;}

/* ─── MARQUEE ─── */
.marquee-section{background:var(--terra);padding:16px 0;overflow:hidden;}
.marquee-track{display:flex;gap:0;animation:marquee 20s linear infinite;white-space:nowrap;}
.marquee-item{padding:0 32px;font-size:13px;font-weight:600;color:rgba(255,255,255,0.9);display:inline-flex;align-items:center;gap:12px;}
.marquee-item span{color:rgba(255,255,255,0.4);font-size:18px;}
@keyframes marquee{0%{transform:translateX(0);}100%{transform:translateX(-50%);}}

/* ─── WHY US ─── */
.why-section{padding:72px 40px;background:var(--warm-white);}
.why-grid{display:grid;grid-template-columns:repeat(auto-fill,minmax(220px,1fr));gap:24px;margin-top:48px;}
.why-card{padding:28px 24px;border-radius:var(--radius);border:1px solid var(--border);background:var(--cream);transition:all .2s;}
.why-card:hover{border-color:var(--terra);transform:translateY(-2px);}
.why-icon{font-size:36px;margin-bottom:16px;display:block;}
.why-title{font-family:'Playfair Display',serif;font-size:18px;font-weight:700;margin-bottom:8px;}
.why-desc{font-size:14px;color:var(--gray);line-height:1.6;}

/* ─── SHOP PAGE ─── */
.shop-layout{display:grid;grid-template-columns:240px 1fr;gap:40px;padding:40px;}
.shop-sidebar{position:sticky;top:calc(var(--nav-h)+20px);align-self:start;}
.filter-section{margin-bottom:28px;}
.filter-title{font-size:13px;font-weight:700;text-transform:uppercase;letter-spacing:1px;margin-bottom:12px;color:var(--ink);}
.filter-option{display:flex;align-items:center;gap:8px;padding:6px 0;cursor:pointer;font-size:14px;color:var(--gray);transition:color .2s;}
.filter-option:hover{color:var(--ink);}
.filter-option input[type=checkbox]{accent-color:var(--terra);width:15px;height:15px;cursor:pointer;}
.filter-option input[type=radio]{accent-color:var(--terra);width:15px;height:15px;cursor:pointer;}
.price-range{display:flex;flex-direction:column;gap:8px;}
.price-inputs{display:flex;gap:8px;}
.price-inputs input{width:100%;padding:8px 10px;border:1.5px solid var(--border);border-radius:8px;font-size:13px;font-family:'Outfit',sans-serif;background:var(--cream);}
.shop-main-header{display:flex;justify-content:space-between;align-items:center;margin-bottom:28px;}
.shop-count{font-size:14px;color:var(--gray);}
.sort-select{padding:8px 14px;border:1.5px solid var(--border);border-radius:8px;font-size:13px;font-family:'Outfit',sans-serif;background:var(--cream);cursor:pointer;color:var(--ink);}
.shop-page-header{padding:40px 40px 0;background:linear-gradient(180deg,var(--terra-pale) 0%,var(--cream) 100%);}
.shop-page-title{font-family:'Playfair Display',serif;font-size:48px;font-weight:900;margin-bottom:8px;}
.shop-page-title em{font-style:italic;color:var(--terra);}

/* ─── PRODUCT DETAIL PAGE ─── */
.detail-layout{display:grid;grid-template-columns:1fr 1fr;gap:64px;padding:48px 64px;max-width:1200px;margin:0 auto;}
.detail-gallery{position:sticky;top:calc(var(--nav-h)+20px);align-self:start;}
.detail-main-img{width:100%;aspect-ratio:4/5;border-radius:20px;display:flex;align-items:center;justify-content:center;font-size:100px;margin-bottom:16px;overflow:hidden;}
.detail-thumbs{display:flex;gap:10px;}
.detail-thumb{width:64px;height:64px;border-radius:10px;display:flex;align-items:center;justify-content:center;font-size:24px;cursor:pointer;border:2px solid transparent;transition:all .2s;overflow:hidden;}
.detail-thumb.active,.detail-thumb:hover{border-color:var(--terra);}
.detail-content{}
.detail-cat{font-size:12px;text-transform:uppercase;letter-spacing:1.5px;color:var(--terra);font-weight:600;margin-bottom:8px;}
.detail-name{font-family:'Playfair Display',serif;font-size:36px;font-weight:800;line-height:1.2;margin-bottom:12px;}
.detail-rating{display:flex;align-items:center;gap:10px;margin-bottom:20px;}
.detail-rating .stars{font-size:16px;color:var(--gold);}
.detail-rating .count{font-size:14px;color:var(--gray);}
.detail-price{font-size:36px;font-weight:800;color:var(--ink);margin-bottom:8px;}
.detail-price .original{font-size:20px;color:var(--gray);text-decoration:line-through;margin-left:10px;font-weight:400;}
.detail-price .savings{display:inline-block;background:var(--gold-light);color:var(--gold);font-size:12px;font-weight:700;padding:3px 10px;border-radius:100px;margin-left:10px;}
.detail-desc{font-size:15px;color:var(--gray);line-height:1.8;margin-bottom:28px;padding-bottom:28px;border-bottom:1px solid var(--border);}
.detail-options{margin-bottom:24px;}
.detail-options-label{font-size:13px;font-weight:600;margin-bottom:10px;text-transform:uppercase;letter-spacing:0.5px;}
.size-chips{display:flex;flex-wrap:wrap;gap:8px;}
.size-chip{padding:8px 18px;border:2px solid var(--border);border-radius:8px;font-size:13px;font-weight:500;cursor:pointer;transition:all .2s;background:white;}
.size-chip.active,.size-chip:hover{border-color:var(--terra);background:var(--terra-pale);color:var(--terra);}
.detail-actions{display:flex;gap:12px;margin-bottom:28px;}
.btn-add-cart{flex:1;background:var(--terra);color:white;border:none;padding:15px 28px;border-radius:100px;font-size:15px;font-weight:700;cursor:pointer;font-family:'Outfit',sans-serif;transition:all .25s;}
.btn-add-cart:hover{background:var(--terra-light);transform:translateY(-2px);box-shadow:0 8px 24px rgba(196,98,45,0.3);}
.btn-wishlist-d{width:52px;height:52px;border:2px solid var(--border);border-radius:50%;background:white;cursor:pointer;font-size:18px;display:flex;align-items:center;justify-content:center;transition:all .2s;flex-shrink:0;}
.btn-wishlist-d:hover,.btn-wishlist-d.active{border-color:var(--terra);background:var(--terra-pale);}
.detail-features{display:flex;flex-direction:column;gap:10px;margin-bottom:24px;}
.detail-feature{display:flex;align-items:center;gap:10px;font-size:14px;color:var(--gray);}
.detail-feature::before{content:'✓';width:20px;height:20px;background:var(--sage-light);border-radius:50%;display:flex;align-items:center;justify-content:center;font-size:11px;color:var(--sage);font-weight:700;flex-shrink:0;}
.detail-reviews{padding:48px 64px;background:var(--warm-white);border-top:1px solid var(--border);}
.review-card{background:white;border:1px solid var(--border);border-radius:var(--radius);padding:20px 24px;margin-bottom:16px;}
.review-header{display:flex;justify-content:space-between;margin-bottom:8px;}
.reviewer-name{font-weight:600;font-size:14px;}
.review-date{font-size:12px;color:var(--gray);}
.review-stars{color:var(--gold);font-size:14px;margin-bottom:8px;}
.review-text{font-size:14px;color:var(--gray);line-height:1.6;}

/* ─── CART SIDEBAR ─── */
.cart-overlay{position:fixed;inset:0;background:rgba(28,23,18,0.5);z-index:800;opacity:0;pointer-events:none;transition:opacity .3s;}
.cart-overlay.open{opacity:1;pointer-events:all;}
.cart-drawer{position:fixed;top:0;right:0;bottom:0;width:420px;background:var(--warm-white);z-index:900;transform:translateX(100%);transition:transform .3s ease;display:flex;flex-direction:column;box-shadow:-8px 0 48px var(--shadow);}
.cart-drawer.open{transform:translateX(0);}
.cart-header{padding:24px 28px;border-bottom:1px solid var(--border);display:flex;justify-content:space-between;align-items:center;}
.cart-title{font-family:'Playfair Display',serif;font-size:24px;font-weight:700;}
.cart-close{background:none;border:none;font-size:22px;cursor:pointer;color:var(--gray);width:36px;height:36px;border-radius:50%;display:flex;align-items:center;justify-content:center;transition:all .2s;}
.cart-close:hover{background:var(--gray-light);}
.cart-items{flex:1;overflow-y:auto;padding:20px 28px;}
.cart-empty{text-align:center;padding:60px 20px;}
.cart-empty-icon{font-size:48px;margin-bottom:16px;display:block;}
.cart-empty-title{font-family:'Playfair Display',serif;font-size:20px;font-weight:700;margin-bottom:8px;}
.cart-empty-sub{font-size:14px;color:var(--gray);margin-bottom:24px;}
.cart-item{display:flex;gap:14px;padding:14px 0;border-bottom:1px solid var(--border);}
.cart-item-img{width:64px;height:80px;border-radius:10px;display:flex;align-items:center;justify-content:center;font-size:28px;flex-shrink:0;overflow:hidden;}
.cart-item-info{flex:1;min-width:0;}
.cart-item-name{font-weight:600;font-size:14px;margin-bottom:4px;line-height:1.3;}
.cart-item-size{font-size:12px;color:var(--gray);margin-bottom:8px;}
.cart-item-row{display:flex;align-items:center;justify-content:space-between;}
.cart-item-price{font-weight:700;font-size:15px;color:var(--terra);}
.qty-control{display:flex;align-items:center;gap:8px;}
.qty-btn{width:26px;height:26px;border-radius:50%;border:1.5px solid var(--border);background:white;cursor:pointer;font-size:14px;display:flex;align-items:center;justify-content:center;transition:all .2s;}
.qty-btn:hover{border-color:var(--terra);color:var(--terra);}
.qty-num{font-size:14px;font-weight:600;min-width:20px;text-align:center;}
.cart-remove{background:none;border:none;cursor:pointer;color:var(--gray);font-size:16px;padding:4px;transition:color .2s;}
.cart-remove:hover{color:var(--terra);}
.cart-footer{padding:20px 28px;border-top:1px solid var(--border);}
.cart-subtotal{display:flex;justify-content:space-between;font-size:15px;margin-bottom:8px;}
.cart-total{display:flex;justify-content:space-between;font-size:18px;font-weight:700;margin-bottom:20px;padding-top:12px;border-top:1px solid var(--border);}
.promo-row{display:flex;gap:8px;margin-bottom:16px;}
.promo-input{flex:1;padding:10px 14px;border:1.5px solid var(--border);border-radius:8px;font-size:13px;font-family:'Outfit',sans-serif;background:var(--cream);}
.promo-input:focus{outline:none;border-color:var(--terra);}
.promo-apply{background:var(--ink);color:white;border:none;padding:10px 16px;border-radius:8px;font-size:13px;font-weight:600;cursor:pointer;font-family:'Outfit',sans-serif;white-space:nowrap;}
.btn-checkout{width:100%;background:var(--terra);color:white;border:none;padding:15px;border-radius:100px;font-size:15px;font-weight:700;cursor:pointer;font-family:'Outfit',sans-serif;transition:all .25s;}
.btn-checkout:hover{background:var(--terra-light);transform:translateY(-1px);box-shadow:0 6px 20px rgba(196,98,45,0.35);}

/* ─── AUTH MODAL ─── */
.modal-overlay{position:fixed;inset:0;background:rgba(28,23,18,0.6);z-index:1000;display:none;align-items:center;justify-content:center;padding:20px;}
.modal-overlay.open{display:flex;}
.modal{background:white;border-radius:24px;width:100%;max-width:440px;overflow:hidden;box-shadow:0 24px 80px rgba(0,0,0,0.2);animation:modalIn .3s ease;}
@keyframes modalIn{from{opacity:0;transform:scale(0.95)translateY(20px);}to{opacity:1;transform:scale(1)translateY(0);}}
.modal-header{padding:32px 36px 24px;text-align:center;background:linear-gradient(135deg,var(--terra-pale),var(--cream));}
.modal-logo{font-family:'Playfair Display',serif;font-size:24px;font-weight:900;margin-bottom:8px;}
.modal-logo span{color:var(--terra);}
.modal-title{font-family:'Playfair Display',serif;font-size:26px;font-weight:700;margin-bottom:4px;}
.modal-sub{font-size:14px;color:var(--gray);}
.modal-body{padding:24px 36px 32px;}
.modal-tabs{display:flex;gap:0;margin-bottom:28px;background:var(--gray-light);border-radius:10px;padding:4px;}
.modal-tab{flex:1;padding:9px;border:none;background:none;border-radius:8px;font-size:14px;font-weight:600;cursor:pointer;font-family:'Outfit',sans-serif;color:var(--gray);transition:all .2s;}
.modal-tab.active{background:white;color:var(--ink);box-shadow:0 2px 8px var(--shadow);}
.form-group{margin-bottom:16px;}
.form-label{display:block;font-size:13px;font-weight:600;margin-bottom:6px;color:var(--ink);}
.form-input{width:100%;padding:12px 16px;border:1.5px solid var(--border);border-radius:10px;font-size:14px;font-family:'Outfit',sans-serif;background:var(--cream);transition:border-color .2s;outline:none;color:var(--ink);}
.form-input:focus{border-color:var(--terra);}
.form-row{display:grid;grid-template-columns:1fr 1fr;gap:12px;}
.btn-submit{width:100%;background:var(--terra);color:white;border:none;padding:14px;border-radius:100px;font-size:15px;font-weight:700;cursor:pointer;font-family:'Outfit',sans-serif;transition:all .25s;margin-top:8px;}
.btn-submit:hover{background:var(--terra-light);transform:translateY(-1px);}
.form-divider{text-align:center;font-size:13px;color:var(--gray);margin:16px 0;position:relative;}
.form-divider::before,.form-divider::after{content:'';position:absolute;top:50%;width:calc(50% - 20px);height:1px;background:var(--border);}
.form-divider::before{left:0;}
.form-divider::after{right:0;}
.oauth-btn{width:100%;padding:12px;border:1.5px solid var(--border);border-radius:10px;background:white;font-size:14px;font-family:'Outfit',sans-serif;cursor:pointer;transition:all .2s;display:flex;align-items:center;justify-content:center;gap:10px;font-weight:500;}
.oauth-btn:hover{border-color:var(--gray);background:var(--cream);}
.modal-close-x{position:absolute;top:16px;right:16px;background:none;border:none;font-size:20px;cursor:pointer;color:var(--gray);width:32px;height:32px;border-radius:50%;display:flex;align-items:center;justify-content:center;transition:background .2s;}
.modal-close-x:hover{background:var(--gray-light);}
.modal-header{position:relative;}
.auth-success{text-align:center;padding:20px 0;}
.auth-success-icon{font-size:48px;margin-bottom:12px;display:block;}

/* ─── CHECKOUT PAGE ─── */
.checkout-layout{display:grid;grid-template-columns:1fr 400px;gap:48px;padding:40px 64px;max-width:1200px;margin:0 auto;}
.checkout-form-section{background:white;border-radius:20px;padding:32px;border:1px solid var(--border);margin-bottom:24px;}
.checkout-section-title{font-family:'Playfair Display',serif;font-size:20px;font-weight:700;margin-bottom:20px;display:flex;align-items:center;gap:10px;}
.checkout-section-title .step-num{width:28px;height:28px;background:var(--terra);color:white;border-radius:50%;display:flex;align-items:center;justify-content:center;font-size:13px;font-weight:700;font-family:'Outfit',sans-serif;}
.payment-method{border:2px solid var(--border);border-radius:12px;padding:14px 18px;cursor:pointer;margin-bottom:10px;transition:all .2s;display:flex;align-items:center;gap:14px;}
.payment-method.selected,.payment-method:hover{border-color:var(--terra);background:var(--terra-pale);}
.payment-method input[type=radio]{accent-color:var(--terra);}
.payment-method-info{flex:1;}
.payment-method-name{font-weight:600;font-size:14px;}
.payment-method-sub{font-size:12px;color:var(--gray);}
.payment-icons{margin-left:auto;display:flex;gap:6px;}
.payment-icon{background:var(--gray-light);border-radius:6px;padding:4px 8px;font-size:11px;font-weight:600;color:var(--gray);}
.checkout-order-summary{background:white;border-radius:20px;padding:28px;border:1px solid var(--border);position:sticky;top:calc(var(--nav-h)+20px);}
.checkout-order-title{font-family:'Playfair Display',serif;font-size:20px;font-weight:700;margin-bottom:20px;}
.checkout-item{display:flex;gap:12px;margin-bottom:14px;padding-bottom:14px;border-bottom:1px solid var(--border);}
.checkout-item-img{width:52px;height:65px;border-radius:8px;flex-shrink:0;display:flex;align-items:center;justify-content:center;font-size:22px;overflow:hidden;}
.checkout-item-name{font-size:13px;font-weight:600;margin-bottom:3px;line-height:1.3;}
.checkout-item-size{font-size:11px;color:var(--gray);}
.checkout-item-price{margin-left:auto;font-weight:700;font-size:14px;white-space:nowrap;}
.checkout-line{display:flex;justify-content:space-between;font-size:14px;margin-bottom:8px;color:var(--gray);}
.checkout-total{display:flex;justify-content:space-between;font-size:18px;font-weight:800;margin-top:12px;padding-top:12px;border-top:2px solid var(--border);}
.btn-place-order{width:100%;background:var(--terra);color:white;border:none;padding:16px;border-radius:100px;font-size:16px;font-weight:700;cursor:pointer;font-family:'Outfit',sans-serif;transition:all .25s;margin-top:20px;}
.btn-place-order:hover{background:var(--terra-light);transform:translateY(-2px);box-shadow:0 8px 28px rgba(196,98,45,0.4);}
.order-success-overlay{display:none;position:fixed;inset:0;background:rgba(28,23,18,0.7);z-index:2000;align-items:center;justify-content:center;}
.order-success-overlay.show{display:flex;}
.order-success-modal{background:white;border-radius:24px;padding:48px;text-align:center;max-width:440px;width:90%;animation:modalIn .4s ease;}
.success-icon{font-size:64px;margin-bottom:20px;display:block;}
.success-title{font-family:'Playfair Display',serif;font-size:28px;font-weight:800;margin-bottom:12px;color:var(--ink);}
.success-sub{font-size:15px;color:var(--gray);margin-bottom:28px;line-height:1.6;}
.success-order-num{background:var(--terra-pale);border-radius:10px;padding:12px 20px;font-weight:700;font-size:14px;margin-bottom:28px;display:inline-block;}

/* ─── ABOUT PAGE ─── */
.about-hero{background:linear-gradient(135deg,var(--terra-pale) 0%,var(--gold-light) 100%);padding:72px 64px;text-align:center;}
.about-hero-title{font-family:'Playfair Display',serif;font-size:52px;font-weight:900;margin-bottom:16px;}
.about-hero-title em{font-style:italic;color:var(--terra);}
.about-hero-sub{font-size:18px;color:var(--gray);max-width:560px;margin:0 auto;line-height:1.7;}
.about-content{padding:72px 64px;max-width:900px;margin:0 auto;}
.about-section{margin-bottom:64px;}
.about-section-title{font-family:'Playfair Display',serif;font-size:32px;font-weight:700;margin-bottom:16px;}
.about-section-title em{font-style:italic;color:var(--terra);}
.about-text{font-size:16px;color:var(--gray);line-height:1.8;margin-bottom:16px;}
.about-grid{display:grid;grid-template-columns:1fr 1fr;gap:24px;margin-top:24px;}
.about-card{background:white;border-radius:var(--radius);padding:24px;border:1px solid var(--border);}
.about-card-icon{font-size:32px;margin-bottom:12px;display:block;}
.about-card-title{font-weight:700;font-size:16px;margin-bottom:6px;}
.about-card-text{font-size:14px;color:var(--gray);line-height:1.6;}
.team-grid{display:grid;grid-template-columns:repeat(3,1fr);gap:24px;margin-top:28px;}
.team-card{text-align:center;background:white;border-radius:var(--radius);padding:28px 20px;border:1px solid var(--border);}
.team-avatar{width:72px;height:72px;border-radius:50%;display:flex;align-items:center;justify-content:center;font-size:28px;margin:0 auto 14px;background:var(--terra-pale);}
.team-name{font-weight:700;font-size:16px;margin-bottom:4px;}
.team-role{font-size:13px;color:var(--terra);font-weight:500;}
.contact-grid{display:grid;grid-template-columns:1fr 1fr;gap:40px;margin-top:28px;}
.contact-form{background:white;border-radius:20px;padding:32px;border:1px solid var(--border);}
.contact-info{display:flex;flex-direction:column;gap:20px;}
.contact-info-item{display:flex;gap:16px;align-items:flex-start;}
.contact-info-icon{width:44px;height:44px;background:var(--terra-pale);border-radius:12px;display:flex;align-items:center;justify-content:center;font-size:20px;flex-shrink:0;}
.contact-info-label{font-weight:600;font-size:14px;margin-bottom:4px;}
.contact-info-value{font-size:14px;color:var(--gray);}

/* ─── FOOTER ─── */
footer{background:var(--ink);color:rgba(255,255,255,0.8);padding:64px 40px 32px;}
.footer-grid{display:grid;grid-template-columns:2fr 1fr 1fr 1fr;gap:40px;margin-bottom:48px;}
.footer-brand .footer-logo{font-family:'Playfair Display',serif;font-size:22px;font-weight:900;color:white;margin-bottom:12px;}
.footer-brand .footer-logo span{color:var(--terra);}
.footer-brand p{font-size:14px;color:rgba(255,255,255,0.5);line-height:1.7;margin-bottom:20px;}
.footer-social{display:flex;gap:10px;}
.social-btn{width:36px;height:36px;background:rgba(255,255,255,0.08);border-radius:8px;display:flex;align-items:center;justify-content:center;font-size:16px;cursor:pointer;transition:all .2s;}
.social-btn:hover{background:var(--terra);}
.footer-col-title{font-size:13px;font-weight:700;text-transform:uppercase;letter-spacing:1px;color:white;margin-bottom:16px;}
.footer-col a{display:block;font-size:14px;color:rgba(255,255,255,0.5);text-decoration:none;margin-bottom:10px;cursor:pointer;transition:color .2s;}
.footer-col a:hover{color:var(--terra);}
.footer-bottom{border-top:1px solid rgba(255,255,255,0.08);padding-top:24px;display:flex;justify-content:space-between;align-items:center;font-size:13px;color:rgba(255,255,255,0.35);}
.footer-bottom span{color:var(--terra);}

/* ─── TOAST ─── */
.toast{position:fixed;bottom:32px;left:50%;transform:translateX(-50%) translateY(100px);background:var(--ink);color:white;padding:14px 24px;border-radius:100px;font-size:14px;font-weight:500;z-index:3000;transition:transform .35s ease;box-shadow:0 8px 32px rgba(0,0,0,0.3);white-space:nowrap;}
.toast.show{transform:translateX(-50%) translateY(0);}
.toast.success::before{content:'✓  ';}
.toast.error::before{content:'✕  ';color:var(--terra);}

/* ─── USER MENU ─── */
.user-menu{position:relative;}
.user-avatar{width:36px;height:36px;background:var(--terra);border-radius:50%;display:flex;align-items:center;justify-content:center;color:white;font-weight:700;font-size:13px;cursor:pointer;border:none;}
.user-dropdown{position:absolute;top:calc(100%+10px);right:0;background:white;border:1px solid var(--border);border-radius:14px;box-shadow:0 8px 32px var(--shadow);min-width:180px;overflow:hidden;display:none;z-index:600;}
.user-dropdown.open{display:block;}
.user-dropdown a{display:block;padding:12px 18px;font-size:14px;font-weight:500;color:var(--ink);text-decoration:none;cursor:pointer;transition:background .15s;}
.user-dropdown a:hover{background:var(--gray-light);}
.user-dropdown .dropdown-divider{border:none;border-top:1px solid var(--border);margin:4px 0;}
.user-dropdown .logout{color:var(--terra);}

/* ─── MOBILE MENU ─── */
.mobile-nav{position:fixed;inset:0;background:var(--warm-white);z-index:700;transform:translateX(-100%);transition:transform .3s ease;padding:80px 32px 32px;display:flex;flex-direction:column;gap:8px;}
.mobile-nav.open{transform:translateX(0);}
.mobile-nav a{font-family:'Playfair Display',serif;font-size:28px;font-weight:700;color:var(--ink);text-decoration:none;cursor:pointer;padding:8px 0;}
.mobile-nav a:hover{color:var(--terra);}
.mobile-nav-close{position:absolute;top:24px;right:24px;background:none;border:none;font-size:24px;cursor:pointer;}

/* ─── PAGE HERO BANNER ─── */
.page-banner{background:linear-gradient(135deg,var(--terra-pale),var(--gold-light));padding:48px 40px;border-bottom:1px solid var(--border);}
.page-banner h2{font-family:'Playfair Display',serif;font-size:40px;font-weight:800;margin-bottom:6px;}
.page-banner p{color:var(--gray);font-size:15px;}
.breadcrumb{font-size:13px;color:var(--gray);margin-bottom:12px;}
.breadcrumb span{cursor:pointer;transition:color .2s;}
.breadcrumb span:hover{color:var(--terra);}

/* ─── RESPONSIVE ─── */
@media(max-width:1024px){
  .hero{grid-template-columns:1fr;padding:40px 28px;min-height:auto;}
  .hero-visual{display:none;}
  .detail-layout{grid-template-columns:1fr;padding:32px 28px;gap:32px;}
  .detail-gallery{position:static;}
  .checkout-layout{grid-template-columns:1fr;padding:28px;}
  .footer-grid{grid-template-columns:1fr 1fr;gap:32px;}
  .shop-layout{grid-template-columns:1fr;gap:24px;}
  .shop-sidebar{position:static;}
  .about-grid,.contact-grid,.team-grid{grid-template-columns:1fr;}
}
@media(max-width:768px){
  nav{padding:0 20px;}
  .nav-links{display:none;}
  .hamburger{display:block;}
  .hero h1{font-size:40px;}
  .featured-section,.categories-strip,.why-section{padding:40px 20px;}
  .cart-drawer{width:100%;}
  .checkout-layout{padding:20px;}
  .about-hero,.about-content{padding:40px 24px;}
  .footer-grid{grid-template-columns:1fr;gap:24px;}
  .section-title{font-size:28px;}
}
</style>
</head>
<body>

<!-- ═══ NAVBAR ═══ -->
<nav id="navbar">
  <div class="nav-logo" onclick="showPage('home')">Sree<span>Digitals</span></div>
  <div class="nav-links">
    <a onclick="showPage('home')" id="nav-home" class="active">Home</a>
    <a onclick="showPage('shop')" id="nav-shop">Shop</a>
    <a onclick="showPage('about')" id="nav-about">About</a>
    <a onclick="showPage('about','contact')" id="nav-contact">Contact</a>
  </div>
  <div class="nav-actions">
    <div id="auth-area">
      <button class="btn-ghost" onclick="openAuth('login')">Log In</button>
      <button class="btn-primary" onclick="openAuth('signup')">Sign Up</button>
    </div>
    <div id="user-area" style="display:none;">
      <div class="user-menu">
        <button class="user-avatar" id="user-avatar-btn" onclick="toggleUserMenu()">S</button>
        <div class="user-dropdown" id="user-dropdown">
          <a>👤 My Profile</a>
          <a onclick="showPage('shop')">📚 My Downloads</a>
          <a>🛒 Order History</a>
          <hr class="dropdown-divider">
          <a class="logout" onclick="logout()">← Log Out</a>
        </div>
      </div>
    </div>
    <button class="cart-btn" onclick="openCart()">
      🛒
      <span class="cart-badge" id="cart-badge">0</span>
    </button>
    <button class="hamburger" onclick="toggleMobileNav()">☰</button>
  </div>
</nav>

<!-- Mobile Nav -->
<div class="mobile-nav" id="mobile-nav">
  <button class="mobile-nav-close" onclick="toggleMobileNav()">✕</button>
  <a onclick="showPage('home');toggleMobileNav()">Home</a>
  <a onclick="showPage('shop');toggleMobileNav()">Shop</a>
  <a onclick="showPage('about');toggleMobileNav()">About</a>
  <a onclick="showPage('about','contact');toggleMobileNav()">Contact</a>
</div>

<!-- ═══ PAGE: HOME ═══ -->
<div class="page active" id="page-home">

  <!-- Hero -->
  <section class="hero">
    <div class="hero-content">
      <div class="hero-eyebrow">✦ Digital Downloads — Instant Access</div>
      <h1>Create. Print.<br><em>Live Freely.</em></h1>
      <p class="hero-sub">Beautiful digital coloring books, wall art, planners & Instagram templates — designed to pull you away from doom scrolling and back into real life.</p>
      <div class="hero-btns">
        <button class="btn-lg btn-lg-primary" onclick="showPage('shop')">Shop All Products</button>
        <button class="btn-lg btn-lg-outline" onclick="showPage('about')">Our Story</button>
      </div>
      <div class="hero-stats">
        <div class="stat"><div class="stat-num">2,400+</div><div class="stat-label">Happy Customers</div></div>
        <div class="stat"><div class="stat-num">120+</div><div class="stat-label">Digital Products</div></div>
        <div class="stat"><div class="stat-num">4.9★</div><div class="stat-label">Average Rating</div></div>
      </div>
    </div>
    <div class="hero-visual">
      <div class="hero-grid">
        <div class="hero-card">
          <div class="hero-card-img coloring">🎨</div>
        </div>
        <div class="hero-card hero-card-offset">
          <div class="hero-card-img planner">📅</div>
        </div>
        <div class="hero-card">
          <div class="hero-card-img poster">🖼️</div>
        </div>
        <div class="hero-card hero-card-offset">
          <div class="hero-card-img instagram">📸</div>
        </div>
      </div>
      <div class="hero-float-tag float-tag-1">✓ Instant Download</div>
      <div class="hero-float-tag float-tag-2">🖨️ Print-Ready Files</div>
    </div>
  </section>

  <!-- Marquee -->
  <div class="marquee-section">
    <div class="marquee-track" id="marquee">
      <div class="marquee-item">Coloring Books <span>✦</span></div>
      <div class="marquee-item">Wall Posters <span>✦</span></div>
      <div class="marquee-item">Digital Planners <span>✦</span></div>
      <div class="marquee-item">Instagram Cards <span>✦</span></div>
      <div class="marquee-item">Kids' Activity Sheets <span>✦</span></div>
      <div class="marquee-item">Habit Trackers <span>✦</span></div>
      <div class="marquee-item">Cinephile Journals <span>✦</span></div>
      <div class="marquee-item">Printable Art <span>✦</span></div>
      <div class="marquee-item">Coloring Books <span>✦</span></div>
      <div class="marquee-item">Wall Posters <span>✦</span></div>
      <div class="marquee-item">Digital Planners <span>✦</span></div>
      <div class="marquee-item">Instagram Cards <span>✦</span></div>
      <div class="marquee-item">Kids' Activity Sheets <span>✦</span></div>
      <div class="marquee-item">Habit Trackers <span>✦</span></div>
      <div class="marquee-item">Cinephile Journals <span>✦</span></div>
      <div class="marquee-item">Printable Art <span>✦</span></div>
    </div>
  </div>

  <!-- Categories -->
  <section class="categories-strip">
    <div class="section-label">Browse by Category</div>
    <div class="cat-scroll">
      <div class="cat-chip active" onclick="filterCategory(this,'all')"><span class="cat-icon">✨</span> All Products</div>
      <div class="cat-chip" onclick="filterCategory(this,'coloring')"><span class="cat-icon">🎨</span> Coloring Books</div>
      <div class="cat-chip" onclick="filterCategory(this,'poster')"><span class="cat-icon">🖼️</span> Wall Posters</div>
      <div class="cat-chip" onclick="filterCategory(this,'planner')"><span class="cat-icon">📅</span> Planners</div>
      <div class="cat-chip" onclick="filterCategory(this,'instagram')"><span class="cat-icon">📸</span> Instagram Cards</div>
      <div class="cat-chip" onclick="filterCategory(this,'kids')"><span class="cat-icon">🧸</span> Kids</div>
      <div class="cat-chip" onclick="filterCategory(this,'cinema')"><span class="cat-icon">🎬</span> Cinema</div>
    </div>
  </section>

  <!-- Featured Products -->
  <section class="featured-section">
    <div class="section-header">
      <div class="section-title">Trending <span>Right Now</span></div>
      <a class="see-all" onclick="showPage('shop')">View all products →</a>
    </div>
    <div class="products-grid" id="home-products"></div>
  </section>

  <!-- Why Us -->
  <section class="why-section">
    <div class="section-label">Why SreeDigitals</div>
    <div class="section-title" style="margin-bottom:0">Everything you need,<br><em style="font-style:italic;color:var(--terra)">nothing you don't.</em></div>
    <div class="why-grid">
      <div class="why-card">
        <span class="why-icon">⚡</span>
        <div class="why-title">Instant Download</div>
        <div class="why-desc">Buy and download your files immediately. No waiting, no shipping — your files are ready the moment you pay.</div>
      </div>
      <div class="why-card">
        <span class="why-icon">🖨️</span>
        <div class="why-title">Print Any Size</div>
        <div class="why-desc">All files are high-resolution and print-ready. Choose A4, A3, Letter, 8×10 or custom — perfect every time.</div>
      </div>
      <div class="why-card">
        <span class="why-icon">♾️</span>
        <div class="why-title">Yours Forever</div>
        <div class="why-desc">Every purchase is saved in your personal library forever. Re-download anytime from any device.</div>
      </div>
      <div class="why-card">
        <span class="why-icon">🧠</span>
        <div class="why-title">Good for Your Mind</div>
        <div class="why-desc">Designed to replace screen fatigue with purposeful creativity — natural dopamine, no algorithm.</div>
      </div>
    </div>
  </section>

  <!-- Footer CTA -->
  <section style="background:var(--ink);padding:72px 40px;text-align:center;">
    <div style="font-family:'Caveat',cursive;font-size:20px;color:var(--terra-light);margin-bottom:12px;">Ready to get started?</div>
    <div style="font-family:'Playfair Display',serif;font-size:42px;font-weight:800;color:white;margin-bottom:16px;line-height:1.2;">Stop scrolling.<br><em style="font-style:italic;color:var(--terra)">Start creating.</em></div>
    <p style="color:rgba(255,255,255,0.5);font-size:16px;margin-bottom:32px;max-width:440px;margin-left:auto;margin-right:auto;line-height:1.7;">Join thousands of creators, parents, planners and film lovers who chose real creativity over the feed.</p>
    <button class="btn-lg btn-lg-primary" onclick="showPage('shop')">Explore the Shop</button>
  </section>

  <footer>
    <div class="footer-grid">
      <div class="footer-brand">
        <div class="footer-logo">Sree<span>Digitals</span></div>
        <p>Beautiful digital downloads for creative souls. Coloring books, planners, wall art and more — made to bring you back to life.</p>
        <div class="footer-social">
          <div class="social-btn">📸</div>
          <div class="social-btn">🐦</div>
          <div class="social-btn">💬</div>
          <div class="social-btn">📌</div>
        </div>
      </div>
      <div class="footer-col">
        <div class="footer-col-title">Shop</div>
        <a onclick="showPage('shop')">All Products</a>
        <a onclick="filterCategory(null,'coloring');showPage('shop')">Coloring Books</a>
        <a onclick="filterCategory(null,'poster');showPage('shop')">Wall Posters</a>
        <a onclick="filterCategory(null,'planner');showPage('shop')">Planners</a>
        <a onclick="filterCategory(null,'instagram');showPage('shop')">Instagram Cards</a>
      </div>
      <div class="footer-col">
        <div class="footer-col-title">Company</div>
        <a onclick="showPage('about')">About Us</a>
        <a onclick="showPage('about','contact')">Contact</a>
        <a>Blog</a>
        <a>Affiliate Program</a>
      </div>
      <div class="footer-col">
        <div class="footer-col-title">Support</div>
        <a>FAQ</a>
        <a>How to Download</a>
        <a>Print Guide</a>
        <a>Privacy Policy</a>
        <a>Terms of Service</a>
      </div>
    </div>
    <div class="footer-bottom">
      <span>© 2026 <span>SreeDigitals</span>. All rights reserved.</span>
      <span>Made with ♥ for creative souls</span>
    </div>
  </footer>
</div>

<!-- ═══ PAGE: SHOP ═══ -->
<div class="page" id="page-shop">
  <div class="shop-page-header">
    <div class="breadcrumb"><span onclick="showPage('home')">Home</span> / <span>Shop</span></div>
    <div class="shop-page-title">Our <em>Collection</em></div>
    <p style="color:var(--gray);font-size:15px;margin-top:8px;">120+ instant-download digital products</p>
  </div>

  <div class="shop-layout">
    <!-- Sidebar Filters -->
    <aside class="shop-sidebar">
      <div class="filter-section">
        <div class="filter-title">Category</div>
        <label class="filter-option"><input type="radio" name="cat-filter" value="all" checked onchange="applyFilters()"> All Products</label>
        <label class="filter-option"><input type="radio" name="cat-filter" value="coloring" onchange="applyFilters()"> 🎨 Coloring Books</label>
        <label class="filter-option"><input type="radio" name="cat-filter" value="poster" onchange="applyFilters()"> 🖼️ Wall Posters</label>
        <label class="filter-option"><input type="radio" name="cat-filter" value="planner" onchange="applyFilters()"> 📅 Planners</label>
        <label class="filter-option"><input type="radio" name="cat-filter" value="instagram" onchange="applyFilters()"> 📸 Instagram Cards</label>
        <label class="filter-option"><input type="radio" name="cat-filter" value="kids" onchange="applyFilters()"> 🧸 Kids</label>
        <label class="filter-option"><input type="radio" name="cat-filter" value="cinema" onchange="applyFilters()"> 🎬 Cinema</label>
      </div>
      <div class="filter-section">
        <div class="filter-title">Price Range</div>
        <div class="price-range">
          <div class="price-inputs">
            <input type="number" placeholder="₹0" id="price-min" onchange="applyFilters()" min="0">
            <input type="number" placeholder="₹999" id="price-max" onchange="applyFilters()" min="0">
          </div>
        </div>
      </div>
      <div class="filter-section">
        <div class="filter-title">Format</div>
        <label class="filter-option"><input type="checkbox" value="pdf" onchange="applyFilters()"> PDF</label>
        <label class="filter-option"><input type="checkbox" value="jpg" onchange="applyFilters()"> JPG / PNG</label>
        <label class="filter-option"><input type="checkbox" value="svg" onchange="applyFilters()"> SVG (Editable)</label>
      </div>
      <button class="btn-ghost" style="width:100%;margin-top:8px;" onclick="resetFilters()">Reset Filters</button>
    </aside>

    <!-- Products -->
    <div>
      <div class="shop-main-header">
        <span class="shop-count" id="shop-count">Showing all products</span>
        <select class="sort-select" onchange="applyFilters()">
          <option value="featured">Featured</option>
          <option value="price-asc">Price: Low to High</option>
          <option value="price-desc">Price: High to Low</option>
          <option value="newest">Newest</option>
          <option value="rating">Top Rated</option>
        </select>
      </div>
      <div class="products-grid" id="shop-products"></div>
    </div>
  </div>

  <footer style="margin-top:80px;">
    <div class="footer-bottom" style="border-top:1px solid rgba(255,255,255,0.08);padding:24px 40px;display:flex;justify-content:space-between;font-size:13px;color:rgba(255,255,255,0.35);background:var(--ink);">
      <span>© 2026 <span style="color:var(--terra)">SreeDigitals</span></span>
      <span>Made with ♥</span>
    </div>
  </footer>
</div>

<!-- ═══ PAGE: PRODUCT DETAIL ═══ -->
<div class="page" id="page-detail">
  <div style="padding:16px 64px 0;" id="detail-breadcrumb"></div>
  <div class="detail-layout">
    <div class="detail-gallery">
      <div class="detail-main-img" id="detail-main-img"></div>
      <div class="detail-thumbs" id="detail-thumbs"></div>
    </div>
    <div class="detail-content">
      <div class="detail-cat" id="detail-cat"></div>
      <div class="detail-name" id="detail-name"></div>
      <div class="detail-rating">
        <span class="stars" id="detail-stars"></span>
        <span class="count" id="detail-rating-count"></span>
      </div>
      <div class="detail-price" id="detail-price"></div>
      <p class="detail-desc" id="detail-desc"></p>
      <div class="detail-options">
        <div class="detail-options-label">Print Size</div>
        <div class="size-chips">
          <div class="size-chip active" onclick="selectSize(this)">A4</div>
          <div class="size-chip" onclick="selectSize(this)">A3</div>
          <div class="size-chip" onclick="selectSize(this)">Letter</div>
          <div class="size-chip" onclick="selectSize(this)">8×10"</div>
          <div class="size-chip" onclick="selectSize(this)">Custom</div>
        </div>
      </div>
      <div class="detail-actions">
        <button class="btn-add-cart" id="detail-add-cart">Add to Cart</button>
        <button class="btn-wishlist-d" id="detail-wishlist" onclick="toggleDetailWishlist(this)">🤍</button>
      </div>
      <div class="detail-features">
        <div class="detail-feature">Instant digital download after purchase</div>
        <div class="detail-feature">High-resolution print-ready file (300 DPI)</div>
        <div class="detail-feature">Multiple sizes included in download</div>
        <div class="detail-feature">Commercial licence — print as many as you need</div>
        <div class="detail-feature">Lifetime access in your personal library</div>
      </div>
    </div>
  </div>

  <!-- Reviews -->
  <div class="detail-reviews">
    <div class="section-title" style="margin-bottom:28px;">Customer <span>Reviews</span></div>
    <div id="detail-reviews-container"></div>
  </div>

  <footer style="margin-top:0;">
    <div class="footer-bottom" style="border-top:1px solid rgba(255,255,255,0.08);padding:24px 40px;display:flex;justify-content:space-between;font-size:13px;color:rgba(255,255,255,0.35);background:var(--ink);">
      <span>© 2026 <span style="color:var(--terra)">SreeDigitals</span></span>
      <span>Made with ♥</span>
    </div>
  </footer>
</div>

<!-- ═══ PAGE: CHECKOUT ═══ -->
<div class="page" id="page-checkout">
  <div class="page-banner">
    <div class="breadcrumb"><span onclick="openCart()">Cart</span> / Checkout</div>
    <h2>Checkout</h2>
    <p>You're almost there — complete your purchase below.</p>
  </div>

  <div class="checkout-layout">
    <div>
      <!-- Contact -->
      <div class="checkout-form-section">
        <div class="checkout-section-title"><span class="step-num">1</span> Contact Information</div>
        <div class="form-row">
          <div class="form-group"><label class="form-label">First Name</label><input class="form-input" id="co-fname" placeholder="Sree"></div>
          <div class="form-group"><label class="form-label">Last Name</label><input class="form-input" id="co-lname" placeholder="Lakshmi"></div>
        </div>
        <div class="form-group"><label class="form-label">Email Address</label><input class="form-input" id="co-email" type="email" placeholder="hello@example.com"></div>
        <div class="form-group"><label class="form-label">Phone Number</label><input class="form-input" id="co-phone" placeholder="+91 98765 43210"></div>
      </div>

      <!-- Payment -->
      <div class="checkout-form-section">
        <div class="checkout-section-title"><span class="step-num">2</span> Payment Method</div>
        <div class="payment-method selected" onclick="selectPayment(this)">
          <input type="radio" name="payment" checked>
          <div class="payment-method-info">
            <div class="payment-method-name">UPI</div>
            <div class="payment-method-sub">Google Pay, PhonePe, Paytm, BHIM</div>
          </div>
          <div class="payment-icons"><span class="payment-icon">GPay</span><span class="payment-icon">UPI</span></div>
        </div>
        <div class="payment-method" onclick="selectPayment(this)">
          <input type="radio" name="payment">
          <div class="payment-method-info">
            <div class="payment-method-name">Credit / Debit Card</div>
            <div class="payment-method-sub">Visa, Mastercard, Rupay</div>
          </div>
          <div class="payment-icons"><span class="payment-icon">VISA</span><span class="payment-icon">MC</span></div>
        </div>
        <div id="card-fields" style="display:none;margin-top:16px;">
          <div class="form-group"><label class="form-label">Card Number</label><input class="form-input" placeholder="1234 5678 9012 3456" maxlength="19" oninput="formatCard(this)"></div>
          <div class="form-row">
            <div class="form-group"><label class="form-label">Expiry</label><input class="form-input" placeholder="MM / YY" maxlength="7"></div>
            <div class="form-group"><label class="form-label">CVV</label><input class="form-input" placeholder="•••" maxlength="3"></div>
          </div>
          <div class="form-group"><label class="form-label">Name on Card</label><input class="form-input" placeholder="As printed on card"></div>
        </div>
        <div class="payment-method" onclick="selectPayment(this)">
          <input type="radio" name="payment">
          <div class="payment-method-info">
            <div class="payment-method-name">Wallet</div>
            <div class="payment-method-sub">Paytm Wallet, Amazon Pay, Airtel Money</div>
          </div>
        </div>

        <div style="margin-top:16px;padding:12px 16px;background:var(--sage-light);border-radius:10px;font-size:13px;color:#3a6b3e;display:flex;align-items:center;gap:8px;">
          🔒 All transactions are encrypted and secure. We never store your card details.
        </div>
      </div>

      <!-- UPI field -->
      <div class="checkout-form-section">
        <div class="checkout-section-title"><span class="step-num">3</span> UPI / Coupon</div>
        <div class="form-group"><label class="form-label">UPI ID (if paying via UPI)</label><input class="form-input" placeholder="yourname@upi"></div>
        <div class="form-group"><label class="form-label">Coupon Code</label>
          <div style="display:flex;gap:8px;">
            <input class="form-input" id="co-coupon" placeholder="Enter coupon code" style="flex:1;">
            <button class="promo-apply" onclick="applyCoupon()">Apply</button>
          </div>
        </div>
        <div id="coupon-msg" style="font-size:13px;margin-top:6px;display:none;"></div>
      </div>
    </div>

    <!-- Order Summary -->
    <div>
      <div class="checkout-order-summary">
        <div class="checkout-order-title">Order Summary</div>
        <div id="checkout-items"></div>
        <div class="checkout-line"><span>Subtotal</span><span id="co-subtotal">₹0</span></div>
        <div class="checkout-line"><span>Discount</span><span id="co-discount" style="color:var(--sage);">-₹0</span></div>
        <div class="checkout-line"><span>Download Fee</span><span style="color:var(--sage)">FREE</span></div>
        <div class="checkout-total"><span>Total</span><span id="co-total">₹0</span></div>
        <button class="btn-place-order" onclick="placeOrder()">Place Order & Pay</button>
        <p style="text-align:center;font-size:12px;color:var(--gray);margin-top:12px;line-height:1.6;">By placing your order, you agree to our Terms of Service and Privacy Policy.</p>
      </div>
    </div>
  </div>
</div>

<!-- ═══ PAGE: ABOUT ═══ -->
<div class="page" id="page-about">
  <div class="about-hero">
    <div style="font-family:'Caveat',cursive;font-size:20px;color:var(--terra);margin-bottom:8px;">Our Story</div>
    <div class="about-hero-title">Born from a <em>love</em> of<br>offline creativity</div>
    <p class="about-hero-sub">SreeDigitals was built for everyone tired of mindless scrolling — and ready to create something beautiful instead.</p>
  </div>

  <div class="about-content">
    <div class="about-section">
      <div class="about-section-title">Why we <em>exist</em></div>
      <p class="about-text">SreeDigitals was born from a simple frustration: too much screen time, not enough real-world creativity. We set out to build a marketplace of beautiful digital products that give people a reason to put down their phone, pick up a pencil, or decorate their space.</p>
      <p class="about-text">Every product in our collection is designed with intention — from mandala coloring books for mindful evenings, to aesthetic wall posters for inspiring spaces, to daily planners that actually help you stay focused.</p>
      <div class="about-grid">
        <div class="about-card">
          <span class="about-card-icon">🎯</span>
          <div class="about-card-title">Our Mission</div>
          <div class="about-card-text">Replace doom scrolling with meaningful creativity. One beautiful download at a time.</div>
        </div>
        <div class="about-card">
          <span class="about-card-icon">💡</span>
          <div class="about-card-title">Our Vision</div>
          <div class="about-card-text">A world where every person has access to beautiful, affordable tools for a more intentional life.</div>
        </div>
        <div class="about-card">
          <span class="about-card-icon">❤️</span>
          <div class="about-card-title">Our Values</div>
          <div class="about-card-text">Creativity, accessibility, mindfulness, and joy. We believe beautiful things should be available to everyone.</div>
        </div>
        <div class="about-card">
          <span class="about-card-icon">🤝</span>
          <div class="about-card-title">Our Promise</div>
          <div class="about-card-text">Every product is tested for quality. If you're not happy, we make it right. Always.</div>
        </div>
      </div>
    </div>

    <div class="about-section">
      <div class="about-section-title">Meet the <em>team</em></div>
      <p class="about-text">We're a small, passionate team of designers, educators, and creatives based in India.</p>
      <div class="team-grid">
        <div class="team-card">
          <div class="team-avatar">🎨</div>
          <div class="team-name">Sreelakshmi</div>
          <div class="team-role">Founder & Lead Designer</div>
        </div>
        <div class="team-card">
          <div class="team-avatar">✏️</div>
          <div class="team-name">Arjun Nair</div>
          <div class="team-role">Illustrator & Content Creator</div>
        </div>
        <div class="team-card">
          <div class="team-avatar">💻</div>
          <div class="team-name">Priya Menon</div>
          <div class="team-role">Tech & Product Manager</div>
        </div>
      </div>
    </div>

    <div class="about-section" id="contact-section">
      <div class="about-section-title">Get in <em>touch</em></div>
      <p class="about-text">Have a question, a custom request, or just want to say hi? We'd love to hear from you.</p>
      <div class="contact-grid">
        <div class="contact-form">
          <div class="form-row">
            <div class="form-group"><label class="form-label">Name</label><input class="form-input" placeholder="Your name"></div>
            <div class="form-group"><label class="form-label">Email</label><input class="form-input" type="email" placeholder="you@example.com"></div>
          </div>
          <div class="form-group"><label class="form-label">Subject</label><input class="form-input" placeholder="How can we help?"></div>
          <div class="form-group"><label class="form-label">Message</label><textarea class="form-input" rows="4" placeholder="Tell us more…" style="resize:vertical;"></textarea></div>
          <button class="btn-submit" onclick="sendMessage()">Send Message</button>
        </div>
        <div class="contact-info">
          <div class="contact-info-item">
            <div class="contact-info-icon">📧</div>
            <div><div class="contact-info-label">Email</div><div class="contact-info-value">hello@sreedigitals.in</div></div>
          </div>
          <div class="contact-info-item">
            <div class="contact-info-icon">📱</div>
            <div><div class="contact-info-label">WhatsApp</div><div class="contact-info-value">+91 98765 43210</div></div>
          </div>
          <div class="contact-info-item">
            <div class="contact-info-icon">📸</div>
            <div><div class="contact-info-label">Instagram</div><div class="contact-info-value">@sreedigitals</div></div>
          </div>
          <div class="contact-info-item">
            <div class="contact-info-icon">⏰</div>
            <div><div class="contact-info-label">Response Time</div><div class="contact-info-value">We reply within 24 hours, Monday–Saturday.</div></div>
          </div>
        </div>
      </div>
    </div>
  </div>

  <footer>
    <div class="footer-bottom" style="padding:24px 40px;display:flex;justify-content:space-between;font-size:13px;color:rgba(255,255,255,0.35);background:var(--ink);">
      <span>© 2026 <span style="color:var(--terra)">SreeDigitals</span></span>
      <span>Made with ♥</span>
    </div>
  </footer>
</div>

<!-- ═══ CART DRAWER ═══ -->
<div class="cart-overlay" id="cart-overlay" onclick="closeCart()"></div>
<div class="cart-drawer" id="cart-drawer">
  <div class="cart-header">
    <div class="cart-title">Your Cart</div>
    <button class="cart-close" onclick="closeCart()">✕</button>
  </div>
  <div class="cart-items" id="cart-items-container"></div>
  <div class="cart-footer" id="cart-footer" style="display:none;">
    <div class="promo-row">
      <input class="promo-input" id="promo-input" placeholder="Promo code (try SREE10)">
      <button class="promo-apply" onclick="applyPromo()">Apply</button>
    </div>
    <div class="cart-subtotal"><span>Subtotal</span><span id="cart-subtotal">₹0</span></div>
    <div class="cart-subtotal" id="discount-row" style="display:none;color:var(--sage);"><span>Discount</span><span id="cart-discount">-₹0</span></div>
    <div class="cart-total"><span>Total</span><span id="cart-total">₹0</span></div>
    <button class="btn-checkout" onclick="goToCheckout()">Proceed to Checkout →</button>
  </div>
</div>

<!-- ═══ AUTH MODAL ═══ -->
<div class="modal-overlay" id="auth-modal">
  <div class="modal" style="position:relative;">
    <div class="modal-header">
      <button class="modal-close-x" onclick="closeAuth()">✕</button>
      <div class="modal-logo">Sree<span>Digitals</span></div>
      <div class="modal-title" id="auth-modal-title">Welcome back</div>
      <div class="modal-sub" id="auth-modal-sub">Log in to access your downloads</div>
    </div>
    <div class="modal-body">
      <div class="modal-tabs">
        <button class="modal-tab active" onclick="switchAuthTab('login',this)">Log In</button>
        <button class="modal-tab" onclick="switchAuthTab('signup',this)">Sign Up</button>
      </div>
      <div id="auth-form-container"></div>
    </div>
  </div>
</div>

<!-- ═══ ORDER SUCCESS MODAL ═══ -->
<div class="order-success-overlay" id="order-success-overlay">
  <div class="order-success-modal">
    <span class="success-icon">🎉</span>
    <div class="success-title">Order Confirmed!</div>
    <p class="success-sub">Your purchase was successful. Your files are ready to download in your personal library. Check your email for the confirmation.</p>
    <div class="success-order-num" id="success-order-num">Order #SD-000000</div>
    <button class="btn-lg btn-lg-primary" style="width:100%;margin-bottom:12px;" onclick="closeOrderSuccess()">Go to My Library</button>
    <button class="btn-lg btn-lg-outline" style="width:100%;border:2px solid var(--border);" onclick="closeOrderSuccess();showPage('shop')">Continue Shopping</button>
  </div>
</div>

<!-- ═══ TOAST ═══ -->
<div class="toast" id="toast"></div>

<script>
// ─── DATA ─────────────────────────────────────────────────────────────
const PRODUCTS = [
  {id:1, name:"Botanical Mandala Coloring Book", cat:"coloring", emoji:"🌿", bg:"linear-gradient(135deg,#FFF5E6,#FFD4AA)", price:249, original:399, badge:"Bestseller", rating:4.9, reviews:284, desc:"A 40-page digital coloring book filled with intricate botanical mandalas. Perfect for stress relief, meditation and mindful evenings. Print in A4 or A3 for the best experience.", format:"PDF"},
  {id:2, name:"2024 Daily Life Planner", cat:"planner", emoji:"📅", bg:"linear-gradient(135deg,#E8F4E8,#BDDCBD)", price:199, original:299, badge:"New", rating:4.8, reviews:156, desc:"A beautifully designed 365-day planner with habit trackers, mood logs, weekly spreads and monthly reviews. Designed for real productivity without overwhelm.", format:"PDF"},
  {id:3, name:"Minimal Aesthetic Wall Poster Set", cat:"poster", emoji:"🖼️", bg:"linear-gradient(135deg,#E8E4F4,#C4B8E0)", price:149, original:null, badge:null, rating:4.7, reviews:98, desc:"6 minimal, museum-quality wall art prints in muted tones. Perfect for living rooms, offices and bedrooms. Print at A4, A3 or frame at 8×10.", format:"JPG"},
  {id:4, name:"Instagram Aesthetic Card Pack", cat:"instagram", emoji:"📸", bg:"linear-gradient(135deg,#FFF0E8,#FFCDB8)", price:179, original:249, badge:"Sale", rating:4.8, reviews:203, desc:"30 beautifully designed Instagram story and post templates in a warm, aesthetic palette. Edit-ready and consistent — post daily without the stress.", format:"JPG/PNG"},
  {id:5, name:"Kids Dinosaur Coloring Adventure", cat:"kids", emoji:"🦕", bg:"linear-gradient(135deg,#E8F4E8,#BDDCBD)", price:129, original:199, badge:"Bestseller", rating:4.9, reviews:412, desc:"A 30-page coloring adventure for children aged 4–10. Features 30 unique dinosaur characters in friendly, easy-to-color designs. Print as many times as you like!", format:"PDF"},
  {id:6, name:"Cinephile Movie Journal", cat:"cinema", emoji:"🎬", bg:"linear-gradient(135deg,#2D1F4E,#6B4FBB)", price:219, original:349, badge:"New", rating:4.9, reviews:87, desc:"Track every film you watch with this gorgeous movie journal. Includes rating grids, director notes, genre trackers and 52 weekly film picks. For serious cinema lovers.", format:"PDF"},
  {id:7, name:"Floral Pattern Coloring Pages", cat:"coloring", emoji:"🌸", bg:"linear-gradient(135deg,#FFE4F0,#FFBBD8)", price:99, original:149, badge:null, rating:4.6, reviews:167, desc:"24 detailed floral coloring pages ranging from simple to intricate. Perfect for adults and older children. Each page is designed to be meditative and beautiful.", format:"PDF"},
  {id:8, name:"Habit Tracker Bundle (12 Designs)", cat:"planner", emoji:"✅", bg:"linear-gradient(135deg,#FFF5E6,#FFD4AA)", price:159, original:229, badge:"Bestseller", rating:4.7, reviews:319, desc:"12 gorgeous habit tracker designs for the whole year. Track water, sleep, exercise, reading, journaling and more. Designed to feel rewarding, not punishing.", format:"PDF"},
  {id:9, name:"Boho Wall Art Collection", cat:"poster", emoji:"🌙", bg:"linear-gradient(135deg,#F5F0E8,#E8DCC8)", price:189, original:null, badge:"New", rating:4.8, reviews:74, desc:"8 boho-inspired wall art prints featuring celestial motifs, sun faces, moons and abstract botanical elements. Warm tones that elevate any space instantly.", format:"JPG"},
  {id:10, name:"Kids Fairy Tale Coloring World", cat:"kids", emoji:"🧚", bg:"linear-gradient(135deg,#E8E4F4,#D4CCEB)", price:139, original:189, badge:null, rating:4.9, reviews:278, desc:"Step into a magical world with 28 fairy-tale coloring pages. Features enchanted forests, castles, fairies and friendly dragons. For ages 5–12.", format:"PDF"},
  {id:11, name:"Travel Memory Journal", cat:"planner", emoji:"✈️", bg:"linear-gradient(135deg,#E8F4F8,#B8D4E0)", price:229, original:299, badge:null, rating:4.7, reviews:143, desc:"Document your travels beautifully with this printable travel journal. Includes packing lists, destination pages, photo prompts, map sketches and memories grids.", format:"PDF"},
  {id:12, name:"Reels Content Calendar", cat:"instagram", emoji:"🎥", bg:"linear-gradient(135deg,#FFE4E4,#FFB8B8)", price:149, original:219, badge:"Sale", rating:4.6, reviews:198, desc:"Plan 3 months of Instagram Reels content with this interactive content calendar. Includes niche prompts, captions and hook ideas. Perfect for creators and small businesses.", format:"PDF"},
];

const REVIEWS_DATA = [
  {name:"Ananya R.", date:"Jan 2026", stars:"★★★★★", text:"Absolutely love the Botanical Mandala book! The quality is incredible and it printed perfectly on A3. My evening wind-down ritual now."},
  {name:"Pradeep K.", date:"Dec 2025", stars:"★★★★★", text:"The planner has completely changed how I work. The layout is thoughtful and the design is beautiful. Worth every rupee."},
  {name:"Meera S.", date:"Feb 2026", stars:"★★★★☆", text:"Great products overall. The Instagram templates saved me so much time. Would love even more variety!"},
  {name:"Rohit V.", date:"Jan 2026", stars:"★★★★★", text:"Bought the kids dinosaur book for my 6-year-old. He's been coloring for hours! No more iPad complaints. Best ₹129 I've spent."},
];

// ─── STATE ────────────────────────────────────────────────────────────
let cart = JSON.parse(localStorage.getItem('sd_cart')||'[]');
let currentUser = JSON.parse(localStorage.getItem('sd_user')||'null');
let currentProduct = null;
let currentDiscount = 0;
let activeCat = 'all';

// ─── INIT ─────────────────────────────────────────────────────────────
document.addEventListener('DOMContentLoaded', ()=>{
  renderHomeProducts();
  renderShopProducts(PRODUCTS);
  updateCartUI();
  if(currentUser) showUserUI();

  window.addEventListener('scroll',()=>{
    document.getElementById('navbar').classList.toggle('scrolled', window.scrollY>20);
  });

  document.addEventListener('click', e=>{
    const dd = document.getElementById('user-dropdown');
    if(dd && !dd.parentElement.contains(e.target)) dd.classList.remove('open');
  });
});

// ─── PAGES ────────────────────────────────────────────────────────────
function showPage(page, section){
  document.querySelectorAll('.page').forEach(p=>p.classList.remove('active'));
  document.getElementById('page-'+page).classList.add('active');
  document.querySelectorAll('.nav-links a').forEach(a=>a.classList.remove('active'));
  const navEl = document.getElementById('nav-'+page);
  if(navEl) navEl.classList.add('active');
  window.scrollTo({top:0,behavior:'smooth'});
  if(section==='contact'){
    setTimeout(()=>{
      document.getElementById('contact-section')?.scrollIntoView({behavior:'smooth',block:'start'});
    },300);
  }
}

// ─── PRODUCT RENDERING ────────────────────────────────────────────────
function productCard(p, clickable=true){
  const sale = p.original ? Math.round((1-p.price/p.original)*100) : 0;
  return `<div class="product-card" ${clickable?`onclick="openDetail(${p.id})"`:''}">
    <div class="product-card-img" style="background:${p.bg};">
      <span style="font-size:56px">${p.emoji}</span>
      ${p.badge?`<span class="product-card-badge ${p.badge==='New'?'new':p.badge==='Sale'?'sale':''}">${p.badge}</span>`:''}
      <button class="product-card-wishlist" onclick="event.stopPropagation();toggleWishlist(this,${p.id})">🤍</button>
    </div>
    <div class="product-card-body">
      <div class="product-card-cat">${catLabel(p.cat)}</div>
      <div class="product-card-name">${p.name}</div>
      <div class="product-card-meta">
        <div class="product-card-price">₹${p.price}${p.original?`<span class="original">₹${p.original}</span>`:''}</div>
        <div class="rating"><span class="stars">★</span>${p.rating} (${p.reviews})</div>
      </div>
    </div>
    <button class="product-card-add" onclick="event.stopPropagation();addToCart(${p.id},'A4')">+ Add to Cart</button>
  </div>`;
}

function catLabel(cat){
  const m={coloring:'Coloring Book',poster:'Wall Poster',planner:'Planner',instagram:'Instagram Cards',kids:'Kids',cinema:'Cinema Journal'};
  return m[cat]||cat;
}

function renderHomeProducts(){
  const featured = PRODUCTS.slice(0,8);
  document.getElementById('home-products').innerHTML = featured.map(p=>productCard(p)).join('');
}

function renderShopProducts(products){
  const container = document.getElementById('shop-products');
  if(!container) return;
  container.innerHTML = products.length ? products.map(p=>productCard(p)).join('') : `<div style="grid-column:1/-1;text-align:center;padding:60px;color:var(--gray);">No products match your filters.</div>`;
  document.getElementById('shop-count').textContent = `Showing ${products.length} product${products.length!==1?'s':''}`;
}

// ─── FILTERS ──────────────────────────────────────────────────────────
function filterCategory(el, cat){
  activeCat = cat;
  if(el){
    document.querySelectorAll('.cat-chip').forEach(c=>c.classList.remove('active'));
    el.classList.add('active');
  }
}

function applyFilters(){
  let filtered = [...PRODUCTS];
  const catEl = document.querySelector('input[name="cat-filter"]:checked');
  const cat = catEl ? catEl.value : 'all';
  if(cat!=='all') filtered = filtered.filter(p=>p.cat===cat);

  const minEl = document.getElementById('price-min');
  const maxEl = document.getElementById('price-max');
  if(minEl?.value) filtered = filtered.filter(p=>p.price>=parseInt(minEl.value));
  if(maxEl?.value) filtered = filtered.filter(p=>p.price<=parseInt(maxEl.value));

  const sortEl = document.querySelector('.sort-select');
  if(sortEl){
    switch(sortEl.value){
      case 'price-asc': filtered.sort((a,b)=>a.price-b.price); break;
      case 'price-desc': filtered.sort((a,b)=>b.price-a.price); break;
      case 'rating': filtered.sort((a,b)=>b.rating-a.rating); break;
      case 'newest': filtered = filtered.filter(p=>p.badge==='New').concat(filtered.filter(p=>p.badge!=='New')); break;
    }
  }
  renderShopProducts(filtered);
}

function resetFilters(){
  document.querySelectorAll('input[name="cat-filter"]')[0].checked = true;
  document.getElementById('price-min').value='';
  document.getElementById('price-max').value='';
  document.querySelector('.sort-select').value='featured';
  renderShopProducts(PRODUCTS);
}

// ─── PRODUCT DETAIL ───────────────────────────────────────────────────
function openDetail(id){
  const p = PRODUCTS.find(x=>x.id===id);
  if(!p) return;
  currentProduct = p;

  document.getElementById('detail-breadcrumb').innerHTML = `<div class="breadcrumb" style="padding-top:16px;"><span onclick="showPage('home')">Home</span> / <span onclick="showPage('shop')">Shop</span> / <span>${p.name}</span></div>`;
  document.getElementById('detail-cat').textContent = catLabel(p.cat);
  document.getElementById('detail-name').textContent = p.name;
  document.getElementById('detail-stars').textContent = '★★★★★'.slice(0,Math.round(p.rating)) + '☆☆☆☆☆'.slice(0,5-Math.round(p.rating));
  document.getElementById('detail-rating-count').textContent = `${p.rating} · ${p.reviews} reviews`;

  const priceEl = document.getElementById('detail-price');
  priceEl.innerHTML = `₹${p.price}${p.original?`<span class="original">₹${p.original}</span><span class="savings">${Math.round((1-p.price/p.original)*100)}% off</span>`:''}`;

  document.getElementById('detail-desc').textContent = p.desc;

  const mainImg = document.getElementById('detail-main-img');
  mainImg.style.background = p.bg;
  mainImg.innerHTML = `<span style="font-size:100px">${p.emoji}</span>`;

  const thumbs = document.getElementById('detail-thumbs');
  const tBgs = [p.bg,'linear-gradient(135deg,#F0F0F0,#E0E0E0)','linear-gradient(135deg,#FFF,#F5F5F5)','linear-gradient(135deg,#E8E4F4,#D4CCEB)'];
  const tEmojis = [p.emoji,'🖼️','📄','✨'];
  thumbs.innerHTML = tBgs.map((bg,i)=>`<div class="detail-thumb ${i===0?'active':''}" style="background:${bg};" onclick="selectThumb(this,'${bg}','${tEmojis[i]}')">${tEmojis[i]}</div>`).join('');

  document.getElementById('detail-add-cart').onclick = ()=>addToCart(p.id, document.querySelector('.size-chip.active')?.textContent||'A4');

  document.getElementById('detail-reviews-container').innerHTML = REVIEWS_DATA.map(r=>`
    <div class="review-card">
      <div class="review-header"><span class="reviewer-name">${r.name}</span><span class="review-date">${r.date}</span></div>
      <div class="review-stars">${r.stars}</div>
      <div class="review-text">${r.text}</div>
    </div>`).join('');

  showPage('detail');
}

function selectThumb(el, bg, emoji){
  document.querySelectorAll('.detail-thumb').forEach(t=>t.classList.remove('active'));
  el.classList.add('active');
  const main = document.getElementById('detail-main-img');
  main.style.background = bg;
  main.innerHTML = `<span style="font-size:100px">${emoji}</span>`;
}

function selectSize(el){
  document.querySelectorAll('.size-chip').forEach(c=>c.classList.remove('active'));
  el.classList.add('active');
}

function toggleDetailWishlist(el){
  el.classList.toggle('active');
  el.textContent = el.classList.contains('active') ? '❤️' : '🤍';
  showToast(el.classList.contains('active') ? 'Added to wishlist!' : 'Removed from wishlist','success');
}

function toggleWishlist(el){
  el.classList.toggle('active');
  el.textContent = el.classList.contains('active') ? '❤️' : '🤍';
  showToast(el.classList.contains('active') ? 'Saved to wishlist!' : 'Removed from wishlist','success');
}

// ─── CART ──────────────────────────────────────────────────────────────
function addToCart(id, size){
  const p = PRODUCTS.find(x=>x.id===id);
  if(!p) return;
  const existing = cart.find(i=>i.id===id && i.size===size);
  if(existing){ existing.qty++; }
  else { cart.push({id, size:size||'A4', qty:1}); }
  saveCart();
  updateCartUI();
  showToast(`${p.name} added to cart! 🛒`, 'success');
}

function removeFromCart(id, size){
  cart = cart.filter(i=>!(i.id===id && i.size===size));
  saveCart(); updateCartUI(); renderCartItems();
}

function changeQty(id, size, delta){
  const item = cart.find(i=>i.id===id && i.size===size);
  if(!item) return;
  item.qty = Math.max(0, item.qty+delta);
  if(item.qty===0) removeFromCart(id, size);
  else { saveCart(); updateCartUI(); renderCartItems(); }
}

function saveCart(){ localStorage.setItem('sd_cart', JSON.stringify(cart)); }

function updateCartUI(){
  const total = cart.reduce((s,i)=>s+i.qty,0);
  const badge = document.getElementById('cart-badge');
  badge.textContent = total;
  badge.classList.toggle('show', total>0);
}

function openCart(){
  document.getElementById('cart-overlay').classList.add('open');
  document.getElementById('cart-drawer').classList.add('open');
  renderCartItems();
}

function closeCart(){
  document.getElementById('cart-overlay').classList.remove('open');
  document.getElementById('cart-drawer').classList.remove('open');
}

function renderCartItems(){
  const container = document.getElementById('cart-items-container');
  const footer = document.getElementById('cart-footer');

  if(cart.length===0){
    container.innerHTML=`<div class="cart-empty"><span class="cart-empty-icon">🛒</span><div class="cart-empty-title">Your cart is empty</div><div class="cart-empty-sub">Discover beautiful digital downloads and fill it up!</div><button class="btn-primary" onclick="closeCart();showPage('shop')">Browse Products</button></div>`;
    footer.style.display='none'; return;
  }

  let subtotal = 0;
  container.innerHTML = cart.map(item=>{
    const p = PRODUCTS.find(x=>x.id===item.id);
    if(!p) return '';
    subtotal += p.price * item.qty;
    return `<div class="cart-item">
      <div class="cart-item-img" style="background:${p.bg}">${p.emoji}</div>
      <div class="cart-item-info">
        <div class="cart-item-name">${p.name}</div>
        <div class="cart-item-size">Size: ${item.size} · PDF</div>
        <div class="cart-item-row">
          <div class="cart-item-price">₹${p.price * item.qty}</div>
          <div class="qty-control">
            <button class="qty-btn" onclick="changeQty(${item.id},'${item.size}',-1)">−</button>
            <span class="qty-num">${item.qty}</span>
            <button class="qty-btn" onclick="changeQty(${item.id},'${item.size}',1)">+</button>
            <button class="cart-remove" onclick="removeFromCart(${item.id},'${item.size}')">🗑</button>
          </div>
        </div>
      </div>
    </div>`;
  }).join('');

  const discounted = Math.round(subtotal * (currentDiscount/100));
  const total = subtotal - discounted;
  document.getElementById('cart-subtotal').textContent = `₹${subtotal}`;
  document.getElementById('cart-discount').textContent = `-₹${discounted}`;
  document.getElementById('discount-row').style.display = discounted>0 ? 'flex' : 'none';
  document.getElementById('cart-total').textContent = `₹${total}`;
  footer.style.display='block';
}

function applyPromo(){
  const code = document.getElementById('promo-input').value.trim().toUpperCase();
  const codes = {'SREE10':10,'WELCOME20':20,'CREATIVE15':15};
  if(codes[code]){
    currentDiscount = codes[code];
    showToast(`Promo applied! ${codes[code]}% off 🎉`,'success');
    renderCartItems();
  } else {
    showToast('Invalid promo code. Try SREE10','error');
  }
}

function goToCheckout(){
  if(!currentUser){ closeCart(); openAuth('login'); return; }
  closeCart();
  renderCheckoutItems();
  showPage('checkout');
}

// ─── CHECKOUT ──────────────────────────────────────────────────────────
function renderCheckoutItems(){
  let subtotal = 0;
  const container = document.getElementById('checkout-items');
  container.innerHTML = cart.map(item=>{
    const p = PRODUCTS.find(x=>x.id===item.id);
    if(!p) return '';
    subtotal += p.price * item.qty;
    return `<div class="checkout-item">
      <div class="checkout-item-img" style="background:${p.bg}">${p.emoji}</div>
      <div style="flex:1;">
        <div class="checkout-item-name">${p.name}</div>
        <div class="checkout-item-size">Size: ${item.size} · Qty: ${item.qty}</div>
      </div>
      <div class="checkout-item-price">₹${p.price * item.qty}</div>
    </div>`;
  }).join('');

  const discounted = Math.round(subtotal*(currentDiscount/100));
  const total = subtotal - discounted;
  document.getElementById('co-subtotal').textContent = `₹${subtotal}`;
  document.getElementById('co-discount').textContent = `-₹${discounted}`;
  document.getElementById('co-total').textContent = `₹${total}`;
}

function selectPayment(el){
  document.querySelectorAll('.payment-method').forEach(m=>m.classList.remove('selected'));
  el.classList.add('selected');
  el.querySelector('input[type=radio]').checked = true;
  const isCard = el.querySelector('.payment-method-name').textContent.includes('Card');
  document.getElementById('card-fields').style.display = isCard ? 'block' : 'none';
}

function applyCoupon(){
  const code = document.getElementById('co-coupon').value.trim().toUpperCase();
  const codes = {'SREE10':10,'WELCOME20':20,'CREATIVE15':15};
  const msgEl = document.getElementById('coupon-msg');
  if(codes[code]){
    currentDiscount = codes[code];
    msgEl.style.display='block'; msgEl.style.color='var(--sage)';
    msgEl.textContent = `✓ Coupon applied! ${codes[code]}% off`;
    renderCheckoutItems();
  } else {
    msgEl.style.display='block'; msgEl.style.color='var(--terra)';
    msgEl.textContent = '✕ Invalid coupon code.';
  }
}

function formatCard(el){
  let v = el.value.replace(/\D/g,'').substring(0,16);
  el.value = v.replace(/(.{4})/g,'$1 ').trim();
}

function placeOrder(){
  const fname = document.getElementById('co-fname').value.trim();
  const email = document.getElementById('co-email').value.trim();
  if(!fname){ showToast('Please enter your first name','error'); return; }
  if(!email || !email.includes('@')){ showToast('Please enter a valid email','error'); return; }

  const btn = document.querySelector('.btn-place-order');
  btn.textContent = 'Processing payment…';
  btn.disabled = true;

  setTimeout(()=>{
    const orderNum = 'SD-' + Math.floor(100000+Math.random()*900000);
    document.getElementById('success-order-num').textContent = `Order #${orderNum}`;
    document.getElementById('order-success-overlay').classList.add('show');
    cart = []; saveCart(); updateCartUI();
    currentDiscount = 0;
    btn.textContent = 'Place Order & Pay'; btn.disabled = false;
  }, 2200);
}

function closeOrderSuccess(){
  document.getElementById('order-success-overlay').classList.remove('show');
  showPage('home');
}

// ─── AUTH ──────────────────────────────────────────────────────────────
function openAuth(tab){
  document.getElementById('auth-modal').classList.add('open');
  renderAuthForm(tab);
  const tabs = document.querySelectorAll('.modal-tab');
  tabs[0].classList.toggle('active', tab==='login');
  tabs[1].classList.toggle('active', tab==='signup');
}

function closeAuth(){ document.getElementById('auth-modal').classList.remove('open'); }

function switchAuthTab(tab, el){
  document.querySelectorAll('.modal-tab').forEach(t=>t.classList.remove('active'));
  el.classList.add('active');
  renderAuthForm(tab);
}

function renderAuthForm(tab){
  const c = document.getElementById('auth-form-container');
  const titleEl = document.getElementById('auth-modal-title');
  const subEl = document.getElementById('auth-modal-sub');
  if(tab==='login'){
    titleEl.textContent='Welcome back';
    subEl.textContent='Log in to access your downloads';
    c.innerHTML=`
      <div class="form-group"><label class="form-label">Email</label><input class="form-input" id="login-email" type="email" placeholder="hello@example.com"></div>
      <div class="form-group"><label class="form-label">Password</label><input class="form-input" id="login-pw" type="password" placeholder="Your password"></div>
      <button class="btn-submit" onclick="doLogin()">Log In</button>
      <div class="form-divider">or</div>
      <button class="oauth-btn" onclick="doOAuth()">🔵 Continue with Google</button>
      <p style="text-align:center;margin-top:16px;font-size:13px;color:var(--gray);">Forgot password? <a style="color:var(--terra);cursor:pointer;">Reset it</a></p>`;
  } else {
    titleEl.textContent='Create an account';
    subEl.textContent='Join thousands of creative souls';
    c.innerHTML=`
      <div class="form-row">
        <div class="form-group"><label class="form-label">First Name</label><input class="form-input" id="su-fname" placeholder="Sree"></div>
        <div class="form-group"><label class="form-label">Last Name</label><input class="form-input" id="su-lname" placeholder="Lakshmi"></div>
      </div>
      <div class="form-group"><label class="form-label">Email</label><input class="form-input" id="su-email" type="email" placeholder="hello@example.com"></div>
      <div class="form-group"><label class="form-label">Password</label><input class="form-input" id="su-pw" type="password" placeholder="Min 8 characters"></div>
      <div class="form-group" style="display:flex;align-items:center;gap:8px;font-size:13px;color:var(--gray);"><input type="checkbox" id="terms-check" style="accent-color:var(--terra);"> I agree to the Terms of Service & Privacy Policy</div>
      <button class="btn-submit" onclick="doSignup()">Create Account</button>
      <div class="form-divider">or</div>
      <button class="oauth-btn" onclick="doOAuth()">🔵 Continue with Google</button>`;
  }
}

function doLogin(){
  const email = document.getElementById('login-email')?.value.trim();
  const pw = document.getElementById('login-pw')?.value;
  if(!email || !email.includes('@')){ showToast('Enter a valid email','error'); return; }
  if(!pw || pw.length<4){ showToast('Enter your password','error'); return; }
  const user = {name: email.split('@')[0], email, initial: email[0].toUpperCase()};
  loginSuccess(user);
}

function doSignup(){
  const fname = document.getElementById('su-fname')?.value.trim();
  const email = document.getElementById('su-email')?.value.trim();
  const pw = document.getElementById('su-pw')?.value;
  const terms = document.getElementById('terms-check')?.checked;
  if(!fname){ showToast('Enter your first name','error'); return; }
  if(!email || !email.includes('@')){ showToast('Enter a valid email','error'); return; }
  if(!pw || pw.length<8){ showToast('Password must be at least 8 characters','error'); return; }
  if(!terms){ showToast('Please accept the Terms of Service','error'); return; }
  const user = {name:fname, email, initial:fname[0].toUpperCase()};
  loginSuccess(user);
}

function doOAuth(){
  const user = {name:'Sree', email:'sree@example.com', initial:'S'};
  loginSuccess(user);
}

function loginSuccess(user){
  currentUser = user;
  localStorage.setItem('sd_user', JSON.stringify(user));
  showUserUI();
  closeAuth();
  showToast(`Welcome, ${user.name}! 🎉`,'success');
}

function showUserUI(){
  document.getElementById('auth-area').style.display='none';
  document.getElementById('user-area').style.display='flex';
  document.getElementById('user-avatar-btn').textContent = currentUser.initial;
}

function logout(){
  currentUser = null;
  localStorage.removeItem('sd_user');
  document.getElementById('auth-area').style.display='flex';
  document.getElementById('user-area').style.display='none';
  document.getElementById('user-dropdown').classList.remove('open');
  showToast('Logged out. See you soon!','success');
}

function toggleUserMenu(){
  document.getElementById('user-dropdown').classList.toggle('open');
}

// ─── MISC ─────────────────────────────────────────────────────────────
function toggleMobileNav(){
  document.getElementById('mobile-nav').classList.toggle('open');
}

let toastTimer;
function showToast(msg, type='success'){
  const el = document.getElementById('toast');
  el.textContent = msg;
  el.className = `toast ${type} show`;
  clearTimeout(toastTimer);
  toastTimer = setTimeout(()=>el.classList.remove('show'), 3000);
}

function sendMessage(){
  showToast("Message sent! We'll reply within 24 hours. 📧",'success');
}

// Close modals on overlay click
document.getElementById('auth-modal').addEventListener('click', function(e){
  if(e.target===this) closeAuth();
});
</script>
</body>
</html>
