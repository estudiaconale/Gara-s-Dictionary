import React, { useState, useEffect, useMemo, useRef } from 'react';
import { 
  BookOpen, 
  Search, 
  Grid, 
  Volume2, 
  Settings, 
  Award, 
  Upload, 
  Check, 
  AlertCircle, 
  ChevronRight, 
  ChevronLeft, 
  RotateCcw, 
  Sliders, 
  HelpCircle,
  Book,
  FileText,
  Play,
  Lightbulb,
  FileUp,
  User,
  Plus,
  Trash2,
  Bookmark,
  CheckCircle,
  Layers
} from 'lucide-react';

// Estilos de fuentes especiales importados dinámicamente
const fontStyles = `
  @import url('https://fonts.googleapis.com/css2?family=Comic+Neue:wght@400;700&family=Lexend:wght@300;400;500;600;700&family=Plus+Jakarta+Sans:wght@300;400;500;600;700;800&display=swap');
  
  .font-lexend { font-family: 'Lexend', sans-serif; }
  .font-comic { font-family: 'Comic Neue', cursive, sans-serif; }
  .font-jakarta { font-family: 'Plus Jakarta Sans', sans-serif; }
`;

// Vocabulario inicial precargado para que la app sea funcional desde el primer segundo
const INITIAL_VOCABULARY = [
  {
    id: "v1",
    word: "Achievement",
    translation: "Logro",
    unit: "Unit 1",
    grammar_type: "Noun",
    pronunciation: "/əˈtʃiːvmənt/",
    example: "Getting a degree is a great achievement for her.",
    tags: ["success", "goals"],
    learned: false,
    letter: "A"
  },
  {
    id: "v2",
    word: "Breathtaking",
    translation: "Asombroso",
    unit: "Unit 1",
    grammar_type: "Adjective",
    pronunciation: "/ˈbreθˌteɪ.kɪŋ/",
    example: "The view from the top of the mountain was breathtaking.",
    tags: ["nature", "beauty"],
    learned: true,
    letter: "B"
  },
  {
    id: "v3",
    word: "Challenge",
    translation: "Desafío",
    unit: "Unit 2",
    grammar_type: "Noun",
    pronunciation: "/ˈtʃæl.ɪndʒ/",
    example: "Learning a new language is always a big challenge.",
    tags: ["difficult", "learning"],
    learned: false,
    letter: "C"
  },
  {
    id: "v4",
    word: "Discover",
    translation: "Descubrir",
    unit: "Unit 2",
    grammar_type: "Verb",
    pronunciation: "/dɪˈskʌv.ər/",
    example: "Scientists want to discover new planets in our galaxy.",
    tags: ["science", "exploration"],
    learned: false,
    letter: "D"
  },
  {
    id: "v5",
    word: "Environment",
    translation: "Medio ambiente",
    unit: "Unit 3",
    grammar_type: "Noun",
    pronunciation: "/ɪnˈvaɪ.rən.mənt/",
    example: "We must take action to protect the natural environment.",
    tags: ["nature", "ecology"],
    learned: true,
    letter: "E"
  },
  {
    id: "v6",
    word: "Flourish",
    translation: "Prosperar",
    unit: "Unit 3",
    grammar_type: "Verb",
    pronunciation: "/ˈflʌr.ɪʃ/",
    example: "These beautiful plants flourish in warm and humid places.",
    tags: ["growth", "nature"],
    learned: false,
    letter: "F"
  },
  {
    id: "v7",
    word: "Gather",
    translation: "Reunirse / Recolectar",
    unit: "Unit 4",
    grammar_type: "Verb",
    pronunciation: "/ˈɡæð.ər/",
    example: "The students gather in the library to work on projects.",
    tags: ["social", "action"],
    learned: false,
    letter: "G"
  },
  {
    id: "v8",
    word: "Harmonious",
    translation: "Armonioso",
    unit: "Unit 4",
    grammar_type: "Adjective",
    pronunciation: "/hɑːˈməʊ.ni.əs/",
    example: "They lived a very quiet and harmonious life in the countryside.",
    tags: ["peace", "relationships"],
    learned: false,
    letter: "H"
  },
  {
    id: "v9",
    word: "Improve",
    translation: "Mejorar",
    unit: "Unit 1",
    grammar_type: "Verb",
    pronunciation: "/ɪmˈpruːv/",
    example: "You can improve your English vocabulary by practicing daily.",
    tags: ["skills", "learning"],
    learned: true,
    letter: "I"
  },
  {
    id: "v10",
    word: "Jeopardize",
    translation: "Poner en peligro",
    unit: "Unit 3",
    grammar_type: "Verb",
    pronunciation: "/ˈdʒep.ə.daɪz/",
    example: "Pollution can jeopardize the survival of marine animals.",
    tags: ["danger", "ecology"],
    learned: false,
    letter: "J"
  },
  {
    id: "v11",
    word: "Knowledge",
    translation: "Conocimiento",
    unit: "Unit 2",
    grammar_type: "Noun",
    pronunciation: "/ˈnɒl.ɪdʒ/",
    example: "Sharing knowledge is the best way to help other learners.",
    tags: ["education", "mind"],
    learned: false,
    letter: "K"
  },
  {
    id: "v12",
    word: "Lively",
    translation: "Alegre / Lleno de vida",
    unit: "Unit 4",
    grammar_type: "Adjective",
    pronunciation: "/ˈlaɪv.li/",
    example: "The children played games in a lively and happy way.",
    tags: ["energy", "happy"],
    letter: "L"
  }
];

export default function App() {
  // --- ESTADOS DE LA APLICACIÓN ---
  const [vocabulary, setVocabulary] = useState(INITIAL_VOCABULARY);
  const [currentView, setCurrentView] = useState('home'); // home, glossary, units, practice, import, stats
  const [selectedUnit, setSelectedUnit] = useState('All');
  const [selectedLetter, setSelectedLetter] = useState('A');
  const [searchQuery, setSearchQuery] = useState('');
  
  // Accesibilidad (DUA)
  const [theme, setTheme] = useState('light'); // light, dark, highcontrast
  const [fontSize, setFontSize] = useState('medium'); // small, medium, large, xlarge
  const [fontFamily, setFontFamily] = useState('lexend'); // lexend, comic, sans
  const [ttsSpeed, setTtsSpeed] = useState(0.85); // Más lento por defecto para accesibilidad cognitiva
  const [showAccessibilityPanel, setShowAccessibilityPanel] = useState(false);

  // Estados de los juegos interactivos
  const [selectedGame, setSelectedGame] = useState(null); // null, flashcards, match, memory, choice, gap, spelling, quiz
  const [gameUnit, setGameUnit] = useState('Unit 1');
  const [gameState, setGameState] = useState({});

  // Simulación del Ingestor de Documentos
  const [importText, setImportText] = useState('');
  const [importedWords, setImportedWords] = useState([]);
  const [isParsing, setIsParsing] = useState(false);
  const [importStatus, setImportStatus] = useState(null);

  // --- AUDIO TEXT-TO-SPEECH ---
  const speakWord = (wordText) => {
    if ('speechSynthesis' in window) {
      window.speechSynthesis.cancel(); // Detener audios anteriores
      const utterance = new SpeechSynthesisUtterance(wordText);
      utterance.lang = 'en-US';
      utterance.rate = ttsSpeed;
      window.speechSynthesis.speak(utterance);
    } else {
      console.warn("Speech Synthesis no es compatible con este navegador.");
    }
  };

  // --- FILTRADO DE PALABRAS ---
  const filteredWords = useMemo(() => {
    return vocabulary.filter(item => {
      const matchSearch = 
        item.word.toLowerCase().includes(searchQuery.toLowerCase()) ||
        item.translation.toLowerCase().includes(searchQuery.toLowerCase()) ||
        item.unit.toLowerCase().includes(searchQuery.toLowerCase()) ||
        item.grammar_type.toLowerCase().includes(searchQuery.toLowerCase()) ||
        item.tags.some(t => t.toLowerCase().includes(searchQuery.toLowerCase()));
      return matchSearch;
    });
  }, [vocabulary, searchQuery]);

  // Palabras agrupadas por unidades
  const unitsList = useMemo(() => {
    const units = new Set(vocabulary.map(item => item.unit));
    return Array.from(units).sort();
  }, [vocabulary]);

  // --- CONTROL DE ACCESIBILIDAD ---
  const getThemeClass = () => {
    if (theme === 'dark') return 'bg-slate-900 text-slate-100 dark-theme';
    if (theme === 'highcontrast') return 'bg-black text-yellow-300 border-yellow-400 high-contrast';
    return 'bg-slate-50 text-slate-800 light-theme';
  };

  const getFontSizeClass = () => {
    if (fontSize === 'small') return 'text-sm';
    if (fontSize === 'large') return 'text-lg md:text-xl';
    if (fontSize === 'xlarge') return 'text-xl md:text-2xl font-bold';
    return 'text-base';
  };

  const getFontFamilyClass = () => {
    if (fontFamily === 'comic') return 'font-comic tracking-wide';
    if (fontFamily === 'sans') return 'font-jakarta';
    return 'font-lexend tracking-normal';
  };

  // --- GENERAR JUEGOS AUTOMÁTICAMENTE ---
  const startFlashcards = (unit) => {
    const words = vocabulary.filter(w => w.unit === unit);
    if (words.length === 0) return;
    setGameState({
      words,
      currentIndex: 0,
      showTranslation: false,
      completed: false
    });
    setSelectedGame('flashcards');
  };

  const startMatch = (unit) => {
    const words = vocabulary.filter(w => w.unit === unit).slice(0, 5);
    if (words.length < 3) {
      setGameState({ error: "Se necesitan al menos 3 palabras en esta unidad para jugar." });
      setSelectedGame('match');
      return;
    }
    // Crear cartas de inglés y español
    const englishCards = words.map(w => ({ id: `en-${w.id}`, text: w.word, type: 'en', originalId: w.id }));
    const spanishCards = words.map(w => ({ id: `es-${w.id}`, text: w.translation, type: 'es', originalId: w.id }));
    
    // Mezclar las cartas
    const shuffledCards = [...englishCards, ...spanishCards].sort(() => Math.random() - 0.5);
    
    setGameState({
      cards: shuffledCards,
      selectedCard: null,
      matches: [],
      score: 0,
      gameOver: false,
      error: null
    });
    setSelectedGame('match');
  };

  const startMemory = (unit) => {
    const words = vocabulary.filter(w => w.unit === unit).slice(0, 4); // 4 pares = 8 cartas
    if (words.length < 2) {
      setGameState({ error: "Se necesitan al menos 2 palabras en esta unidad para jugar." });
      setSelectedGame('memory');
      return;
    }
    
    const cards = [];
    words.forEach(w => {
      cards.push({ id: `en-${w.id}`, text: w.word, type: 'en', pairId: w.id, isFlipped: false, isMatched: false });
      cards.push({ id: `es-${w.id}`, text: w.translation, type: 'es', pairId: w.id, isFlipped: false, isMatched: false });
    });

    setGameState({
      cards: cards.sort(() => Math.random() - 0.5),
      flippedIndices: [],
      matchesCount: 0,
      turns: 0,
      gameOver: false,
      error: null
    });
    setSelectedGame('memory');
  };

  const startMultipleChoice = (unit) => {
    const unitWords = vocabulary.filter(w => w.unit === unit);
    if (unitWords.length < 3) {
      setGameState({ error: "Necesitas al menos 3 palabras en esta unidad para el test de opciones." });
      setSelectedGame('choice');
      return;
    }

    const allTranslations = vocabulary.map(w => w.translation);
    const questions = unitWords.map(word => {
      // Filtrar respuestas incorrectas al azar
      const incorrect = allTranslations
        .filter(t => t !== word.translation)
        .sort(() => Math.random() - 0.5)
        .slice(0, 3);
      
      const options = [...incorrect, word.translation].sort(() => Math.random() - 0.5);

      return {
        word: word.word,
        correctAnswer: word.translation,
        options,
        userAnswer: null
      };
    });

    setGameState({
      questions,
      currentIndex: 0,
      score: 0,
      showFeedback: false,
      gameOver: false,
      error: null
    });
    setSelectedGame('choice');
  };

  const startFillGap = (unit) => {
    const unitWords = vocabulary.filter(w => w.unit === unit && w.example);
    if (unitWords.length === 0) {
      setGameState({ error: "No hay ejemplos prácticos con frases en esta unidad para rellenar huecos." });
      setSelectedGame('gap');
      return;
    }

    const questions = unitWords.map(word => {
      // Reemplazar la palabra en el ejemplo para crear el hueco
      const regex = new RegExp(`\\b${word.word}\\b`, 'gi');
      const gapSentence = word.example.replace(regex, "_______");
      
      // Opciones para elegir
      const incorrectWords = vocabulary
        .filter(w => w.word !== word.word)
        .map(w => w.word)
        .sort(() => Math.random() - 0.5)
        .slice(0, 3);
      const options = [...incorrectWords, word.word].sort(() => Math.random() - 0.5);

      return {
        sentence: gapSentence,
        correctWord: word.word,
        options,
        translation: word.translation,
        userAnswer: null
      };
    });

    setGameState({
      questions,
      currentIndex: 0,
      score: 0,
      gameOver: false,
      error: null
    });
    setSelectedGame('gap');
  };

  const startSpelling = (unit) => {
    const unitWords = vocabulary.filter(w => w.unit === unit);
    if (unitWords.length === 0) {
      setGameState({ error: "No hay palabras disponibles para practicar deletreo." });
      setSelectedGame('spelling');
      return;
    }

    setGameState({
      words: unitWords.sort(() => Math.random() - 0.5),
      currentIndex: 0,
      inputValue: '',
      isCorrect: null,
      score: 0,
      hintUsed: false,
      gameOver: false,
      error: null
    });
    setSelectedGame('spelling');
  };

  const startUnitQuiz = (unit) => {
    const unitWords = vocabulary.filter(w => w.unit === unit);
    if (unitWords.length < 3) {
      setGameState({ error: "Necesitas al menos 3 palabras para generar un Quiz completo de esta Unidad." });
      setSelectedGame('quiz');
      return;
    }

    // El quiz mezclará preguntas de Opción Múltiple y Rellenar Huecos
    const questions = unitWords.map((word, index) => {
      const isChoice = index % 2 === 0;
      const allOptions = vocabulary.map(w => w.translation);
      const incorrectOpts = allOptions.filter(o => o !== word.translation).sort(() => Math.random() - 0.5).slice(0, 3);
      const options = [...incorrectOpts, word.translation].sort(() => Math.random() - 0.5);

      if (isChoice || !word.example) {
        return {
          type: 'choice',
          title: `¿Qué significa la palabra "${word.word}"?`,
          correct: word.translation,
          options,
          userAnswer: null,
          wordObj: word
        };
      } else {
        const regex = new RegExp(`\\b${word.word}\\b`, 'gi');
        const sentence = word.example.replace(regex, "_______");
        const incorrectWords = vocabulary.filter(w => w.word !== word.word).map(w => w.word).sort(() => Math.random() - 0.5).slice(0, 3);
        const sentenceOptions = [...incorrectWords, word.word].sort(() => Math.random() - 0.5);

        return {
          type: 'gap',
          title: `Completa la frase con la palabra correcta:`,
          text: sentence,
          correct: word.word,
          options: sentenceOptions,
          userAnswer: null,
          wordObj: word
        };
      }
    });

    setGameState({
      questions,
      currentIndex: 0,
      score: 0,
      quizAnswers: [],
      gameOver: false,
      error: null
    });
    setSelectedGame('quiz');
  };

  // --- MANEJADORES DE ACCIONES DE JUEGOS ---
  
  // Flashcards
  const handleNextFlashcard = () => {
    if (gameState.currentIndex < gameState.words.length - 1) {
      setGameState(prev => ({
        ...prev,
        currentIndex: prev.currentIndex + 1,
        showTranslation: false
      }));
    } else {
      setGameState(prev => ({ ...prev, completed: true }));
    }
  };

  // Emparejar (Match)
  const handleMatchSelect = (card) => {
    if (gameState.matches.includes(card.originalId)) return;

    if (!gameState.selectedCard) {
      setGameState(prev => ({ ...prev, selectedCard: card }));
    } else {
      const firstCard = gameState.selectedCard;
      
      // Evitar emparejar la misma carta o cartas del mismo tipo
      if (firstCard.id === card.id || firstCard.type === card.type) {
        setGameState(prev => ({ ...prev, selectedCard: card }));
        return;
      }

      if (firstCard.originalId === card.originalId) {
        // Acierto
        const newMatches = [...gameState.matches, card.originalId];
        const isGameOver = newMatches.length === gameState.cards.length / 2;
        setGameState(prev => ({
          ...prev,
          matches: newMatches,
          selectedCard: null,
          score: prev.score + 20,
          gameOver: isGameOver
        }));
        speakWord(vocabulary.find(w => w.id === card.originalId).word);
      } else {
        // Error temporal
        setGameState(prev => ({ ...prev, selectedCard: card }));
      }
    }
  };

  // Memoria (Memory)
  const handleMemorySelect = (index) => {
    const { flippedIndices, cards, matchesCount, turns } = gameState;
    
    // Evitar interacciones si ya hay 2 cartas dadas la vuelta o la carta ya está revelada
    if (flippedIndices.length >= 2 || cards[index].isFlipped || cards[index].isMatched) return;

    const updatedCards = [...cards];
    updatedCards[index].isFlipped = true;

    const newFlippedIndices = [...flippedIndices, index];

    setGameState(prev => ({
      ...prev,
      cards: updatedCards,
      flippedIndices: newFlippedIndices
    }));

    if (newFlippedIndices.length === 2) {
      const [firstIdx, secondIdx] = newFlippedIndices;
      const firstCard = cards[firstIdx];
      const secondCard = cards[secondIdx];

      if (firstCard.pairId === secondCard.pairId) {
        // ¡Pareja encontrada!
        setTimeout(() => {
          setGameState(prev => {
            const nextCards = [...prev.cards];
            nextCards[firstIdx].isMatched = true;
            nextCards[secondIdx].isMatched = true;
            
            const matches = prev.matchesCount + 1;
            const isGameOver = matches === prev.cards.length / 2;

            return {
              ...prev,
              cards: nextCards,
              flippedIndices: [],
              matchesCount: matches,
              turns: prev.turns + 1,
              gameOver: isGameOver
            };
          });
          speakWord(vocabulary.find(w => w.id === firstCard.pairId).word);
        }, 500);
      } else {
        // No coinciden, voltear de nuevo después de 1.2 segundos
        setTimeout(() => {
          setGameState(prev => {
            const nextCards = [...prev.cards];
            nextCards[firstIdx].isFlipped = false;
            nextCards[secondIdx].isFlipped = false;
            return {
              ...prev,
              cards: nextCards,
              flippedIndices: [],
              turns: prev.turns + 1
            };
          });
        }, 1200);
      }
    }
  };

  // Opción Múltiple (Multiple Choice)
  const handleMultipleChoiceAnswer = (answer) => {
    const { questions, currentIndex, score } = gameState;
    const currentQuestion = questions[currentIndex];
    const isCorrect = answer === currentQuestion.correctAnswer;
    
    const updatedQuestions = [...questions];
    updatedQuestions[currentIndex].userAnswer = answer;

    setGameState(prev => ({
      ...prev,
      questions: updatedQuestions,
      score: isCorrect ? prev.score + 10 : prev.score,
      showFeedback: true
    }));
    
    if (isCorrect) {
      speakWord(currentQuestion.word);
    }
  };

  const handleNextMultipleChoice = () => {
    const { currentIndex, questions } = gameState;
    if (currentIndex < questions.length - 1) {
      setGameState(prev => ({
        ...prev,
        currentIndex: prev.currentIndex + 1,
        showFeedback: false
      }));
    } else {
      setGameState(prev => ({ ...prev, gameOver: true }));
    }
  };

  // Rellenar Huecos (Fill Gap)
  const handleFillGapAnswer = (option) => {
    const { questions, currentIndex, score } = gameState;
    const current = questions[currentIndex];
    const isCorrect = option === current.correctWord;

    const updated = [...questions];
    updated[currentIndex].userAnswer = option;

    setGameState(prev => ({
      ...prev,
      questions: updated,
      score: isCorrect ? prev.score + 15 : prev.score
    }));

    if (isCorrect) {
      speakWord(current.correctWord);
    }

    setTimeout(() => {
      if (currentIndex < questions.length - 1) {
        setGameState(prev => ({ ...prev, currentIndex: prev.currentIndex + 1 }));
      } else {
        setGameState(prev => ({ ...prev, gameOver: true }));
      }
    }, 1500);
  };

  // Deletreo (Spelling)
  const handleSpellingSubmit = (e) => {
    e.preventDefault();
    const { words, currentIndex, inputValue, score } = gameState;
    const targetWord = words[currentIndex].word.trim();
    const isCorrect = inputValue.trim().toLowerCase() === targetWord.toLowerCase();

    setGameState(prev => ({
      ...prev,
      isCorrect,
      score: isCorrect ? prev.score + 25 : prev.score
    }));

    if (isCorrect) {
      speakWord(targetWord);
    }
  };

  const handleNextSpelling = () => {
    const { currentIndex, words } = gameState;
    if (currentIndex < words.length - 1) {
      setGameState(prev => ({
        ...prev,
        currentIndex: prev.currentIndex + 1,
        inputValue: '',
        isCorrect: null,
        hintUsed: false
      }));
    } else {
      setGameState(prev => ({ ...prev, gameOver: true }));
    }
  };

  // Quiz Completo (Unit Quiz)
  const handleQuizAnswer = (answer) => {
    const { questions, currentIndex, score } = gameState;
    const current = questions[currentIndex];
    const isCorrect = answer === current.correct;

    const updated = [...questions];
    updated[currentIndex].userAnswer = answer;

    setGameState(prev => ({
      ...prev,
      questions: updated,
      score: isCorrect ? prev.score + 1 : prev.score
    }));

    if (isCorrect && current.wordObj) {
      speakWord(current.wordObj.word);
    }

    setTimeout(() => {
      if (currentIndex < questions.length - 1) {
        setGameState(prev => ({ ...prev, currentIndex: prev.currentIndex + 1 }));
      } else {
        setGameState(prev => ({ ...prev, gameOver: true }));
      }
    }, 1200);
  };

  // --- REGISTRO DE APRENDIZAJE Y ACCIONES DE PALABRAS ---
  const toggleLearned = (id) => {
    setVocabulary(prev => prev.map(item => {
      if (item.id === id) {
        return { ...item, learned: !item.learned };
      }
      return item;
    }));
  };

  const addNewWord = (newWordObj) => {
    setVocabulary(prev => {
      if (prev.some(w => w.word.toLowerCase() === newWordObj.word.toLowerCase())) {
        return prev; // Evitar duplicado directo
      }
      return [newWordObj, ...prev];
    });
  };

  const deleteWord = (id) => {
    setVocabulary(prev => prev.filter(item => item.id !== id));
  };

  // --- IMPORTADOR DE DOCUMENTOS (SIMULADO) ---
  const handleSimulateImport = () => {
    if (!importText.trim()) return;

    setIsParsing(true);
    setImportStatus(null);

    setTimeout(() => {
      // Simular extracción inteligente basada en Regex e IA
      const lines = importText.split('\n');
      const detected = [];

      lines.forEach((line, index) => {
        // Buscar patrones como "palabra - traducción" o "palabra : traducción"
        const parts = line.split(/[-:–]/);
        if (parts.length >= 2 && parts[0].trim().length > 1) {
          const word = parts[0].trim();
          const translation = parts[1].trim();
          
          // Clasificación gramatical automática de apoyo cognitivo
          let grammar = 'Noun';
          if (word.endsWith('ly')) grammar = 'Adverb';
          else if (word.endsWith('ing') || word.endsWith('ed')) grammar = 'Adjective';
          else if (word.length > 8 && word.endsWith('ate')) grammar = 'Verb';

          // Evitar registrar duplicados en la misma importación
          if (!detected.some(w => w.word.toLowerCase() === word.toLowerCase())) {
            detected.push({
              id: `imported-${index}-${Date.now()}`,
              word: word.charAt(0).toUpperCase() + word.slice(1),
              translation: translation.charAt(0).toUpperCase() + translation.slice(1),
              unit: selectedUnit === 'All' ? 'Unit 1' : selectedUnit,
              grammar_type: grammar,
              pronunciation: `/pʰrəʊˈnʌn.si.eɪ.ʃən/`, // marcador
              example: `The word ${word} is newly imported vocabulary.`,
              tags: ["imported"],
              learned: false,
              letter: word.charAt(0).toUpperCase()
            });
          }
        }
      });

      if (detected.length === 0) {
        // En caso de texto simple no estructurado, simular extracción ficticia
        detected.push({
          id: `imp-1-${Date.now()}`,
          word: "Innovation",
          translation: "Innovación",
          unit: "Unit 1",
          grammar_type: "Noun",
          pronunciation: "/ˌɪn.əˈveɪ.ʃən/",
          example: "Technical innovation is essential for progress.",
          tags: ["imported", "tech"],
          learned: false,
          letter: "I"
        });
        detected.push({
          id: `imp-2-${Date.now()}`,
          word: "Enthusiastic",
          translation: "Entusiasta",
          unit: "Unit 2",
          grammar_type: "Adjective",
          pronunciation: "/ɪnˈθjuː.zi.æst.ɪk/",
          example: "She is very enthusiastic about teaching children.",
          tags: ["imported", "emotion"],
          learned: false,
          letter: "E"
        });
      }

      setImportedWords(detected);
      setIsParsing(false);
      setImportStatus('preview');
    }, 1500);
  };

  const confirmImport = () => {
    // Filtrar duplicados con el vocabulario actual
    const currentWordsLower = vocabulary.map(w => w.word.toLowerCase());
    const uniqueImported = importedWords.filter(w => !currentWordsLower.includes(w.word.toLowerCase()));

    setVocabulary(prev => [...uniqueImported, ...prev]);
    setImportStatus('success');
    setImportedWords([]);
    setImportText('');
  };

  // --- CÁLCULO DE ESTADÍSTICAS ---
  const stats = useMemo(() => {
    const total = vocabulary.length;
    const learned = vocabulary.filter(w => w.learned).length;
    const percentage = total > 0 ? Math.round((learned / total) * 100) : 0;
    
    // Contar tipos gramaticales para visualizaciones de progreso
    const grammarCounts = vocabulary.reduce((acc, curr) => {
      acc[curr.grammar_type] = (acc[curr.grammar_type] || 0) + 1;
      return acc;
    }, {});

    return { total, learned, percentage, grammarCounts };
  }, [vocabulary]);

  return (
    <div className={`min-h-screen transition-colors duration-200 ${getThemeClass()} ${getFontFamilyClass()}`}>
      <style>{fontStyles}</style>

      {/* --- ACCESSIBILITY BOTTOM FIXED TOOLBAR --- */}
      <div className="fixed bottom-4 right-4 z-50">
        <button 
          onClick={() => setShowAccessibilityPanel(!showAccessibilityPanel)}
          className="bg-indigo-600 hover:bg-indigo-700 text-white p-4 rounded-full shadow-2xl flex items-center justify-center border-2 border-white focus:ring-4 focus:ring-indigo-300 transition-transform hover:scale-105"
          aria-label="Panel de Accesibilidad DUA"
          title="Opciones de Accesibilidad y Ayuda Visual DUA"
        >
          <Sliders className="w-6 h-6" />
          <span className="ml-2 font-bold hidden md:inline">Accesibilidad DUA</span>
        </button>

        {showAccessibilityPanel && (
          <div className="absolute bottom-16 right-0 w-80 p-6 rounded-2xl shadow-3xl border border-slate-200 dark:border-slate-700 bg-white text-slate-800 dark:bg-slate-800 dark:text-slate-100 animate-in fade-in slide-in-from-bottom-5">
            <h3 className="text-lg font-bold flex items-center border-b pb-2 mb-4">
              <Settings className="w-5 h-5 mr-2 text-indigo-500" />
              Adaptación Visual & Voz
            </h3>
            
            {/* Selector de Contraste / Tema */}
            <div className="mb-4">
              <label className="block text-xs font-bold uppercase tracking-wider text-slate-500 dark:text-slate-400 mb-2">Tema y Contraste</label>
              <div className="grid grid-cols-3 gap-2">
                <button 
                  onClick={() => setTheme('light')}
                  className={`py-2 px-1 text-xs font-semibold rounded-lg border ${theme === 'light' ? 'border-indigo-600 bg-indigo-50 text-indigo-700' : 'border-slate-200 hover:bg-slate-50 text-slate-700'}`}
                >
                  Claro
                </button>
                <button 
                  onClick={() => setTheme('dark')}
                  className={`py-2 px-1 text-xs font-semibold rounded-lg border ${theme === 'dark' ? 'border-indigo-400 bg-indigo-950 text-indigo-300' : 'border-slate-700 hover:bg-slate-800 text-slate-300'}`}
                >
                  Oscuro
                </button>
                <button 
                  onClick={() => setTheme('highcontrast')}
                  className={`py-2 px-1 text-xs font-bold rounded-lg border ${theme === 'highcontrast' ? 'border-yellow-400 bg-black text-yellow-300' : 'border-slate-200 text-slate-800 hover:bg-slate-100'}`}
                >
                  Alto Contraste
                </button>
              </div>
            </div>

            {/* Tamaño del texto */}
            <div className="mb-4">
              <label className="block text-xs font-bold uppercase tracking-wider text-slate-500 dark:text-slate-400 mb-2">Tamaño de letra</label>
              <div className="grid grid-cols-4 gap-2">
                {['small', 'medium', 'large', 'xlarge'].map((size) => (
                  <button
                    key={size}
                    onClick={() => setFontSize(size)}
                    className={`py-1 px-2 text-xs font-bold rounded-lg border ${fontSize === size ? 'bg-indigo-600 text-white' : 'bg-slate-100 hover:bg-slate-200 text-slate-800'}`}
                  >
                    {size === 'small' ? 'A-' : size === 'medium' ? 'A' : size === 'large' ? 'A+' : 'A++'}
                  </button>
                ))}
              </div>
            </div>

            {/* Fuentes Adaptadas para Dislexia / TDAH */}
            <div className="mb-4">
              <label className="block text-xs font-bold uppercase tracking-wider text-slate-500 dark:text-slate-400 mb-2">Tipografía Especial</label>
              <div className="grid grid-cols-3 gap-2">
                <button 
                  onClick={() => setFontFamily('lexend')}
                  className={`py-2 px-1 text-xs rounded-lg border font-lexend ${fontFamily === 'lexend' ? 'bg-indigo-600 text-white' : 'bg-slate-100 text-slate-800'}`}
                >
                  Lexend
                </button>
                <button 
                  onClick={() => setFontFamily('comic')}
                  className={`py-2 px-1 text-xs rounded-lg border font-comic ${fontFamily === 'comic' ? 'bg-indigo-600 text-white' : 'bg-slate-100 text-slate-800'}`}
                >
                  Dislexia / Comic
                </button>
                <button 
                  onClick={() => setFontFamily('sans')}
                  className={`py-2 px-1 text-xs rounded-lg border font-jakarta ${fontFamily === 'sans' ? 'bg-indigo-600 text-white' : 'bg-slate-100 text-slate-800'}`}
                >
                  Estándar
                </button>
              </div>
              <p className="text-[10px] mt-2 text-indigo-600 dark:text-indigo-400 font-semibold leading-tight">
                * Las fuentes "Lexend" y "Comic" tienen pesos visuales específicos diseñados para facilitar la lectura silábica y evitar la rotación mental de caracteres.
              </p>
            </div>

            {/* Velocidad de Pronunciación */}
            <div>
              <label className="block text-xs font-bold uppercase tracking-wider text-slate-500 dark:text-slate-400 mb-1 flex justify-between">
                <span>Velocidad de voz (TTS)</span>
                <span className="font-bold text-indigo-600">{ttsSpeed}x</span>
              </label>
              <input 
                type="range" 
                min="0.5" 
                max="1.2" 
                step="0.05" 
                value={ttsSpeed} 
                onChange={(e) => setTtsSpeed(parseFloat(e.target.value))}
                className="w-full h-2 bg-slate-200 rounded-lg appearance-none cursor-pointer"
              />
              <span className="text-[10px] text-slate-500">Ideal para alumnado con Trastorno Específico del Lenguaje (TEL) o procesamiento lento.</span>
            </div>
          </div>
        )}
      </div>

      {/* --- ENCABEZADO PRINCIPAL (NAV) --- */}
      <header className="border-b border-slate-200 dark:border-slate-800 bg-white dark:bg-slate-900 sticky top-0 z-40 transition-shadow hover:shadow-md">
        <div className="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8 py-4 flex flex-col md:flex-row items-center justify-between gap-4">
          
          {/* Logo / Título */}
          <div className="flex items-center space-x-3 cursor-pointer" onClick={() => setCurrentView('home')}>
            <div className="p-3 bg-indigo-600 text-white rounded-2xl shadow-lg shadow-indigo-200 dark:shadow-none">
              <BookOpen className="w-7 h-7" />
            </div>
            <div>
              <h1 className="text-2xl font-extrabold tracking-tight font-jakarta text-indigo-600 dark:text-indigo-400 flex items-center">
                English Vocabulary Hub
              </h1>
              <p className="text-xs text-slate-500 dark:text-slate-400 font-medium">Plataforma Educativa Inclusiva • DUA</p>
            </div>
          </div>

          {/* Buscador Global Integrado */}
          <div className="relative w-full md:w-96">
            <Search className="absolute left-3.5 top-1/2 -translate-y-1/2 text-slate-400 w-5 h-5" />
            <input 
              type="text" 
              placeholder="Buscar por palabra, traducción o unidad..."
              value={searchQuery}
              onChange={(e) => setSearchQuery(e.target.value)}
              className="w-full pl-11 pr-4 py-2.5 rounded-2xl bg-slate-100 dark:bg-slate-800 text-sm border-2 border-transparent focus:border-indigo-500 focus:bg-white dark:focus:bg-slate-900 transition-all outline-none"
            />
          </div>

          {/* Menú de Navegación Simple */}
          <nav className="flex items-center space-x-2 w-full md:w-auto overflow-x-auto pb-1 md:pb-0">
            {[
              { id: 'home', label: 'Dashboard', icon: Grid },
              { id: 'glossary', label: 'Glosario A-Z', icon: Book },
              { id: 'units', label: 'Unidades', icon: Layers },
              { id: 'practice', label: 'Práctica & Juegos', icon: Play },
              { id: 'import', label: 'Importar', icon: FileUp }
            ].map(item => {
              const Icon = item.icon;
              const isActive = currentView === item.id;
              return (
                <button
                  key={item.id}
                  onClick={() => {
                    setCurrentView(item.id);
                    setSelectedGame(null); // Resetear juego activo si cambia de pestaña
                  }}
                  className={`flex items-center space-x-2 px-4 py-2.5 rounded-xl font-bold text-sm transition-all focus:outline-none focus:ring-2 focus:ring-indigo-500 ${
                    isActive 
                      ? 'bg-indigo-600 text-white shadow-md' 
                      : 'hover:bg-slate-100 dark:hover:bg-slate-800 text-slate-600 dark:text-slate-300'
                  }`}
                >
                  <Icon className="w-4 h-4" />
                  <span>{item.label}</span>
                </button>
              );
            })}
          </nav>
        </div>
      </header>

      {/* --- CUERPO PRINCIPAL --- */}
      <main className={`max-w-7xl mx-auto px-4 sm:px-6 lg:px-8 py-8 ${getFontSizeClass()}`}>
        
        {/* Banner de accesibilidad cognitiva para cuando se activa el buscador */}
        {searchQuery && (
          <div className="mb-6 p-4 rounded-2xl bg-indigo-50 dark:bg-slate-800 border-2 border-indigo-200 dark:border-indigo-900 flex items-center justify-between">
            <div className="flex items-center space-x-3">
              <Lightbulb className="w-5 h-5 text-indigo-600 dark:text-indigo-400 shrink-0" />
              <p className="text-sm font-semibold text-slate-700 dark:text-slate-300">
                Se muestran resultados de búsqueda en tiempo real para: <span className="font-extrabold text-indigo-700 dark:text-indigo-400">"{searchQuery}"</span>
              </p>
            </div>
            <button 
              onClick={() => setSearchQuery('')}
              className="text-xs font-bold text-indigo-600 dark:text-indigo-400 hover:underline"
            >
              Limpiar búsqueda
            </button>
          </div>
        )}

        {/* ==================================== */}
        {/* PANTALLA 1: HOME / DASHBOARD */}
        {/* ==================================== */}
        {currentView === 'home' && (
          <div className="space-y-8 animate-in fade-in duration-300">
            
            {/* Banner de bienvenida inclusivo */}
            <div className="p-8 rounded-3xl bg-gradient-to-r from-indigo-600 via-indigo-700 to-violet-700 text-white shadow-xl relative overflow-hidden">
              <div className="relative z-10 max-w-2xl">
                <h2 className="text-3xl md:text-4xl font-extrabold font-jakarta mb-3">
                  Welcome to English Vocabulary Hub
                </h2>
                <p className="text-base md:text-lg text-indigo-100 leading-relaxed font-medium mb-6">
                  Una herramienta educativa adaptada con metodologías visuales simplificadas. Practica y consolida tu vocabulario de clase a través de juegos interactivos sin barreras cognitivas.
                </p>
                <div className="flex flex-wrap gap-3">
                  <button 
                    onClick={() => setCurrentView('practice')}
                    className="px-6 py-3 rounded-xl bg-white text-indigo-700 font-extrabold shadow-md hover:bg-slate-50 transition-all flex items-center space-x-2"
                  >
                    <Play className="w-5 h-5 text-indigo-600 fill-indigo-600" />
                    <span>Empezar a Jugar</span>
                  </button>
                  <button 
                    onClick={() => setCurrentView('glossary')}
                    className="px-6 py-3 rounded-xl bg-indigo-500/30 text-white font-extrabold border border-indigo-300 hover:bg-indigo-500/50 transition-all flex items-center space-x-2"
                  >
                    <Book className="w-5 h-5" />
                    <span>Explorar Glosario</span>
                  </button>
                </div>
              </div>
              <div className="absolute right-0 bottom-0 opacity-10 transform translate-y-12 translate-x-12 hidden lg:block">
                <BookOpen className="w-96 h-96" />
              </div>
            </div>

            {/* Panel de Seguimiento del Aprendizaje */}
            <section className="bg-white dark:bg-slate-800 rounded-3xl p-6 shadow-md border border-slate-100 dark:border-slate-700">
              <h3 className="text-xl font-extrabold mb-6 flex items-center text-slate-800 dark:text-slate-100">
                <Award className="w-6 h-6 mr-2 text-yellow-500" />
                Mi Panel de Aprendizaje y Progreso
              </h3>
              
              <div className="grid grid-cols-1 md:grid-cols-4 gap-6">
                
                {/* Porcentaje de Dominio */}
                <div className="bg-indigo-50/50 dark:bg-slate-900 rounded-2xl p-6 flex flex-col items-center justify-center text-center">
                  <div className="relative w-28 h-28 flex items-center justify-center mb-3">
                    <svg className="w-full h-full transform -rotate-90">
                      <circle cx="56" cy="56" r="48" className="stroke-slate-200 dark:stroke-slate-800" strokeWidth="8" fill="none" />
                      <circle cx="56" cy="56" r="48" className="stroke-indigo-600 transition-all duration-500" strokeWidth="10" strokeDasharray={301.6} strokeDashoffset={301.6 - (301.6 * stats.percentage) / 100} fill="none" strokeLinecap="round" />
                    </svg>
                    <span className="absolute text-2xl font-extrabold text-indigo-700 dark:text-indigo-400">{stats.percentage}%</span>
                  </div>
                  <h4 className="text-sm font-bold text-slate-700 dark:text-slate-300">Dominio del Vocabulario</h4>
                </div>

                {/* Estadísticas en números */}
                <div className="md:col-span-3 grid grid-cols-1 sm:grid-cols-3 gap-4">
                  
                  <div className="bg-emerald-50 dark:bg-slate-900 border border-emerald-100 dark:border-slate-800 rounded-2xl p-5">
                    <div className="text-emerald-600 dark:text-emerald-400 text-3xl font-extrabold mb-1">
                      {stats.learned}
                    </div>
                    <div className="text-sm font-bold text-emerald-800 dark:text-emerald-300 mb-1">Palabras Aprendidas</div>
                    <p className="text-xs text-slate-500">Completamente consolidadas y listas.</p>
                  </div>

                  <div className="bg-amber-50 dark:bg-slate-900 border border-amber-100 dark:border-slate-800 rounded-2xl p-5">
                    <div className="text-amber-600 dark:text-amber-400 text-3xl font-extrabold mb-1">
                      {stats.total - stats.learned}
                    </div>
                    <div className="text-sm font-bold text-amber-800 dark:text-amber-300 mb-1">Palabras Pendientes</div>
                    <p className="text-xs text-slate-500">Pendientes por repasar en los juegos.</p>
                  </div>

                  <div className="bg-indigo-50 dark:bg-slate-900 border border-indigo-100 dark:border-slate-800 rounded-2xl p-5">
                    <div className="text-indigo-600 dark:text-indigo-400 text-3xl font-extrabold mb-1">
                      {stats.total}
                    </div>
                    <div className="text-sm font-bold text-indigo-800 dark:text-indigo-300 mb-1">Vocablos Totales</div>
                    <p className="text-xs text-slate-500">En la base de datos interactiva.</p>
                  </div>

                </div>
              </div>

              {/* Categorías gramaticales representadas de forma accesible */}
              <div className="mt-8 border-t border-slate-100 dark:border-slate-700 pt-6">
                <h4 className="text-sm font-bold uppercase tracking-wider text-slate-500 dark:text-slate-400 mb-4">Análisis del tipo de vocabulario</h4>
                <div className="grid grid-cols-2 sm:grid-cols-5 gap-3">
                  {Object.entries(stats.grammar_counts || {}).map(([type, count]) => (
                    <div key={type} className="bg-slate-100 dark:bg-slate-900 rounded-xl p-3 text-center">
                      <div className="text-xs font-bold text-slate-500">{type}</div>
                      <div className="text-lg font-extrabold text-slate-700 dark:text-slate-300">{count} {count === 1 ? 'palabra' : 'palabras'}</div>
                    </div>
                  ))}
                </div>
              </div>
            </section>

            {/* Listado Rápido de Vocabulario Reciente con diseño limpio */}
            <section className="bg-white dark:bg-slate-800 rounded-3xl p-6 shadow-md border border-slate-100 dark:border-slate-700">
              <div className="flex justify-between items-center mb-6">
                <h3 className="text-xl font-extrabold text-slate-800 dark:text-slate-100">Palabras Recientes</h3>
                <button 
                  onClick={() => setCurrentView('glossary')}
                  className="text-sm font-bold text-indigo-600 dark:text-indigo-400 flex items-center hover:underline"
                >
                  Ver todo el Glosario <ChevronRight className="w-4 h-4 ml-1" />
                </button>
              </div>

              <div className="grid grid-cols-1 md:grid-cols-2 gap-4">
                {vocabulary.slice(0, 4).map(item => (
                  <div 
                    key={item.id}
                    className="border-2 border-slate-100 dark:border-slate-700 p-5 rounded-2xl flex items-start justify-between hover:border-indigo-200 transition-all bg-slate-50/50 dark:bg-slate-900/50"
                  >
                    <div>
                      <div className="flex items-center space-x-2 mb-1.5">
                        <span className="text-xs font-bold px-2 py-0.5 rounded bg-indigo-100 text-indigo-800 dark:bg-indigo-950 dark:text-indigo-300">
                          {item.grammar_type}
                        </span>
                        <span className="text-xs font-bold px-2 py-0.5 rounded bg-slate-200 text-slate-800 dark:bg-slate-700 dark:text-slate-300">
                          {item.unit}
                        </span>
                      </div>
                      <h4 className="text-xl font-extrabold text-indigo-600 dark:text-indigo-400">{item.word}</h4>
                      <p className="text-sm font-semibold text-slate-600 dark:text-slate-300 mb-2">Traducción: {item.translation}</p>
                      <p className="text-xs text-slate-500 italic">"{item.example}"</p>
                    </div>

                    <div className="flex flex-col space-y-2">
                      <button 
                        onClick={() => speakWord(item.word)}
                        className="p-2.5 rounded-xl bg-indigo-50 dark:bg-slate-800 text-indigo-600 dark:text-indigo-400 hover:bg-indigo-100 transition-colors"
                        title="Escuchar Pronunciación"
                      >
                        <Volume2 className="w-5 h-5" />
                      </button>
                      <button 
                        onClick={() => toggleLearned(item.id)}
                        className={`p-2.5 rounded-xl border transition-all ${
                          item.learned 
                            ? 'bg-emerald-100 text-emerald-800 border-emerald-200' 
                            : 'bg-white text-slate-400 border-slate-200 hover:text-indigo-600'
                        }`}
                        title={item.learned ? "Marcar como pendiente" : "Marcar como aprendido"}
                      >
                        <Check className="w-5 h-5" />
                      </button>
                    </div>
                  </div>
                ))}
              </div>
            </section>
          </div>
        )}

        {/* ==================================== */}
        {/* PANTALLA 2: GLOSARIO ALFABÉTICO */}
        {/* ==================================== */}
        {currentView === 'glossary' && (
          <div className="space-y-6 animate-in fade-in duration-300">
            <div className="flex flex-col md:flex-row md:items-center justify-between gap-4">
              <div>
                <h2 className="text-2xl font-extrabold text-slate-800 dark:text-slate-100">Interactive English Glossary</h2>
                <p className="text-slate-500 dark:text-slate-400">Filtra las palabras por su letra inicial o búscalas directamente.</p>
              </div>

              {/* Filtro de tipo gramatical rápido */}
              <div className="flex flex-wrap gap-2">
                {['All', 'Noun', 'Verb', 'Adjective', 'Adverb', 'Expression'].map(cat => (
                  <button
                    key={cat}
                    onClick={() => setSearchQuery(cat === 'All' ? '' : cat)}
                    className="px-3 py-1.5 rounded-lg text-xs font-bold bg-slate-200 hover:bg-slate-300 dark:bg-slate-800 dark:text-slate-200 text-slate-800 transition-all"
                  >
                    {cat}
                  </button>
                ))}
              </div>
            </div>

            {/* Selector de Letras del Alfabeto */}
            <div className="bg-white dark:bg-slate-800 p-4 rounded-3xl shadow-sm border border-slate-100 dark:border-slate-700">
              <div className="flex flex-wrap gap-2 justify-center">
                {"ABCDEFGHIJKLMNOPQRSTUVWXYZ".split("").map(letter => {
                  const hasWords = vocabulary.some(w => w.word.charAt(0).toUpperCase() === letter);
                  const isSelected = selectedLetter === letter;
                  return (
                    <button
                      key={letter}
                      onClick={() => {
                        setSelectedLetter(letter);
                        setSearchQuery(''); // Limpiar buscador para enfocar letra
                      }}
                      disabled={!hasWords}
                      className={`w-10 h-10 rounded-xl font-extrabold flex items-center justify-center text-sm border-2 transition-all ${
                        isSelected 
                          ? 'bg-indigo-600 text-white border-indigo-600 scale-110 shadow-lg' 
                          : hasWords 
                            ? 'bg-indigo-50 text-indigo-800 border-indigo-100 hover:bg-indigo-100 dark:bg-slate-700 dark:text-slate-100 dark:border-slate-600' 
                            : 'bg-slate-100 text-slate-300 border-transparent cursor-not-allowed opacity-40'
                      }`}
                    >
                      {letter}
                    </button>
                  );
                })}
              </div>
            </div>

            {/* Listado de palabras en forma de Tarjetas DUA */}
            <div className="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-6">
              {(searchQuery ? filteredWords : vocabulary.filter(w => w.word.charAt(0).toUpperCase() === selectedLetter)).map(item => (
                <article 
                  key={item.id}
                  className="bg-white dark:bg-slate-800 rounded-3xl p-6 shadow-md border-2 border-slate-100 dark:border-slate-700 hover:border-indigo-400 transition-all flex flex-col justify-between"
                >
                  <div>
                    <div className="flex items-center justify-between mb-3">
                      <span className="text-xs font-extrabold tracking-wider uppercase px-2.5 py-1 rounded-full bg-indigo-50 text-indigo-700 dark:bg-indigo-950 dark:text-indigo-300">
                        {item.grammar_type}
                      </span>
                      <span className="text-xs font-bold text-slate-400">
                        {item.unit}
                      </span>
                    </div>

                    <h3 className="text-2xl font-extrabold text-indigo-700 dark:text-indigo-400 mb-1 flex items-center justify-between">
                      <span>{item.word}</span>
                      <span className="text-sm font-normal text-slate-400 font-mono tracking-normal">{item.pronunciation}</span>
                    </h3>

                    <p className="text-lg font-bold text-slate-800 dark:text-slate-200 mb-4">
                      {item.translation}
                    </p>

                    <div className="bg-slate-50 dark:bg-slate-900 p-3.5 rounded-2xl mb-4 border border-slate-100 dark:border-slate-800">
                      <span className="text-xs font-extrabold text-indigo-500 uppercase block mb-1">Ejemplo de uso:</span>
                      <p className="text-sm font-medium italic text-slate-600 dark:text-slate-300">
                        "{item.example}"
                      </p>
                    </div>

                    <div className="flex flex-wrap gap-1.5 mb-6">
                      {item.tags.map(tag => (
                        <span key={tag} className="text-xs font-semibold px-2 py-0.5 rounded-md bg-slate-100 text-slate-600 dark:bg-slate-700 dark:text-slate-300">
                          #{tag}
                        </span>
                      ))}
                    </div>
                  </div>

                  {/* Acciones principales de la tarjeta */}
                  <div className="flex items-center space-x-2 border-t border-slate-100 dark:border-slate-700 pt-4">
                    <button
                      onClick={() => speakWord(item.word)}
                      className="flex-1 py-2.5 rounded-xl bg-indigo-50 hover:bg-indigo-100 text-indigo-700 dark:bg-indigo-950 dark:text-indigo-300 font-extrabold text-xs flex items-center justify-center space-x-1.5"
                    >
                      <Volume2 className="w-4 h-4" />
                      <span>Pronunciar</span>
                    </button>

                    <button
                      onClick={() => toggleLearned(item.id)}
                      className={`px-4 py-2.5 rounded-xl border text-xs font-extrabold flex items-center space-x-1 ${
                        item.learned 
                          ? 'bg-emerald-100 text-emerald-800 border-emerald-200' 
                          : 'bg-white hover:bg-slate-50 text-slate-500 border-slate-200'
                      }`}
                    >
                      <Check className="w-4 h-4" />
                      <span>{item.learned ? 'Dominado' : 'Aprender'}</span>
                    </button>

                    <button
                      onClick={() => deleteWord(item.id)}
                      className="p-2.5 rounded-xl text-red-500 hover:bg-red-50 dark:hover:bg-slate-900"
                      title="Eliminar palabra"
                    >
                      <Trash2 className="w-4 h-4" />
                    </button>
                  </div>
                </article>
              ))}

              {/* Mensaje de ausencia de resultados */}
              {(searchQuery ? filteredWords : vocabulary.filter(w => w.word.charAt(0).toUpperCase() === selectedLetter)).length === 0 && (
                <div className="col-span-full py-12 text-center bg-white dark:bg-slate-800 rounded-3xl p-8 border border-slate-200 dark:border-slate-700">
                  <AlertCircle className="w-12 h-12 mx-auto text-indigo-500 mb-4" />
                  <h3 className="text-xl font-bold mb-2">No se encontraron palabras</h3>
                  <p className="text-slate-500">Agrega nuevo vocabulario o cambia el filtro de búsqueda.</p>
                </div>
              )}
            </div>
          </div>
        )}

        {/* ==================================== */}
        {/* PANTALLA 3: UNIDADES DIDÁCTICAS */}
        {/* ==================================== */}
        {currentView === 'units' && (
          <div className="space-y-6 animate-in fade-in duration-300">
            <div>
              <h2 className="text-2xl font-extrabold text-slate-800 dark:text-slate-100">Unidades Didácticas (Units)</h2>
              <p className="text-slate-500 dark:text-slate-400">Organiza tu plan escolar y asocia juegos para consolidar de forma automática.</p>
            </div>

            <div className="grid grid-cols-1 md:grid-cols-4 gap-6">
              
              {/* Listado de Unidades */}
              <div className="md:col-span-1 space-y-2">
                {['All', ...unitsList].map(unit => {
                  const unitCount = vocabulary.filter(w => unit === 'All' ? true : w.unit === unit).length;
                  const unitLearned = vocabulary.filter(w => (unit === 'All' ? true : w.unit === unit) && w.learned).length;
                  const pct = unitCount > 0 ? Math.round((unitLearned / unitCount) * 100) : 0;

                  return (
                    <button
                      key={unit}
                      onClick={() => setSelectedUnit(unit)}
                      className={`w-full text-left p-4 rounded-2xl border-2 transition-all flex justify-between items-center ${
                        selectedUnit === unit 
                          ? 'bg-indigo-600 text-white border-indigo-600 shadow-md' 
                          : 'bg-white dark:bg-slate-800 border-slate-100 dark:border-slate-700 hover:border-slate-200 text-slate-700 dark:text-slate-200'
                      }`}
                    >
                      <div>
                        <div className="font-extrabold text-base">{unit === 'All' ? 'Todas las Unidades' : unit}</div>
                        <div className="text-xs opacity-80">{unitCount} {unitCount === 1 ? 'palabra' : 'palabras'}</div>
                      </div>
                      <span className={`text-xs font-extrabold px-2 py-1 rounded-lg ${
                        selectedUnit === unit ? 'bg-indigo-500 text-white' : 'bg-slate-100 text-slate-800 dark:bg-slate-900 dark:text-slate-100'
                      }`}>
                        {pct}%
                      </span>
                    </button>
                  );
                })}
              </div>

              {/* Detalle de Unidad seleccionada */}
              <div className="md:col-span-3 space-y-6">
                <div className="bg-white dark:bg-slate-800 rounded-3xl p-6 shadow-sm border border-slate-100 dark:border-slate-700">
                  <div className="flex flex-col sm:flex-row sm:items-center justify-between gap-4 mb-6">
                    <div>
                      <h3 className="text-2xl font-extrabold text-slate-800 dark:text-slate-100">
                        {selectedUnit === 'All' ? 'Todas las Unidades' : selectedUnit}
                      </h3>
                      <p className="text-slate-500">
                        Total de palabras registradas: <span className="font-extrabold text-indigo-600">{vocabulary.filter(w => selectedUnit === 'All' ? true : w.unit === selectedUnit).length}</span>
                      </p>
                    </div>

                    {/* Acciones de Juego asociadas a la Unidad */}
                    {selectedUnit !== 'All' && (
                      <div className="flex flex-wrap gap-2">
                        <button
                          onClick={() => {
                            setCurrentView('practice');
                            startUnitQuiz(selectedUnit);
                          }}
                          className="px-4 py-2 rounded-xl bg-amber-500 hover:bg-amber-600 text-white font-extrabold text-sm shadow-sm flex items-center space-x-1.5"
                        >
                          <Award className="w-4 h-4" />
                          <span>Unit Quiz</span>
                        </button>
                        <button
                          onClick={() => {
                            setCurrentView('practice');
                            startFlashcards(selectedUnit);
                          }}
                          className="px-4 py-2 rounded-xl bg-indigo-600 hover:bg-indigo-700 text-white font-extrabold text-sm shadow-sm flex items-center space-x-1.5"
                        >
                          <Play className="w-4 h-4" />
                          <span>Jugar Flashcards</span>
                        </button>
                      </div>
                    )}
                  </div>

                  {/* Tabla accesible de vocabulario para esta unidad */}
                  <div className="overflow-x-auto">
                    <table className="w-full text-left border-collapse">
                      <thead>
                        <tr className="border-b border-slate-100 dark:border-slate-700 text-slate-500 text-xs uppercase font-extrabold">
                          <th className="py-3 px-4">Palabra (Inglés)</th>
                          <th className="py-3 px-4">Traducción</th>
                          <th className="py-3 px-4">Categoría</th>
                          <th className="py-3 px-4">Pronunciación</th>
                          <th className="py-3 px-4 text-center">Estado</th>
                          <th className="py-3 px-4 text-center">Audio</th>
                        </tr>
                      </thead>
                      <tbody>
                        {vocabulary.filter(w => selectedUnit === 'All' ? true : w.unit === selectedUnit).map(item => (
                          <tr 
                            key={item.id}
                            className="border-b border-slate-50 dark:border-slate-800 hover:bg-slate-50 dark:hover:bg-slate-900/40 text-sm font-medium"
                          >
                            <td className="py-3.5 px-4 font-extrabold text-indigo-600 dark:text-indigo-400">{item.word}</td>
                            <td className="py-3.5 px-4 text-slate-700 dark:text-slate-300">{item.translation}</td>
                            <td className="py-3.5 px-4">
                              <span className="text-xs px-2 py-0.5 rounded bg-slate-100 text-slate-700 dark:bg-slate-800 dark:text-slate-300">
                                {item.grammar_type}
                              </span>
                            </td>
                            <td className="py-3.5 px-4 font-mono text-slate-400">{item.pronunciation}</td>
                            <td className="py-3.5 px-4 text-center">
                              <button
                                onClick={() => toggleLearned(item.id)}
                                className={`inline-flex items-center justify-center p-1.5 rounded-full ${
                                  item.learned ? 'bg-emerald-100 text-emerald-800' : 'bg-slate-100 text-slate-400'
                                }`}
                              >
                                <Check className="w-4 h-4" />
                              </button>
                            </td>
                            <td className="py-3.5 px-4 text-center">
                              <button
                                onClick={() => speakWord(item.word)}
                                className="p-1.5 rounded bg-indigo-50 hover:bg-indigo-100 text-indigo-700"
                              >
                                <Volume2 className="w-4 h-4" />
                              </button>
                            </td>
                          </tr>
                        ))}
                      </tbody>
                    </table>
                  </div>
                </div>
              </div>

            </div>
          </div>
        )}

        {/* ==================================== */}
        {/* PANTALLA 4: PRÁCTICA & JUEGOS */}
        {/* ==================================== */}
        {currentView === 'practice' && (
          <div className="space-y-6 animate-in fade-in duration-300">
            
            {!selectedGame ? (
              <>
                <div className="flex flex-col md:flex-row md:items-center justify-between gap-4">
                  <div>
                    <h2 className="text-2xl font-extrabold text-slate-800 dark:text-slate-100">Practice & Educational Games</h2>
                    <p className="text-slate-500 dark:text-slate-400">Juegos educativos automatizados para autoevaluación adaptativa.</p>
                  </div>

                  {/* Selector de Unidad para el juego */}
                  <div className="flex items-center space-x-2">
                    <span className="text-sm font-bold text-slate-500">Unidad de práctica:</span>
                    <select
                      value={gameUnit}
                      onChange={(e) => setGameUnit(e.target.value)}
                      className="bg-white dark:bg-slate-800 border border-slate-300 dark:border-slate-700 rounded-xl px-3 py-1.5 text-sm font-bold outline-none text-slate-800 dark:text-slate-100"
                    >
                      {unitsList.map(u => (
                        <option key={u} value={u}>{u}</option>
                      ))}
                    </select>
                  </div>
                </div>

                {/* Grid de 7 Juegos Autogenerados */}
                <div className="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-6">
                  
                  {/* Juego 1: Flashcards */}
                  <div className="bg-white dark:bg-slate-800 rounded-3xl p-6 shadow-sm border-2 border-slate-100 dark:border-slate-700 flex flex-col justify-between">
                    <div>
                      <div className="p-3 bg-indigo-50 text-indigo-600 rounded-2xl w-fit mb-4">
                        <Bookmark className="w-6 h-6" />
                      </div>
                      <h3 className="text-xl font-extrabold mb-2">1. Flashcards Interactivos</h3>
                      <p className="text-sm text-slate-500 leading-relaxed mb-4">
                        Tarjetas auto-reversibles inglés-español con audio para estimulación visual y auditiva combinada.
                      </p>
                    </div>
                    <button 
                      onClick={() => startFlashcards(gameUnit)}
                      className="w-full py-3 bg-indigo-600 hover:bg-indigo-700 text-white font-extrabold rounded-xl text-sm"
                    >
                      Iniciar Juego
                    </button>
                  </div>

                  {/* Juego 2: Match */}
                  <div className="bg-white dark:bg-slate-800 rounded-3xl p-6 shadow-sm border-2 border-slate-100 dark:border-slate-700 flex flex-col justify-between">
                    <div>
                      <div className="p-3 bg-emerald-50 text-emerald-600 rounded-2xl w-fit mb-4">
                        <Layers className="w-6 h-6" />
                      </div>
                      <h3 className="text-xl font-extrabold mb-2">2. Match Word-Translation</h3>
                      <p className="text-sm text-slate-500 leading-relaxed mb-4">
                        Empareja palabras en inglés con su traducción correspondiente en español con marcadores interactivos rápidos.
                      </p>
                    </div>
                    <button 
                      onClick={() => startMatch(gameUnit)}
                      className="w-full py-3 bg-emerald-600 hover:bg-emerald-700 text-white font-extrabold rounded-xl text-sm"
                    >
                      Iniciar Juego
                    </button>
                  </div>

                  {/* Juego 3: Memory Game */}
                  <div className="bg-white dark:bg-slate-800 rounded-3xl p-6 shadow-sm border-2 border-slate-100 dark:border-slate-700 flex flex-col justify-between">
                    <div>
                      <div className="p-3 bg-amber-50 text-amber-600 rounded-2xl w-fit mb-4">
                        <RotateCcw className="w-6 h-6" />
                      </div>
                      <h3 className="text-xl font-extrabold mb-2">3. Memory Match</h3>
                      <p className="text-sm text-slate-500 leading-relaxed mb-4">
                        El clásico juego de cartas boca abajo. Encuentra las parejas inglés-español entrenando tu retención visual.
                      </p>
                    </div>
                    <button 
                      onClick={() => startMemory(gameUnit)}
                      className="w-full py-3 bg-amber-600 hover:bg-amber-700 text-white font-extrabold rounded-xl text-sm"
                    >
                      Iniciar Juego
                    </button>
                  </div>

                  {/* Juego 4: Multiple Choice */}
                  <div className="bg-white dark:bg-slate-800 rounded-3xl p-6 shadow-sm border-2 border-slate-100 dark:border-slate-700 flex flex-col justify-between">
                    <div>
                      <div className="p-3 bg-sky-50 text-sky-600 rounded-2xl w-fit mb-4">
                        <HelpCircle className="w-6 h-6" />
                      </div>
                      <h3 className="text-xl font-extrabold mb-2">4. Multiple Choice Quiz</h3>
                      <p className="text-sm text-slate-500 leading-relaxed mb-4">
                        Preguntas con opciones múltiples autogeneradas de traducción directa con retroalimentación inmediata.
                      </p>
                    </div>
                    <button 
                      onClick={() => startMultipleChoice(gameUnit)}
                      className="w-full py-3 bg-sky-600 hover:bg-sky-700 text-white font-extrabold rounded-xl text-sm"
                    >
                      Iniciar Juego
                    </button>
                  </div>

                  {/* Juego 5: Fill in the Gap */}
                  <div className="bg-white dark:bg-slate-800 rounded-3xl p-6 shadow-sm border-2 border-slate-100 dark:border-slate-700 flex flex-col justify-between">
                    <div>
                      <div className="p-3 bg-violet-50 text-violet-600 rounded-2xl w-fit mb-4">
                        <FileText className="w-6 h-6" />
                      </div>
                      <h3 className="text-xl font-extrabold mb-2">5. Fill in the Gap</h3>
                      <p className="text-sm text-slate-500 leading-relaxed mb-4">
                        Completar oraciones reales contextualizadas usando los vocablos estudiados en la unidad.
                      </p>
                    </div>
                    <button 
                      onClick={() => startFillGap(gameUnit)}
                      className="w-full py-3 bg-violet-600 hover:bg-violet-700 text-white font-extrabold rounded-xl text-sm"
                    >
                      Iniciar Juego
                    </button>
                  </div>

                  {/* Juego 6: Spelling Challenge */}
                  <div className="bg-white dark:bg-slate-800 rounded-3xl p-6 shadow-sm border-2 border-slate-100 dark:border-slate-700 flex flex-col justify-between">
                    <div>
                      <div className="p-3 bg-rose-50 text-rose-600 rounded-2xl w-fit mb-4">
                        <Volume2 className="w-6 h-6" />
                      </div>
                      <h3 className="text-xl font-extrabold mb-2">6. Spelling & Dictation</h3>
                      <p className="text-sm text-slate-500 leading-relaxed mb-4">
                        Escucha la palabra reproducida por voz sintética y escríbela correctamente. Ideal para disgrafía y dislexia.
                      </p>
                    </div>
                    <button 
                      onClick={() => startSpelling(gameUnit)}
                      className="w-full py-3 bg-rose-600 hover:bg-rose-700 text-white font-extrabold rounded-xl text-sm"
                    >
                      Iniciar Juego
                    </button>
                  </div>

                  {/* Juego 7: Unit Quiz */}
                  <div className="bg-slate-900 text-white rounded-3xl p-6 shadow-md flex flex-col justify-between col-span-1 md:col-span-2 lg:col-span-3 border-2 border-yellow-400">
                    <div className="flex flex-col md:flex-row justify-between gap-4">
                      <div className="max-w-xl">
                        <div className="inline-block px-3 py-1 bg-yellow-400 text-slate-900 font-extrabold rounded-lg text-xs uppercase tracking-wider mb-3">
                          Evaluación Completa
                        </div>
                        <h3 className="text-2xl font-black mb-2">7. Quiz Integrado de Unidad</h3>
                        <p className="text-sm text-slate-300 leading-relaxed mb-4">
                          Prueba mixta de 5 preguntas rápidas para asimilar el aprendizaje del día con recomendaciones y análisis inteligente de fallos.
                        </p>
                      </div>
                      <div className="flex items-center">
                        <Award className="w-16 h-16 text-yellow-400 shrink-0 hidden md:block" />
                      </div>
                    </div>
                    <button 
                      onClick={() => startUnitQuiz(gameUnit)}
                      className="w-full py-3.5 bg-yellow-400 hover:bg-yellow-500 text-slate-950 font-black rounded-xl text-sm shadow-md transition-all"
                    >
                      Realizar Evaluación Completa
                    </button>
                  </div>

                </div>
              </>
            ) : (
              // VISTA DE JUEGO ACTIVO
              <div className="space-y-6">
                
                {/* Botón Volver */}
                <button 
                  onClick={() => setSelectedGame(null)}
                  className="px-4 py-2 rounded-xl bg-slate-100 hover:bg-slate-200 dark:bg-slate-800 dark:text-slate-100 text-slate-700 font-extrabold text-sm flex items-center space-x-2"
                >
                  <ChevronLeft className="w-4 h-4" />
                  <span>Volver a Juegos</span>
                </button>

                {/* --- 1. JUEGO FLASHCARDS --- */}
                {selectedGame === 'flashcards' && (
                  <div className="max-w-xl mx-auto space-y-6">
                    <div className="text-center">
                      <h3 className="text-xl font-extrabold">Flashcards: {gameUnit}</h3>
                      <p className="text-sm text-slate-500">Carta {gameState.currentIndex + 1} de {gameState.words.length}</p>
                    </div>

                    {!gameState.completed ? (
                      <div className="space-y-6">
                        {/* Tarjeta Reversible */}
                        <div 
                          onClick={() => setGameState(prev => ({ ...prev, showTranslation: !prev.showTranslation }))}
                          className={`h-80 rounded-3xl p-8 border-4 cursor-pointer flex flex-col justify-between items-center text-center transition-all transform hover:scale-102 ${
                            gameState.showTranslation 
                              ? 'bg-indigo-600 text-white border-indigo-700 shadow-xl' 
                              : 'bg-white dark:bg-slate-800 text-slate-800 dark:text-slate-100 border-slate-200 dark:border-slate-700 shadow-md'
                          }`}
                        >
                          <div className="text-xs font-bold uppercase tracking-widest opacity-65">
                            {gameState.showTranslation ? "Español (Pulsa para ver Inglés)" : "Inglés (Pulsa para ver Español)"}
                          </div>

                          <div className="space-y-3">
                            <h4 className="text-4xl font-extrabold tracking-tight">
                              {gameState.showTranslation ? gameState.words[gameState.currentIndex].translation : gameState.words[gameState.currentIndex].word}
                            </h4>
                            {!gameState.showTranslation && (
                              <p className="text-sm font-mono opacity-70">{gameState.words[gameState.currentIndex].pronunciation}</p>
                            )}
                          </div>

                          <div className="flex items-center space-x-2">
                            {!gameState.showTranslation ? (
                              <button 
                                onClick={(e) => {
                                  e.stopPropagation();
                                  speakWord(gameState.words[gameState.currentIndex].word);
                                }}
                                className="p-3 bg-indigo-50 text-indigo-700 rounded-full hover:bg-indigo-100 transition-colors"
                              >
                                <Volume2 className="w-6 h-6" />
                              </button>
                            ) : (
                              <p className="text-sm italic opacity-90 font-medium">
                                "{gameState.words[gameState.currentIndex].example}"
                              </p>
                            )}
                          </div>
                        </div>

                        {/* Controles de Navegación */}
                        <div className="flex space-x-4">
                          <button
                            onClick={() => toggleLearned(gameState.words[gameState.currentIndex].id)}
                            className={`flex-1 py-3.5 rounded-2xl border-2 text-sm font-extrabold flex items-center justify-center space-x-2 ${
                              gameState.words[gameState.currentIndex].learned 
                                ? 'bg-emerald-50 text-emerald-800 border-emerald-300' 
                                : 'bg-slate-50 text-slate-700 border-slate-200'
                            }`}
                          >
                            <Check className="w-5 h-5" />
                            <span>{gameState.words[gameState.currentIndex].learned ? 'Dominado' : 'Marcar como Dominado'}</span>
                          </button>

                          <button 
                            onClick={handleNextFlashcard}
                            className="flex-1 py-3.5 rounded-2xl bg-indigo-600 hover:bg-indigo-700 text-white font-extrabold text-sm flex items-center justify-center space-x-2"
                          >
                            <span>Siguiente</span>
                            <ChevronRight className="w-5 h-5" />
                          </button>
                        </div>
                      </div>
                    ) : (
                      // Fin del juego
                      <div className="bg-white dark:bg-slate-800 p-8 rounded-3xl text-center shadow-md space-y-4">
                        <CheckCircle className="w-16 h-16 text-emerald-500 mx-auto" />
                        <h4 className="text-2xl font-black">¡Felicidades!</h4>
                        <p className="text-slate-500">Has revisado todas las flashcards de la {gameUnit}.</p>
                        <button 
                          onClick={() => startFlashcards(gameUnit)}
                          className="px-6 py-3 bg-indigo-600 text-white rounded-xl font-bold"
                        >
                          Volver a empezar
                        </button>
                      </div>
                    )}
                  </div>
                )}

                {/* --- 2. JUEGO MATCH --- */}
                {selectedGame === 'match' && (
                  <div className="max-w-2xl mx-auto space-y-6">
                    <div className="text-center">
                      <h3 className="text-xl font-extrabold">Match Game: {gameUnit}</h3>
                      <p className="text-sm text-slate-500">Puntos acumulados: <span className="font-extrabold text-indigo-600">{gameState.score}</span></p>
                    </div>

                    {gameState.error ? (
                      <div className="p-6 bg-red-50 text-red-800 rounded-2xl text-center font-bold">
                        {gameState.error}
                      </div>
                    ) : !gameState.gameOver ? (
                      <div className="grid grid-cols-2 sm:grid-cols-3 gap-4">
                        {gameState.cards.map((card, idx) => {
                          const isMatched = gameState.matches.includes(card.originalId);
                          const isSelected = gameState.selectedCard?.id === card.id;

                          return (
                            <button
                              key={card.id}
                              onClick={() => handleMatchSelect(card)}
                              disabled={isMatched}
                              className={`h-24 rounded-2xl p-3 flex items-center justify-center text-center font-bold text-sm border-2 transition-all ${
                                isMatched 
                                  ? 'bg-emerald-100 text-emerald-800 border-emerald-300 opacity-60' 
                                  : isSelected 
                                    ? 'bg-indigo-600 text-white border-indigo-700 scale-102 shadow-lg' 
                                    : 'bg-white dark:bg-slate-800 text-slate-800 dark:text-slate-100 border-slate-200 dark:border-slate-700 hover:border-slate-300'
                              }`}
                            >
                              <span>{card.text}</span>
                            </button>
                          );
                        })}
                      </div>
                    ) : (
                      // Fin del juego
                      <div className="bg-white dark:bg-slate-800 p-8 rounded-3xl text-center shadow-md space-y-4">
                        <Award className="w-16 h-16 text-yellow-500 mx-auto animate-bounce" />
                        <h4 className="text-2xl font-black">¡Excelente emparejamiento!</h4>
                        <p className="text-slate-500">Puntaje total obtenido: <span className="font-bold text-emerald-600">{gameState.score} puntos</span></p>
                        <button 
                          onClick={() => startMatch(gameUnit)}
                          className="px-6 py-3 bg-indigo-600 text-white rounded-xl font-bold"
                        >
                          Jugar de nuevo
                        </button>
                      </div>
                    )}
                  </div>
                )}

                {/* --- 3. JUEGO MEMORY GAME --- */}
                {selectedGame === 'memory' && (
                  <div className="max-w-xl mx-auto space-y-6">
                    <div className="text-center">
                      <h3 className="text-xl font-extrabold">Memory Match: {gameUnit}</h3>
                      <p className="text-sm text-slate-500">Turnos completados: <span className="font-extrabold">{gameState.turns}</span></p>
                    </div>

                    {gameState.error ? (
                      <div className="p-6 bg-red-50 text-red-800 rounded-2xl text-center font-bold">
                        {gameState.error}
                      </div>
                    ) : !gameState.gameOver ? (
                      <div className="grid grid-cols-2 sm:grid-cols-4 gap-4">
                        {gameState.cards.map((card, idx) => {
                          const isFlipped = card.isFlipped || card.isMatched;
                          
                          return (
                            <button
                              key={card.id}
                              onClick={() => handleMemorySelect(idx)}
                              disabled={card.isMatched}
                              className={`h-28 rounded-2xl flex items-center justify-center text-center font-bold text-sm border-2 transition-all duration-300 ${
                                card.isMatched 
                                  ? 'bg-emerald-100 text-emerald-800 border-emerald-300 opacity-60 cursor-not-allowed' 
                                  : isFlipped 
                                    ? 'bg-indigo-600 text-white border-indigo-700' 
                                    : 'bg-indigo-50 text-indigo-700 border-indigo-200 hover:bg-indigo-100'
                              }`}
                            >
                              {isFlipped ? (
                                <span>{card.text}</span>
                              ) : (
                                <HelpCircle className="w-8 h-8 opacity-60" />
                              )}
                            </button>
                          );
                        })}
                      </div>
                    ) : (
                      <div className="bg-white dark:bg-slate-800 p-8 rounded-3xl text-center shadow-md space-y-4">
                        <CheckCircle className="w-16 h-16 text-indigo-500 mx-auto" />
                        <h4 className="text-2xl font-black">¡Memoria completada!</h4>
                        <p className="text-slate-500">Has resuelto todas las parejas en <span className="font-bold text-indigo-600">{gameState.turns} turnos</span>.</p>
                        <button 
                          onClick={() => startMemory(gameUnit)}
                          className="px-6 py-3 bg-indigo-600 text-white rounded-xl font-bold"
                        >
                          Volver a Jugar
                        </button>
                      </div>
                    )}
                  </div>
                )}

                {/* --- 4. JUEGO MULTIPLE CHOICE --- */}
                {selectedGame === 'choice' && (
                  <div className="max-w-xl mx-auto space-y-6">
                    <div className="text-center">
                      <h3 className="text-xl font-extrabold">Multiple Choice: {gameUnit}</h3>
                      <p className="text-sm text-slate-500">Pregunta {gameState.currentIndex + 1} de {gameState.questions?.length}</p>
                    </div>

                    {gameState.error ? (
                      <div className="p-6 bg-red-50 text-red-800 rounded-2xl text-center font-bold">
                        {gameState.error}
                      </div>
                    ) : !gameState.gameOver ? (
                      <div className="space-y-6">
                        {/* Pregunta */}
                        <div className="bg-white dark:bg-slate-800 p-8 rounded-3xl shadow-sm border border-slate-200 dark:border-slate-700 text-center">
                          <span className="text-xs uppercase font-extrabold text-indigo-500 tracking-wider">¿Cuál es el significado correcto?</span>
                          <h4 className="text-3xl font-black text-indigo-700 dark:text-indigo-400 mt-2">{gameState.questions[gameState.currentIndex]?.word}</h4>
                        </div>

                        {/* Opciones */}
                        <div className="grid grid-cols-1 gap-3">
                          {gameState.questions[gameState.currentIndex]?.options.map((option, idx) => {
                            const isAnswered = gameState.questions[gameState.currentIndex].userAnswer !== null;
                            const isSelected = gameState.questions[gameState.currentIndex].userAnswer === option;
                            const isCorrect = option === gameState.questions[gameState.currentIndex].correctAnswer;

                            return (
                              <button
                                key={idx}
                                disabled={isAnswered}
                                onClick={() => handleMultipleChoiceAnswer(option)}
                                className={`w-full text-left p-5 rounded-2xl border-2 font-bold text-base transition-all ${
                                  isAnswered 
                                    ? isCorrect 
                                      ? 'bg-emerald-100 text-emerald-800 border-emerald-400' 
                                      : isSelected 
                                        ? 'bg-red-100 text-red-800 border-red-400' 
                                        : 'bg-slate-100 text-slate-400 border-transparent'
                                    : 'bg-white dark:bg-slate-800 text-slate-800 dark:text-slate-100 border-slate-200 dark:border-slate-700 hover:border-indigo-400'
                                }`}
                              >
                                {option}
                              </button>
                            );
                          })}
                        </div>

                        {/* Control Siguiente */}
                        {gameState.showFeedback && (
                          <button
                            onClick={handleNextMultipleChoice}
                            className="w-full py-4 bg-indigo-600 hover:bg-indigo-700 text-white font-extrabold rounded-2xl text-sm"
                          >
                            Continuar
                          </button>
                        )}
                      </div>
                    ) : (
                      <div className="bg-white dark:bg-slate-800 p-8 rounded-3xl text-center shadow-md space-y-4">
                        <Award className="w-16 h-16 text-yellow-500 mx-auto" />
                        <h4 className="text-2xl font-black">¡Prueba Finalizada!</h4>
                        <p className="text-slate-500">Puntuación alcanzada: <span className="font-extrabold text-emerald-600">{gameState.score} puntos</span></p>
                        <button 
                          onClick={() => startMultipleChoice(gameUnit)}
                          className="px-6 py-3 bg-indigo-600 text-white rounded-xl font-bold"
                        >
                          Reiniciar Evaluación
                        </button>
                      </div>
                    )}
                  </div>
                )}

                {/* --- 5. JUEGO FILL IN THE GAP --- */}
                {selectedGame === 'gap' && (
                  <div className="max-w-xl mx-auto space-y-6">
                    <div className="text-center">
                      <h3 className="text-xl font-extrabold">Fill in the Gap: {gameUnit}</h3>
                      <p className="text-sm text-slate-500">Frase {gameState.currentIndex + 1} de {gameState.questions?.length}</p>
                    </div>

                    {gameState.error ? (
                      <div className="p-6 bg-red-50 text-red-800 rounded-2xl text-center font-bold">
                        {gameState.error}
                      </div>
                    ) : !gameState.gameOver ? (
                      <div className="space-y-6">
                        
                        {/* Frase incompleta */}
                        <div className="bg-white dark:bg-slate-800 p-8 rounded-3xl shadow-sm border border-slate-200 dark:border-slate-700 text-center">
                          <span className="text-xs uppercase font-extrabold text-indigo-500 tracking-wider">Completa la frase contextualizada:</span>
                          <blockquote className="text-2xl font-bold leading-relaxed text-slate-700 dark:text-slate-200 mt-4 italic">
                            "{gameState.questions[gameState.currentIndex]?.sentence}"
                          </blockquote>
                          <p className="text-sm text-slate-400 mt-2">Pista traducción: "{gameState.questions[gameState.currentIndex]?.translation}"</p>
                        </div>

                        {/* Opciones de respuesta */}
                        <div className="grid grid-cols-2 gap-3">
                          {gameState.questions[gameState.currentIndex]?.options.map((option, idx) => {
                            return (
                              <button
                                key={idx}
                                onClick={() => handleFillGapAnswer(option)}
                                className="p-4 rounded-xl bg-white dark:bg-slate-800 text-slate-800 dark:text-slate-100 border-2 border-slate-200 dark:border-slate-700 hover:border-indigo-500 font-bold transition-all text-sm"
                              >
                                {option}
                              </button>
                            );
                          })}
                        </div>
                      </div>
                    ) : (
                      <div className="bg-white dark:bg-slate-800 p-8 rounded-3xl text-center shadow-md space-y-4">
                        <CheckCircle className="w-16 h-16 text-indigo-500 mx-auto" />
                        <h4 className="text-2xl font-black">¡Huecos Completados!</h4>
                        <p className="text-slate-500">Has finalizado el ejercicio de gramática aplicada de la unidad.</p>
                        <button 
                          onClick={() => startFillGap(gameUnit)}
                          className="px-6 py-3 bg-indigo-600 text-white rounded-xl font-bold"
                        >
                          Practicar de nuevo
                        </button>
                      </div>
                    )}
                  </div>
                )}

                {/* --- 6. JUEGO SPELLING CHALLENGE --- */}
                {selectedGame === 'spelling' && (
                  <div className="max-w-xl mx-auto space-y-6">
                    <div className="text-center">
                      <h3 className="text-xl font-extrabold">Spelling Challenge: {gameUnit}</h3>
                      <p className="text-sm text-slate-500">Palabra {gameState.currentIndex + 1} de {gameState.words?.length}</p>
                    </div>

                    {gameState.error ? (
                      <div className="p-6 bg-red-50 text-red-800 rounded-2xl text-center font-bold">
                        {gameState.error}
                      </div>
                    ) : !gameState.gameOver ? (
                      <div className="space-y-6">
                        
                        <div className="bg-white dark:bg-slate-800 p-8 rounded-3xl shadow-sm border border-slate-200 dark:border-slate-700 text-center space-y-4">
                          <span className="text-xs uppercase font-extrabold text-indigo-500 tracking-wider block">Escucha con atención y escribe la palabra</span>
                          
                          <button
                            onClick={() => speakWord(gameState.words[gameState.currentIndex].word)}
                            className="mx-auto p-4 bg-indigo-100 text-indigo-700 rounded-full hover:bg-indigo-200 transition-colors flex items-center justify-center space-x-2"
                          >
                            <Volume2 className="w-8 h-8" />
                            <span className="font-extrabold text-sm pr-2">Reproducir Audio</span>
                          </button>

                          <p className="text-sm text-slate-500">Significado: <span className="font-bold text-slate-800 dark:text-slate-200">{gameState.words[gameState.currentIndex].translation}</span></p>
                        </div>

                        {/* Entrada del usuario */}
                        <form onSubmit={handleSpellingSubmit} className="space-y-4">
                          <input 
                            type="text"
                            placeholder="Escribe la palabra en inglés aquí..."
                            value={gameState.inputValue}
                            onChange={(e) => setGameState(prev => ({ ...prev, inputValue: e.target.value }))}
                            disabled={gameState.isCorrect !== null}
                            className="w-full p-4 rounded-2xl border-2 border-slate-300 dark:border-slate-700 dark:bg-slate-800 text-center text-xl font-bold uppercase tracking-wider outline-none focus:border-indigo-500"
                          />

                          {gameState.isCorrect === null ? (
                            <button
                              type="submit"
                              className="w-full py-4 bg-indigo-600 text-white font-extrabold rounded-2xl text-sm shadow-md"
                            >
                              Validar Deletreo
                            </button>
                          ) : (
                            <div className="space-y-4">
                              {gameState.isCorrect ? (
                                <div className="p-4 bg-emerald-50 border-2 border-emerald-300 text-emerald-800 rounded-2xl text-center font-bold">
                                  ¡Es Correcto! Excelente deletreo.
                                </div>
                              ) : (
                                <div className="p-4 bg-red-50 border-2 border-red-300 text-red-800 rounded-2xl text-center">
                                  <p className="font-bold">Incorrecto.</p>
                                  <p className="text-sm">La ortografía correcta es: <span className="font-extrabold uppercase text-indigo-600">{gameState.words[gameState.currentIndex].word}</span></p>
                                </div>
                              )}
                              <button
                                type="button"
                                onClick={handleNextSpelling}
                                className="w-full py-4 bg-indigo-600 text-white font-extrabold rounded-2xl text-sm"
                              >
                                Siguiente palabra
                              </button>
                            </div>
                          )}
                        </form>
                      </div>
                    ) : (
                      <div className="bg-white dark:bg-slate-800 p-8 rounded-3xl text-center shadow-md space-y-4">
                        <CheckCircle className="w-16 h-16 text-indigo-500 mx-auto" />
                        <h4 className="text-2xl font-black">Dictado Finalizado</h4>
                        <p className="text-slate-500 font-bold">Puntaje de ortografía: {gameState.score} puntos</p>
                        <button 
                          onClick={() => startSpelling(gameUnit)}
                          className="px-6 py-3 bg-indigo-600 text-white rounded-xl font-bold"
                        >
                          Volver a Intentar
                        </button>
                      </div>
                    )}
                  </div>
                )}

                {/* --- 7. JUEGO UNIT QUIZ --- */}
                {selectedGame === 'quiz' && (
                  <div className="max-w-xl mx-auto space-y-6">
                    <div className="text-center">
                      <h3 className="text-xl font-extrabold">Evaluación Completa: {gameUnit}</h3>
                      <p className="text-sm text-slate-500">Pregunta {gameState.currentIndex + 1} de {gameState.questions?.length}</p>
                    </div>

                    {gameState.error ? (
                      <div className="p-6 bg-red-50 text-red-800 rounded-2xl text-center font-bold">
                        {gameState.error}
                      </div>
                    ) : !gameState.gameOver ? (
                      <div className="space-y-6 animate-in fade-in">
                        
                        <div className="bg-white dark:bg-slate-800 p-6 rounded-3xl shadow-sm border-2 border-indigo-100 dark:border-slate-700">
                          <span className="text-xs uppercase font-extrabold px-2 py-1 rounded bg-indigo-100 text-indigo-800">
                            {gameState.questions[gameState.currentIndex]?.type === 'choice' ? 'Opción Múltiple' : 'Contexto'}
                          </span>
                          <h4 className="text-xl font-extrabold text-slate-800 dark:text-slate-100 mt-4 leading-relaxed">
                            {gameState.questions[gameState.currentIndex]?.title}
                          </h4>
                          {gameState.questions[gameState.currentIndex]?.text && (
                            <p className="text-lg font-bold italic text-indigo-600 mt-3">
                              "{gameState.questions[gameState.currentIndex]?.text}"
                            </p>
                          )}
                        </div>

                        {/* Opciones */}
                        <div className="grid grid-cols-1 gap-2.5">
                          {gameState.questions[gameState.currentIndex]?.options.map((opt, index) => (
                            <button
                              key={index}
                              onClick={() => handleQuizAnswer(opt)}
                              className="w-full text-left p-4 rounded-xl border-2 border-slate-200 hover:border-indigo-600 dark:bg-slate-800 text-slate-800 dark:text-slate-100 font-bold text-sm transition-all"
                            >
                              {opt}
                            </button>
                          ))}
                        </div>

                      </div>
                    ) : (
                      // Reporte final inteligente
                      <div className="bg-white dark:bg-slate-800 p-8 rounded-3xl shadow-md border border-slate-100 dark:border-slate-700 space-y-6">
                        <div className="text-center">
                          <Award className="w-16 h-16 text-yellow-400 mx-auto mb-2" />
                          <h4 className="text-2xl font-black">Reporte Final de la Unidad</h4>
                          <p className="text-slate-500">Aciertos conseguidos: <span className="font-extrabold text-indigo-600">{gameState.score} de {gameState.questions.length}</span></p>
                        </div>

                        {/* Recomendaciones adaptativas automatizadas */}
                        <div className="bg-indigo-50 dark:bg-slate-900 p-5 rounded-2xl border border-indigo-100 dark:border-slate-800">
                          <h5 className="font-extrabold text-sm uppercase text-indigo-800 dark:text-indigo-400 mb-2 flex items-center">
                            <Lightbulb className="w-5 h-5 mr-1.5" />
                            Consejo del Tutor Inclusivo:
                          </h5>
                          <p className="text-sm text-slate-700 dark:text-slate-300 font-medium">
                            {gameState.score === gameState.questions.length 
                              ? "¡Excelente dominio! Estás completamente consolidado con esta Unidad Didáctica. Puedes avanzar a importar nuevos documentos." 
                              : "Te recomendamos repasar los términos fallados con el juego de Flashcards o deletreo para reforzar la memoria ortográfica de esta unidad."}
                          </p>
                        </div>

                        {/* Historial de respuestas para aprendizaje visual rápido */}
                        <div className="space-y-2">
                          <h5 className="font-extrabold text-xs uppercase text-slate-400">Revisión de respuestas</h5>
                          {gameState.questions.map((q, idx) => (
                            <div key={idx} className="p-3 bg-slate-50 dark:bg-slate-900 rounded-xl flex items-center justify-between">
                              <span className="text-sm font-bold text-slate-700 dark:text-slate-200">{q.correct}</span>
                              <span className={`text-xs font-bold px-2 py-1 rounded ${
                                q.userAnswer === q.correct ? 'bg-emerald-100 text-emerald-800' : 'bg-red-100 text-red-800'
                              }`}>
                                {q.userAnswer === q.correct ? 'Correcta' : 'Errada'}
                              </span>
                            </div>
                          ))}
                        </div>

                        <button 
                          onClick={() => startUnitQuiz(gameUnit)}
                          className="w-full py-3.5 bg-indigo-600 text-white font-extrabold rounded-xl text-sm"
                        >
                          Intentar el Quiz Nuevamente
                        </button>
                      </div>
                    )}
                  </div>
                )}

              </div>
            )}

          </div>
        )}

        {/* ==================================== */}
        {/* PANTALLA 5: IMPORTAR VOCABULARIO */}
        {/* ==================================== */}
        {currentView === 'import' && (
          <div className="space-y-6 animate-in fade-in duration-300 max-w-3xl mx-auto">
            <div>
              <h2 className="text-2xl font-extrabold text-slate-800 dark:text-slate-100">Ingestor Inteligente de Vocabulario</h2>
              <p className="text-slate-500 dark:text-slate-400">Pega texto estructurado o apuntes de clase para extraer palabras automáticamente eliminando duplicados.</p>
            </div>

            <div className="bg-white dark:bg-slate-800 rounded-3xl p-6 shadow-sm border border-slate-100 dark:border-slate-700 space-y-6">
              
              <div>
                <label className="block text-sm font-bold text-slate-700 dark:text-slate-200 mb-2">
                  Escribe o copia tu glosario de estudio aquí:
                </label>
                <textarea 
                  value={importText}
                  onChange={(e) => setImportText(e.target.value)}
                  placeholder="Ejemplo de estructura de apuntes:&#10;Incredible - Increíble&#10;Adventure - Aventura&#10;Resilient - Resiliente"
                  rows={6}
                  className="w-full p-4 rounded-2xl border-2 border-slate-200 dark:border-slate-700 dark:bg-slate-900 font-mono text-sm focus:border-indigo-500 outline-none transition-all"
                />
              </div>

              {/* Ajustes de importación */}
              <div className="grid grid-cols-1 sm:grid-cols-2 gap-4">
                <div>
                  <label className="block text-xs font-bold uppercase text-slate-400 mb-1.5">Asociar a la unidad:</label>
                  <select
                    value={selectedUnit}
                    onChange={(e) => setSelectedUnit(e.target.value)}
                    className="w-full p-3 rounded-xl border border-slate-200 dark:border-slate-700 dark:bg-slate-900 text-sm font-bold"
                  >
                    <option value="Unit 1">Unit 1</option>
                    <option value="Unit 2">Unit 2</option>
                    <option value="Unit 3">Unit 3</option>
                    <option value="Unit 4">Unit 4</option>
                    <option value="Unit 5">Unit 5 (New)</option>
                  </select>
                </div>

                <div className="flex items-end">
                  <button
                    onClick={handleSimulateImport}
                    disabled={isParsing || !importText.trim()}
                    className="w-full py-3 px-4 bg-indigo-600 hover:bg-indigo-700 text-white font-extrabold rounded-xl text-sm flex items-center justify-center space-x-2 shadow-md disabled:opacity-50"
                  >
                    {isParsing ? (
                      <>
                        <RotateCcw className="w-5 h-5 animate-spin" />
                        <span>Analizando Documento...</span>
                      </>
                    ) : (
                      <>
                        <Upload className="w-5 h-5" />
                        <span>Escanear y Analizar</span>
                      </>
                    )}
                  </button>
                </div>
              </div>

              {/* Status de Importación */}
              {importStatus === 'preview' && (
                <div className="space-y-4 border-t border-slate-100 dark:border-slate-700 pt-6">
                  <div className="flex justify-between items-center">
                    <h4 className="font-extrabold text-base text-slate-800 dark:text-slate-100">Vista previa del vocabulario detectado:</h4>
                    <span className="text-xs font-extrabold bg-indigo-100 text-indigo-800 px-2.5 py-1 rounded-full">
                      {importedWords.length} palabras encontradas
                    </span>
                  </div>

                  <div className="max-h-60 overflow-y-auto border border-slate-100 dark:border-slate-700 rounded-2xl">
                    <table className="w-full text-left text-sm">
                      <thead className="bg-slate-50 dark:bg-slate-900 text-xs font-bold text-slate-500 sticky top-0">
                        <tr>
                          <th className="p-3">Inglés</th>
                          <th className="p-3">Traducción sugerida</th>
                          <th className="p-3">Categoría</th>
                          <th className="p-3">Unidad</th>
                        </tr>
                      </thead>
                      <tbody>
                        {importedWords.map((item, idx) => (
                          <tr key={idx} className="border-b border-slate-100 dark:border-slate-800">
                            <td className="p-3 font-extrabold text-indigo-600">{item.word}</td>
                            <td className="p-3 text-slate-600 dark:text-slate-300">{item.translation}</td>
                            <td className="p-3">
                              <span className="text-xs font-semibold px-2 py-0.5 rounded bg-slate-100">
                                {item.grammar_type}
                              </span>
                            </td>
                            <td className="p-3 text-slate-500">{item.unit}</td>
                          </tr>
                        ))}
                      </tbody>
                    </table>
                  </div>

                  <div className="flex space-x-3 pt-2">
                    <button
                      onClick={confirmImport}
                      className="flex-1 py-3 bg-emerald-600 hover:bg-emerald-700 text-white font-extrabold rounded-xl text-sm"
                    >
                      Confirmar Ingesta en Glosario
                    </button>
                    <button
                      onClick={() => {
                        setImportStatus(null);
                        setImportedWords([]);
                      }}
                      className="px-6 py-3 bg-slate-100 hover:bg-slate-200 text-slate-700 font-extrabold rounded-xl text-sm"
                    >
                      Cancelar
                    </button>
                  </div>
                </div>
              )}

              {importStatus === 'success' && (
                <div className="p-5 bg-emerald-50 border-2 border-emerald-300 text-emerald-800 rounded-3xl flex items-center space-x-3">
                  <CheckCircle className="w-8 h-8 text-emerald-600 shrink-0" />
                  <div>
                    <h5 className="font-extrabold text-base">¡Importación Exitosa!</h5>
                    <p className="text-xs text-emerald-700 font-medium">La base de datos del glosario se ha actualizado de forma segura evitando solapamientos y duplicados de vocabulario.</p>
                  </div>
                </div>
              )}

            </div>
          </div>
        )}

      </main>

      {/* --- PIE DE PÁGINA ACCESIBLE --- */}
      <footer className="border-t border-slate-200 dark:border-slate-800 bg-white dark:bg-slate-900 mt-12 py-8 transition-colors">
        <div className="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8 text-center space-y-4">
          <p className="text-sm font-semibold text-slate-500 dark:text-slate-400 leading-relaxed">
            English Vocabulary Hub de diseño abierto y código limpio. Creado con ❤️ siguiendo metodologías de accesibilidad cognitiva para la reducción del estrés en estudiantes neurodiversos.
          </p>
          <div className="flex justify-center space-x-6 text-xs font-bold text-indigo-600 dark:text-indigo-400">
            <span>Guía DUA Aplicada</span>
            <span>•</span>
            <span>Regulaciones de Accesibilidad WCAG 2.1AA</span>
            <span>•</span>
            <span>Atención a la Neurodiversidad</span>
          </div>
        </div>
      </footer>
    </div>
  );
}