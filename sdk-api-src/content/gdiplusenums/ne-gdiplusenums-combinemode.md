---
UID: NE:gdiplusenums.CombineMode
title: CombineMode
author: windows-sdk-content
description: The CombineMode enumeration specifies how a new region is combined with an existing region.
old-location: gdiplus\_gdiplus_ENUM_CombineMode.htm
old-project: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\enumerations\combinemode.htm
ms.author: windowssdkdev
ms.date: 05/24/2018
ms.keywords: CombineMode, CombineMode enumeration [GDI+], CombineModeComplement, CombineModeExclude, CombineModeIntersect, CombineModeReplace, CombineModeUnion, CombineModeXor, _gdiplus_ENUM_CombineMode, gdiplus._gdiplus_ENUM_CombineMode, gdiplusenums/CombineMode, gdiplusenums/CombineModeComplement, gdiplusenums/CombineModeExclude, gdiplusenums/CombineModeIntersect, gdiplusenums/CombineModeReplace, gdiplusenums/CombineModeUnion, gdiplusenums/CombineModeXor
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
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Gdiplusenums.h
api_name:
-	CombineMode
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.0
---

# CombineMode enumeration


## -description


The <b>CombineMode</b> enumeration specifies how a new region is combined with an existing region.


## -enum-fields




### -field CombineModeReplace

Specifies that the existing region is replaced by the new region. 


### -field CombineModeIntersect

Specifies that the existing region is replaced by the intersection of itself and the new region. 


### -field CombineModeUnion

Specifies that the existing region is replaced by the union of itself and the new region. 


### -field CombineModeXor

Specifies that the existing region is replaced by the result of performing an 
				<b>XOR</b> on the two regions. A point is in the 
				<b>XOR</b> of two regions if it is in one region or the other but not in both regions. 


### -field CombineModeExclude

Specifies that the existing region is replaced by the portion of itself that is outside of the new region. 


### -field CombineModeComplement

Specifies that the existing region is replaced by the portion of the new region that is outside of the existing region. 

