# DESIGN.MD — Design System EasySN AI

## Palette de Couleurs

### Couleurs principales
```css
/* Primary (Orange énergique) */
--color-primary: #F59E0B;          /* Base orange */
--color-primary-hover: #D97706;     /* Hover plus foncé */
--color-primary-muted: #FEF3C7;     /* Version très claire pour backgrounds */

/* Secondary (Neutres chauds) */
--color-secondary: #78716C;         /* Gris chaud */
--color-secondary-hover: #57534E;   /* Hover plus foncé */

/* Accent & Glow */
--color-accent: #F59E0B;            /* Identique à primary pour cohérence */
--color-accent-hover: #FBBF24;      /* Version plus claire pour glow */
--color-accent-muted: #FEF3C7;      /* Pour overlays subtils */

/* Backgrounds (approche layered) */
--color-background: #FAFAFA;        /* Background principal */
--color-surface: #FFFFFF;           /* Cards, modales */
--color-surface-elevated: #FFFFFF;  /* Éléments flottants (même que surface pour simplicité) */

/* Texte (hiérarchie claire) */
--color-text-primary: #1F2937;      /* Titres, texte important */
--color-text-secondary: #4B5563;    /* Sous-titres, texte body */
--color-text-muted: #9CA3AF;        /* Texte secondaire, captions */
--color-text-ghost: #D1D5DB;        /* Placeholders, éléments désactivés */

/* Bordures */
--color-border-primary: #E5E7EB;    /* Bordures principales */
--color-border-subtle: #F3F4F6;     /* Bordures très subtiles */

/* États */
--color-success: #10B981;           /* Validations, succès */
--color-error: #EF4444;             /* Erreurs, alertes */
--color-warning: #F59E0B;           /* Warnings (utilise notre orange) */
```

### Couleurs en HSL (pour manipulations dynamiques)
```css
--color-primary-hsl: 38, 92%, 50%;
--color-accent-hsl: 38, 92%, 50%;
--color-background-hsl: 0, 0%, 98%;
--color-surface-hsl: 0, 0%, 100%;
--color-text-primary-hsl: 215, 25%, 27%;
```

## Typographie Premium

### Font Families
```css
/* Heading & Body (cohérence avec Outfit) */
--font-heading: 'Outfit', -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, 'Helvetica Neue', Arial, sans-serif;
--font-body: 'Outfit', -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, 'Helvetica Neue', Arial, sans-serif;
--font-mono: 'SF Mono', Monaco, 'Inconsolata', 'Roboto Mono', 'Source Code Pro', Consolas, monospace;
```

### Échelle Typographique

#### Desktop
```css
/* Display (Hero titles) */
--text-display: 4rem;           /* 64px */
--text-display-weight: 700;
--text-display-height: 1.1;     /* 70.4px */
--text-display-spacing: -0.02em;
--text-display-transform: none;

/* Headings */
--text-h1: 3rem;               /* 48px */
--text-h1-weight: 600;
--text-h1-height: 1.2;         /* 57.6px */
--text-h1-spacing: -0.01em;

--text-h2: 2.25rem;            /* 36px */
--text-h2-weight: 600;
--text-h2-height: 1.3;         /* 46.8px */
--text-h2-spacing: -0.01em;

--text-h3: 1.875rem;           /* 30px */
--text-h3-weight: 500;
--text-h3-height: 1.4;         /* 42px */

--text-h4: 1.5rem;             /* 24px */
--text-h4-weight: 500;
--text-h4-height: 1.4;         /* 33.6px */

/* Body */
--text-body-lg: 1.125rem;      /* 18px */
--text-body-lg-weight: 400;
--text-body-lg-height: 1.6;    /* 28.8px */

--text-body: 1rem;             /* 16px */
--text-body-weight: 400;
--text-body-height: 1.6;       /* 25.6px */

--text-body-sm: 0.875rem;      /* 14px */
--text-body-sm-weight: 400;
--text-body-sm-height: 1.5;    /* 21px */

--text-caption: 0.75rem;       /* 12px */
--text-caption-weight: 500;
--text-caption-height: 1.4;    /* 16.8px */
```

#### Mobile
```css
/* Display (réduit pour mobile) */
--text-display-mobile: 2.5rem;  /* 40px */
--text-h1-mobile: 2rem;         /* 32px */
--text-h2-mobile: 1.75rem;      /* 28px */
--text-h3-mobile: 1.5rem;       /* 24px */
--text-h4-mobile: 1.25rem;      /* 20px */
```

### Styles Spéciaux
```css
/* Gradient text pour les titres hero */
.gradient-text {
  background: linear-gradient(135deg, #F59E0B 0%, #FBBF24 50%, #F97316 100%);
  background-clip: text;
  -webkit-background-clip: text;
  -webkit-text-fill-color: transparent;
  background-size: 200% 200%;
  animation: gradient-shift 3s ease-in-out infinite alternate;
}

/* Text glow pour les CTA */
.text-glow {
  text-shadow: 0 0 20px rgba(245, 158, 11, 0.3);
}

/* Text balance pour meilleure lisibilité */
.text-balance {
  text-wrap: balance;
}
```

## Spacing & Layout

### Tokens de spacing
```css
--space-1: 0.25rem;    /* 4px */
--space-2: 0.5rem;     /* 8px */
--space-3: 0.75rem;    /* 12px */
--space-4: 1rem;       /* 16px */
--space-5: 1.25rem;    /* 20px */
--space-6: 1.5rem;     /* 24px */
--space-8: 2rem;       /* 32px */
--space-12: 3rem;      /* 48px */
--space-16: 4rem;      /* 64px */
--space-20: 5rem;      /* 80px */
--space-24: 6rem;      /* 96px */
--space-32: 8rem;      /* 128px */
```

### Section Padding
```css
/* Desktop */
--section-padding-y: var(--space-24);      /* 96px vertical */
--section-padding-y-lg: var(--space-32);   /* 128px pour hero */
--section-padding-x: var(--space-6);       /* 24px horizontal */

/* Mobile */
--section-padding-y-mobile: var(--space-16);    /* 64px */
--section-padding-y-lg-mobile: var(--space-20); /* 80px pour hero */
```

### Max Widths
```css
--max-width-prose: 42.5rem;    /* 680px - texte lecture */
--max-width-content: 67.5rem;  /* 1080px - contenu principal */
--max-width-wide: 80rem;       /* 1280px - sections larges */
--max-width-full: 100%;        /* pleine largeur */
```

### Grid System
```css
--grid-cols: 12;
--grid-gap: 1.5rem;           /* 24px desktop */
--grid-gap-mobile: 1rem;      /* 16px mobile */
```

## Ombres Multicouches

```css
/* Niveaux d'élévation progressifs */
--shadow-xs: 
  0 1px 2px rgba(0, 0, 0, 0.05);

--shadow-sm: 
  0 1px 3px rgba(0, 0, 0, 0.08),
  0 1px 2px rgba(0, 0, 0, 0.12);

--shadow-md: 
  0 4px 6px rgba(0, 0, 0, 0.07),
  0 2px 4px rgba(0, 0, 0, 0.06),
  0 12px 20px rgba(0, 0, 0, 0.04);

--shadow-lg: 
  0 8px 30px rgba(0, 0, 0, 0.12),
  0 4px 10px rgba(0, 0, 0, 0.08),
  0 20px 40px rgba(0, 0, 0, 0.06);

/* Glow avec couleur accent */
--shadow-glow: 
  0 0 30px rgba(245, 158, 11, 0.15),
  0 0 60px rgba(245, 158, 11, 0.08),
  0 4px 20px rgba(0, 0, 0, 0.1);

/* Glow intense pour CTA */
--shadow-glow-intense: 
  0 0 40px rgba(245, 158, 11, 0.25),
  0 0 80px rgba(245, 158, 11, 0.12),
  0 8px 32px rgba(0, 0, 0, 0.15);
```

## Border Radius

```css
--radius-none: 0;
--radius-xs: 0.25rem;      /* 4px */
--radius-sm: 0.5rem;       /* 8px */
--radius-md: 0.75rem;      /* 12px */
--radius-lg: 1rem;         /* 16px */
--radius-xl: 1.5rem;       /* 24px */
--radius-full: 9999px;     /* cercle parfait */
```

## Gradients Nommés

```css
/* Hero gradient - complexe et dynamique */
--gradient-hero: 
  linear-gradient(135deg, 
    #FAFAFA 0%, 
    #FEF3C7 15%, 
    #FAFAFA 35%, 
    #FEF3C7 55%, 
    #FAFAFA 75%, 
    #FEF3C7 100%
  );

/* Accent gradient pour boutons */
--gradient-accent: 
  linear-gradient(135deg, #F59E0B 0%, #FBBF24 100%);

/* Surface gradient - profondeur subtile */
--gradient-surface: 
  linear-gradient(to bottom, 
    rgba(255, 255, 255, 0.08) 0%, 
    rgba(255, 255, 255, 0) 100%
  );

/* Glow gradient - halo lumineux */
--gradient-glow: 
  radial-gradient(circle at 50% 50%, 
    rgba(245, 158, 11, 0.1) 0%, 
    rgba(245, 158, 11, 0.05) 50%, 
    transparent 100%
  );

/* Text gradient pour titres */
--gradient-text: 
  linear-gradient(135deg, 
    #F59E0B 0%, 
    #FBBF24 50%, 
    #F97316 100%
  );

/* Border gradient animé */
--gradient-border: 
  conic-gradient(from 0deg, 
    #F59E0B, 
    #FBBF24, 
    #F97316, 
    #F59E0B
  );
```

## Effets Visuels Avancés

### Glassmorphism (cards flottantes)
```css
.glass {
  backdrop-filter: blur(16px);
  -webkit-backdrop-filter: blur(16px);
  background: rgba(255, 255, 255, 0.8);
  border: 1px solid rgba(255, 255, 255, 0.2);
  box-shadow: var(--shadow-lg);
}
```

### Texture grain/noise
```css
.grain-texture {
  background-image: url("data:image/svg+xml,%3Csvg viewBox='0 0 256 256' xmlns='http://www.w3.org/2000/svg'%3E%3Cfilter id='noiseFilter'%3E%3CfeTurbulence type='fractalNoise' baseFrequency='0.9' numOctaves='4' stitchTiles='stitch'/%3E%3C/filter%3E%3Crect width='100%25' height='100%25' filter='url(%23noiseFilter)' opacity='0.03'/%3E%3C/svg%3E");
  background-repeat: repeat;
}
```

### Glow orbs (fond hero/CTA)
```css
.glow-orb-1 {
  position: absolute;
  width: 400px;
  height: 400px;
  background: var(--gradient-glow);
  border-radius: 50%;
  filter: blur(80px);
  top: -200px;
  left: -200px;
  z-index: -1;
  opacity: 0.6;
}

.glow-orb-2 {
  position: absolute;
  width: 300px;
  height: 300px;
  background: radial-gradient(circle, rgba(251, 191, 36, 0.15) 0%, transparent 70%);
  border-radius: 50%;
  filter: blur(60px);
  bottom: -150px;
  right: -150px;
  z-index: -1;
  opacity: 0.4;
}
```

### Dividers entre sections
```css
.section-divider {
  width: 100%;
  height: 1px;
  background: linear-gradient(90deg, 
    transparent 0%, 
    var(--color-border-primary) 20%, 
    var(--color-primary) 50%, 
    var(--color-border-primary) 80%, 
    transparent 100%
  );
  margin: var(--space-16) 0;
}
```

### Image treatments
```css
.image-treatment {
  border-radius: var(--radius-lg);
  box-shadow: var(--shadow-md);
  transition: transform 0.3s ease, box-shadow 0.3s ease;
  overflow: hidden;
}

.image-treatment:hover {
  transform: scale(1.02);
  box-shadow: var(--shadow-lg);
}

.image-overlay {
  position: relative;
}

.image-overlay::after {
  content: '';
  position: absolute;
  top: 0;
  left: 0;
  right: 0;
  bottom: 0;
  background: linear-gradient(45deg, 
    rgba(245, 158, 11, 0.1) 0%, 
    transparent 50%
  );
  transition: opacity 0.3s ease;
  opacity: 0;
}

.image-overlay:hover::after {
  opacity: 1;
}
```

## Composants Documentés

### Boutons
```css
/* Primary Button */
.btn-primary {
  background: var(--gradient-accent);
  color: white;
  padding: 0.875rem 2rem;
  border-radius: var(--radius-lg);
  font-weight: 500;
  font-size: var(--text-body);
  border: none;
  cursor: pointer;
  transition: all 0.2s ease;
  box-shadow: var(--shadow-sm);
  position: relative;
  overflow: hidden;
}

.btn-primary:hover {
  transform: scale(1.02);
  box-shadow: var(--shadow-glow);
}

.btn-primary:active {
  transform: scale(0.98);
}

.btn-primary:disabled {
  opacity: 0.6;
  cursor: not-allowed;
  transform: none;
}

.btn-primary:focus-visible {
  outline: none;
  box-shadow: var(--shadow-glow), 0 0 0 3px rgba(245, 158, 11, 0.3);
}

/* Secondary Button */
.btn-secondary {
  background: var(--color-surface);
  color: var(--color-text-primary);
  border: 1px solid var(--color-border-primary);
  padding: 0.875rem 2rem;
  border-radius: var(--radius-lg);
  font-weight: 500;
  transition: all 0.2s ease;
}

.btn-secondary:hover {
  border-color: var(--color-primary);
  background: var(--color-primary-muted);
  transform: scale(1.02);
}

/* Outline Button */
.btn-outline {
  background: transparent;
  color: var(--color-primary);
  border: 2px solid var(--color-primary);
  padding: 0.75rem 2rem;
  border-radius: var(--radius-lg);
  font-weight: 500;
  transition: all 0.2s ease;
}

.btn-outline:hover {
  background: var(--color-primary);
  color: white;
  transform: scale(1.02);
}

/* Ghost Button */
.btn-ghost {
  background: transparent;
  color: var(--color-text-secondary);
  border: none;
  padding: 0.875rem 2rem;
  border-radius: var(--radius-lg);
  font-weight: 500;
  transition: all 0.2s ease;
}

.btn-ghost:hover {
  background: var(--color-primary-muted);
  color: var(--color-primary);
}
```

### Cards
```css
.card {
  background: var(--color-surface);
  border: 1px solid var(--color-border-subtle);
  border-radius: var(--radius-xl);
  padding: var(--space-8);
  box-shadow: var(--shadow-sm);
  transition: all 0.3s ease;
  position: relative;
  overflow: hidden;
}

.card::before {
  content: '';
  position: absolute;
  top: 0;
  left: 0;
  right: 0;
  height: 1px;
  background: var(--gradient-surface);
  opacity: 0;
  transition: opacity 0.3s ease;
}

.card:hover {
  transform: translateY(-4px);
  box-shadow: var(--shadow-md);
  border-color: var(--color-primary);
}

.card:hover::before {
  opacity: 1;
}

/* Card élevée */
.card-elevated {
  box-shadow: var(--shadow-md);
  background: var(--color-surface);
}

.card-elevated:hover {
  box-shadow: var(--shadow-lg);
  transform: translateY(-6px);
}
```

### Badges/Pills
```css
.badge {
  display: inline-flex;
  align-items: center;
  padding: 0.375rem 0.875rem;
  background: var(--color-primary-muted);
  color: var(--color-primary);
  border-radius: var(--radius-full);
  font-size: var(--text-body-sm);
  font-weight: 500;
  border: 1px solid rgba(245, 158, 11, 0.2);
}

.badge-success {
  background: rgba(16, 185, 129, 0.1);
  color: var(--color-success);
  border-color: rgba(16, 185, 129, 0.2);
}

.badge-outline {
  background: transparent;
  border: 1px solid var(--color-primary);
  color: var(--color-primary);
}
```

### Inputs
```css
.input {
  width: 100%;
  padding: 0.875rem 1rem;
  border: 1px solid var(--color-border-primary);
  border-radius: var(--radius-md);
  font-size: var(--text-body);
  background: var(--color-surface);
  color: var(--color-text-primary);
  transition: all 0.2s ease;
}

.input::placeholder {
  color: var(--color-text-muted);
}

.input:focus {
  outline: none;
  border-color: var(--color-primary);
  box-shadow: 0 0 0 3px rgba(245, 158, 11, 0.1);
}

.input:hover {
  border-color: var(--color-text-secondary);
}
```

### Navigation
```css
.nav {
  position: sticky;
  top: 0;
  z-index: 50;
  background: rgba(255, 255, 255, 0.9);
  backdrop-filter: blur(16px);
  -webkit-backdrop-filter: blur(16px);
  border-bottom: 1px solid var(--color-border-subtle);
  transition: all 0.3s ease;
}

.nav-scrolled {
  background: rgba(255, 255, 255, 0.95);
  border-bottom-color: var(--color-border-primary);
  box-shadow: var(--shadow-sm);
}
```

## Animations & Micro-interactions

### Scroll Reveal
```css
.scroll-reveal {
  opacity: 0;
  transform: translateY(30px);
  filter: blur(8px);
  transition: all 0.8s cubic-bezier(0.16, 1, 0.3, 1);
}

.scroll-reveal.visible {
  opacity: 1;
  transform: translateY(0);
  filter: blur(0);
}

/* Stagger effect */
.scroll-reveal-stagger > * {
  transition-delay: calc(var(--stagger-delay, 0) * 0.1s);
}
```

### Hover Cards Animation
```css
@keyframes card-float {
  0%, 100% { transform: translateY(-4px); }
  50% { transform: translateY(-8px); }
}

.card-hover:hover {
  animation: card-float 2s ease-in-out infinite;
}
```

### Boutons Hover
```css
.btn-hover-effect {
  position: relative;
  overflow: hidden;
}

.btn-hover-effect::before {
  content: '';
  position: absolute;
  top: 0;
  left: -100%;
  width: 100%;
  height: 100%;
  background: linear-gradient(90deg, 
    transparent 0%, 
    rgba(255, 255, 255, 0.2) 50%, 
    transparent 100%
  );
  transition: left 0.5s ease;
}

.btn-hover-effect:hover::before {
  left: 100%;
}
```

### Compteurs Animés
```css
@keyframes count-up {
  from { opacity: 0; transform: translateY(20px); }
  to { opacity: 1; transform: translateY(0); }
}

.counter {
  animation: count-up 0.6s ease-out;
}
```

### Marquee pour logos
```css
@keyframes marquee {
  0% { transform: translateX(0); }
  100% { transform: translateX(-50%); }
}

.marquee {
  display: flex;
  animation: marquee 30s linear infinite;
}

.marquee:hover {
  animation-play-state: paused;
}
```

### Page Load Animation
```css
@keyframes page-fade-in {
  from { 
    opacity: 0; 
    transform: translateY(20px); 
  }
  to { 
    opacity: 1; 
    transform: translateY(0); 
  }
}

.page-container {
  animation: page-fade-in 0.8s ease-out;
}

.hero-stagger > * {
  opacity: 0;
  animation: page-fade-in 0.8s ease-out forwards;
}

.hero-stagger > *:nth-child(1) { animation-delay: 0.1s; }
.hero-stagger > *:nth-child(2) { animation-delay: 0.2s; }
.hero-stagger > *:nth-child(3) { animation-delay: 0.3s; }
.hero-stagger > *:nth-child(4) { animation-delay: 0.4s; }
```

## Responsive Breakpoints

### Breakpoints
```css
/* Mobile First Approach */
@media (min-width: 640px) { /* tablet */ }
@media (min-width: 1024px) { /* desktop */ }
@media (min-width: 1280px) { /* large desktop */ }
```

### Adaptations Concrètes

#### Navigation
```css
/* Mobile: burger menu */
@media (max-width: 639px) {
  .nav-menu { 
    display: none; 
  }
  .nav-burger { 
    display: block; 
  }
}

/* Desktop: menu horizontal */
@media (min-width: 640px) {
  .nav-menu { 
    display: flex; 
  }
  .nav-burger { 
    display: none; 
  }
}
```

#### Grille
```css
/* Mobile: 1 colonne */
.grid-responsive {
  display: grid;
  grid-template-columns: 1fr;
  gap: var(--grid-gap-mobile);
}

/* Tablet: 2 colonnes */
@media (min-width: 640px) {
  .grid-responsive {
    grid-template-columns: repeat(2, 1fr);
    gap: var(--grid-gap);
  }
}

/* Desktop: grille complète */
@media (min-width: 1024px) {
  .grid-responsive {
    grid-template-columns: repeat(var(--grid-cols), 1fr);
  }
}
```

#### Typographie responsive
```css
.responsive-text {
  font-size: var(--text-h1-mobile);
  line-height: 1.2;
}

@media (min-width: 640px) {
  .responsive-text {
    font-size: var(--text-h1);
    line-height: 1.1;
  }
}
```

#### Padding sections responsive
```css
.section {
  padding: var(--section-padding-y-mobile) var(--section-padding-x);
}

@media (min-width: 640px) {
  .section {
    padding: var(--section-padding-y) var(--section-padding-x);
  }
}

.section-hero {
  padding: var(--section-padding-y-lg-mobile) var(--section-padding-x);
}

@media (min-width: 640px) {
  .section-hero {
    padding: var(--section-padding-y-lg) var(--section-padding-x);
  }
}
```