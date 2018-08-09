---
UID: NE:gdiplusenums.StringTrimming
title: StringTrimming
author: windows-sdk-content
description: The StringTrimming enumeration specifies how to trim characters from a string so that the string fits into a layout rectangle. The layout rectangle is used to position and size the display string.
old-location: gdiplus\_gdiplus_ENUM_StringTrimming.htm
old-project: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\enumerations\stringtrimming.htm
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: StringTrimming, StringTrimming enumeration [GDI+], StringTrimmingCharacter, StringTrimmingEllipsisCharacter, StringTrimmingEllipsisPath, StringTrimmingEllipsisWord, StringTrimmingNone, StringTrimmingWord, _gdiplus_ENUM_StringTrimming, gdiplus._gdiplus_ENUM_StringTrimming, gdiplusenums/StringTrimming, gdiplusenums/StringTrimmingCharacter, gdiplusenums/StringTrimmingEllipsisCharacter, gdiplusenums/StringTrimmingEllipsisPath, gdiplusenums/StringTrimmingEllipsisWord, gdiplusenums/StringTrimmingNone, gdiplusenums/StringTrimmingWord
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Gdiplusenums.h
api_name:
 - StringTrimming
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




<a href="https://msdn.microsoft.com/en-us/library/ms535759(v=VS.85).aspx">DrawString Methods</a>



<a href="https://msdn.microsoft.com/en-us/library/ms533823(v=VS.85).aspx">Formatting Text</a>



<a href="https://msdn.microsoft.com/en-us/library/ms535787(v=VS.85).aspx">MeasureString Methods</a>



<a href="https://msdn.microsoft.com/en-us/library/ms534177(v=VS.85).aspx">StringAlignment</a>



<a href="https://msdn.microsoft.com/en-us/library/ms534179(v=VS.85).aspx">StringDigitSubstitute</a>



<a href="https://msdn.microsoft.com/en-us/library/ms534731(v=VS.85).aspx">StringFormat::SetTrimming</a>



<a href="https://msdn.microsoft.com/en-us/library/ms534181(v=VS.85).aspx">StringFormatFlags</a>
 

 

