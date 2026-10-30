<script setup>
import dividers from '@/assets/figma/divisores.svg'

const experiences = [
  {
    title: '1985 – Presente | The Pinheads',
    role: 'Guitarrista Principal',
    description: `Composição e performance de Rock 'n' Roll. Responsável pela audição da "Batalha das Bandas" (mesmo sendo considerado "barulhento demais" por alguns juízes).`,
  },
  {
    title: '1955 – Baile Encanto sob o Mar',
    role: 'Músico Substituto (Guitarra)',
    description:
      'Substituição emergencial do guitarrista Marvin Berry. Responsável pela introdução cultural do gênero Heavy Metal trinta anos antes do previsto.',
  },
  {
    title: '1885 – Consultoria de Segurança Hill Valley (Velho Oeste)',
    role: 'Assistente de Ferreiro',
    description:
      'Auxílio técnico em engenharia ferroviária improvisada e mediação de conflitos com a gangue de Buford "Cachorro Louco" Tannen.',
  },
  {
    title: '1985 – Indústrias Biffco',
    role: 'Sobrevivente Urbano',
    description:
      'Gestão de crises em ambientes distópicos e recuperação de artefatos\nesportivos (almanaques) para restauração da ordem cronológica.',
  },
]

const education = [
  {
    title: '1986 | Hill Valley High School',
    role: 'Ensino Médio Completo',
    description: 'Foco em Artes e Música',
  },
  {
    title: '1955 | Cultural Hill Valley',
    role: 'Intercâmbio',
    description:
      'Estudos intensivos sobre dinâmicas sociais da década de 50 e etiqueta de lanchonetes.',
  },
  {
    title: '1985 | Engenharia Aplicada',
    role: 'Workshop',
    description:
      'Treinamento prático em sistemas de 1.21 Gigawatts e mecânica de DeLorean (sob mentoria do Dr. Emmett Brown).',
  },
  {
    title: '2015 | Mobilidade Urbana Futurista',
    role: 'Treinamento',
    description:
      'Curso intensivo de pilotagem de Hoverboard em superfícies sólidas (atenção: pranchas não funcionam na água sem potência extra).',
  },
]
</script>

<template>
  <div class="resume">
    <header class="resume-header">
      <div class="monogram" aria-hidden="true">MM</div>
      <div class="identity">
        <h1>Marty McFly</h1>
        <p>Consultor de Cronologia e Especialista em Performance Musical</p>
      </div>
    </header>

    <div class="resume-body">
      <img
        class="design-dividers"
        :src="dividers"
        alt=""
        width="1332"
        height="1260"
        aria-hidden="true"
      />
      <main class="career">
        <p class="biography">
          Jovem dinâmico, pontual (quando o capacitor de fluxo permite) e com vasta experiência em
          resolução de paradoxos temporais. Guitarrista talentoso com domínio de técnicas avançadas
          de shredding antes mesmo de serem inventadas. Experiente em lidar com figuras históricas,
          direção defensiva de veículos modificados e skate urbano. Nota: Não me chame de frangote.
        </p>
        <section class="experience" aria-labelledby="experience-title">
          <h2 id="experience-title" class="section-title">Experiências Profissionais</h2>
          <article v-for="item in experiences" :key="item.title" class="resume-entry">
            <h3>{{ item.title }}</h3>
            <p class="entry-role">{{ item.role }}</p>
            <p class="entry-description">{{ item.description }}</p>
          </article>
        </section>
      </main>

      <aside class="sidebar" aria-label="Educação e contato">
        <section class="education" aria-labelledby="education-title">
          <h2 id="education-title" class="section-title">Educação</h2>
          <article v-for="item in education" :key="item.title" class="resume-entry">
            <h3>{{ item.title }}</h3>
            <p class="entry-role">{{ item.role }}</p>
            <p>{{ item.description }}</p>
          </article>
        </section>
        <section class="contact" aria-labelledby="contact-title">
          <h2 id="contact-title" class="section-title">Contato</h2>
          <address>
            <p><strong>Endereço:</strong> Lyon Estates, Hill Valley, CA.</p>
            <p>
              <strong>E-mail:</strong>
              <a href="mailto:contato@delorean.com">contato@delorean.com</a>
            </p>
            <p><strong>Telefone:</strong> <a href="tel:+558899990000">+55 (88) 9999 0000</a></p>
          </address>
        </section>
      </aside>
      <footer class="resume-footer">Copyright 2026 - todos os direitos reservados</footer>
    </div>
  </div>
</template>
