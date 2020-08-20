Para criar uma nova quest/npc
deve-se adicionar um novo arquivo de texto
com a extensão '.c'

A sintaxe é a seguinte

QUEST* : Define um parametro da quest.
	*: indica o número da quest
	O limite de quests é de 1 à 45.
	Exemplo: QUEST1 NAME QuestNpc

Parametros:

NAME n : Define o nome do npc da quest
	n: indica o nome do npc
	O Arquivo do npc precisa estar
	na pasta quest.

POSITION x y : Define a posição que o npc será criado.

BASE_SPEECH s: Define uma mensagem que o npc falará de
	tempos em tempos.

	Todas as CONDITION e REWARD, para usar você define um index para cada uma
	EX, para adicionar duas conditions, uma é uma fala, a outra é um requerimento
	de level:
		CONDITION-1 SPEECH Oi
		CONDITION-2 LEVEL 300 400
	O mesmo para as REWARD.
		REWARD-1 GIVEGOLD 1000
		REWARD-2 GIVEEXP 1000
		
CONDITION
	SPEECH
	LEVEL
	ITEM
	ITEMSANC
	CONNAME
	GOLDCHECK
	ISLOG
	TIMECHECK
	EQITEM
	CHECKBIT
	CHECKCLASS
	CHECKSTAT
	NOTEQUIP	EXEMPLO: NOTEQUIP 3 999 = NÃO PODE ESTAR EQUIPADO O ITEM 999 NO SLOT 3 ( NAO TESTEI )
	ISTRANS		EXEMPLO: ISTRANS 0 = SÓ ENTRA MORTAIS, ISTRANS 1 = SÓ ENTRA ARCH

REWARD-
	SPEECH - Fala que o npc vai falar como recompensa
	ITEM - Item que o npc vai dar como recompensa
	LEVEL - Quantos leveis o npc vai dar como recompensa
	DELETEITEM - Qual item será deletado ao concluir o evento
	EQUIP - Qual item será equipado? (Precisa testar)
	SKILL - Qual skill será ganha? (Precisa testar)
	QITEM - Sei lá, precisa descobrir
	GIVEGOLD - Quanto de gold será adicionado ao player
	GIVEEXP - Quanto de exp será adicionado ao player
	TELEPORT - Posição que o player será teleportado
	EQDELETE - Precisa descobrir, talvez deleta algo que esteja equipado
	SETBIT - Precisa descobrir
	RESTAT - Reseta os stats? Precisa testar
	RESTATALL - Reseta stats e skills? Precisa testar
