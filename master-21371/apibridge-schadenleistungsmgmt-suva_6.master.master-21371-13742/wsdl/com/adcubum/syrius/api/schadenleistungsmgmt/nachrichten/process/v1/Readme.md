#Übersicht
Der UvgKtgNachrichtenService ist angelehnt an eine `DialogMessage` aus dem [Leistungsstandard-CH (KLE) von Swissdec](https://www.swissdec.ch/de/releases-und-updates/richtlinien-kle/).

#Schemaanpassungen zu KLE
| KLE | Adcubum | Begründung |
|-----|---------|------------|
| `DialogMessageType` erweitert `StoryBaseType` | Vererbung entfernt | Wir brauchen diese Abstraktion nicht, wir haben nur eine Konkretisierung. |
| `DialogMessageType` | umbenannt zu `WsNachrichtType` | #1, #2 |
| `DialogMessageType.Creation` | umbenannt zu `WsNachrichtType.erstellung` | #1 |
| `DialogMessageType.StoryID` | umbenannt zu `WsNachrichtType.nachrichtId` | #1 |
| `DialogMessageType.Previous` | umbenannt zu `WsNachrichtType.vorherigeNachrichtId` | #1 |
| `DialogMessageType.Title` | umbenannt zu `WsNachrichtType.titel` | #1 |
| `DialogMessageType.Paragraph` | umbenannt zu `WsNachrichtType.absatz` | #1 |
| nicht vorhanden | `WsNachrichtType.dokumentId` eigefügt | Um diese Nachricht im Archiv zu referenzieren. |
| `DialogMessageType.StandardDialogID` | nicht vorhanden | #3 |
| `DialogMessageType.Description` | nicht vorhanden | #3 |
| `DialogMessageType.Section` | nicht vorhanden | #3 |
| `PreviousType` | nicht vorhanden | #3 |
| `ParagraphType` | umbenannt zu `WsAbsatzType` | #1, #2 |
| `ParagraphType.ID` | umbenannt zu `reihenfolge` | #1; Die Id wird verwendet um die Reihenfolge aufsteigend zu sortieren. |
| `ParagraphType.Label` | umbenannt zu `WsAbsatzType.text` | #1 |
| `ParagraphType.Value` | nicht vorhanden | #3 |
| `ParagraphType.Answer` | nicht vorhanden | #3 |
| `ParagraphType.sectionIDRef` | nicht vorhanden | #3 |
| `ParagraphValueType` | nicht vorhanden | #3 |
| `ParagraphAnswerType` | nicht vorhanden | #3 |
| `Answer*Type` | nicht vorhanden | #3 |
| `AnswerYesNoUnknownType` | nicht vorhanden | #3 |
| `SectionType` | nicht vorhanden | #3 |
| `YesNoUnknownType` | nicht vorhanden | #3 |
| `EmptySimpleType` | nicht vorhanden | #3 |
| `NotEmptyStringType` | nicht vorhanden | #3 |
| `IdType` | umbenannt zu `WsKurzerStringType` | #1, #2 |

#### Begründungen
| # |   |
|---|---|
| 1 | Unsere Schnittstellen sind grundsätzlich auf Deutsch. |
| 2 | Unsere Schnittstellen-Typen beginnen grundsätzlich mit `Ws`. |
| 3 | Für `SimpleMessage`-Nachrichten nicht benötigt. |
