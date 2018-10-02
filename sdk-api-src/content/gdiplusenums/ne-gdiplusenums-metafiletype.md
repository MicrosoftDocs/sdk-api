---
UID: NE:gdiplusenums.MetafileType
title: MetafileType
author: windows-sdk-content
description: The MetafileType enumeration specifies types of metafiles. The MetafileHeader::GetType method returns an element of this enumeration.
old-location: gdiplus\_gdiplus_ENUM_MetafileType.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\enumerations\metafiletype.htm
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: MetafileType, MetafileType enumeration [GDI+], MetafileTypeEmf, MetafileTypeEmfPlusDual, MetafileTypeEmfPlusOnly, MetafileTypeInvalid, MetafileTypeWmf, MetafileTypeWmfPlaceable, _gdiplus_ENUM_MetafileType, gdiplus._gdiplus_ENUM_MetafileType, gdiplusenums/MetafileType, gdiplusenums/MetafileTypeEmf, gdiplusenums/MetafileTypeEmfPlusDual, gdiplusenums/MetafileTypeEmfPlusOnly, gdiplusenums/MetafileTypeInvalid, gdiplusenums/MetafileTypeWmf, gdiplusenums/MetafileTypeWmfPlaceable
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Gdiplusenums.h
api_name:
 - MetafileType
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
req.product: GDI+ 1.0
---

# MetafileType enumeration


## -description


The <b>MetafileType</b> enumeration specifies types of metafiles. The 
			<a href="https://msdn.microsoft.com/42acdd2c-b87d-455a-83c0-0630bd552c45">MetafileHeader::GetType</a> method returns an element of this enumeration.


## -enum-fields




### -field MetafileTypeInvalid

Specifies a metafile format that is not recognized in GDI+. 


### -field MetafileTypeWmf

Specifies a WMF file. Such a file contains only GDI records. 


### -field MetafileTypeWmfPlaceable

Specifies a WMF file that has a placeable metafile header in front of it. 


### -field MetafileTypeEmf

Specifies an EMF file. Such a file contains only GDI records. 


### -field MetafileTypeEmfPlusOnly

Specifies an EMF+ file. Such a file contains only GDI+ records and must be displayed by using GDI+. Displaying the records using GDI may cause unpredictable results. 


### -field MetafileTypeEmfPlusDual

Specifies an EMF+ Dual file. Such a file contains GDI+ records along with alternative GDI records and can be displayed by using either GDI or GDI+. Displaying the records using GDI may cause some quality degradation. 


## -see-also




<a href="https://msdn.microsoft.com/42acdd2c-b87d-455a-83c0-0630bd552c45">MetafileHeader::GetType</a>
 

 

