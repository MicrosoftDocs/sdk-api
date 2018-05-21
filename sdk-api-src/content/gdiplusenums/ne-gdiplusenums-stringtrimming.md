---
UID: NE:gdiplusenums.StringTrimming
title: StringTrimming
author: windows-driver-content
description: The StringTrimming enumeration specifies how to trim characters from a string so that the string fits into a layout rectangle. The layout rectangle is used to position and size the display string.
old-location: gdiplus\_gdiplus_ENUM_StringTrimming.htm
old-project: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\enumerations\stringtrimming.htm
ms.author: windowsdriverdev
ms.date: 5/14/2018
ms.keywords: StringTrimming, StringTrimming enumeration [GDI+], StringTrimmingCharacter, StringTrimmingEllipsisCharacter, StringTrimmingEllipsisPath, StringTrimmingEllipsisWord, StringTrimmingNone, StringTrimmingWord, _gdiplus_ENUM_StringTrimming, gdiplus._gdiplus_ENUM_StringTrimming, gdiplusenums/StringTrimming, gdiplusenums/StringTrimmingCharacter, gdiplusenums/StringTrimmingEllipsisCharacter, gdiplusenums/StringTrimmingEllipsisPath, gdiplusenums/StringTrimmingEllipsisWord, gdiplusenums/StringTrimmingNone, gdiplusenums/StringTrimmingWord
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: enum
req.header: gdiplusenums.h
req.include-header: Gdiplus.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP, Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: 
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Gdiplusenums.h
api_name:
-	StringTrimming
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.0
---

# StringTrimming enumeration


## -description


The <b>StringTrimming</b> enumeration specifies how to trim characters from a string so that the string fits into a layout rectangle. The layout rectangle is used to position and size the display string.


## -enum-fields




### -field StringTrimmingNone

Specifies that no trimming is done. 


### -field StringTrimmingCharacter

Specifies that the string is broken at the boundary of the last character that is inside the layout rectangle. This is the default. 


### -field StringTrimmingWord

Specifies that the string is broken at the boundary of the last word that is inside the layout rectangle. 


### -field StringTrimmingEllipsisCharacter

Specifies that the string is broken at the boundary of the last character that is inside the layout rectangle and an ellipsis (...) is inserted after the character. 


### -field StringTrimmingEllipsisWord

Specifies that the string is broken at the boundary of the last word that is inside the layout rectangle and an ellipsis (...) is inserted after the word. 


### -field StringTrimmingEllipsisPath

Specifies that the center is removed from the string and replaced by an ellipsis. The algorithm keeps as much of the last portion of the string as possible. 


## -remarks



Trimming affects only the last visible or partly visible (due to clipping) line of text.




## -see-also




<a href="https://msdn.microsoft.com/b3568ed9-e359-4916-a83d-7553c021d197">DrawString Methods</a>



<a href="https://msdn.microsoft.com/4014a602-88f6-4fac-b4b2-3dafdcff8f33">Formatting Text</a>



<a href="https://msdn.microsoft.com/947c3080-1035-4dfe-aa7d-f73753a568cf">MeasureString Methods</a>



<a href="https://msdn.microsoft.com/d395f6b4-8d8a-41b1-9c49-6fc2f005ca5d">StringAlignment</a>



<a href="https://msdn.microsoft.com/b61e9a88-2b00-43f5-bc8d-1d6b4d6ecb19">StringDigitSubstitute</a>



<a href="https://msdn.microsoft.com/a5966441-e295-41e5-85eb-189ec3831c31">StringFormat::SetTrimming</a>



<a href="https://msdn.microsoft.com/9bbddab0-46b1-49db-86c1-cf9086692958">StringFormatFlags</a>
 

 

