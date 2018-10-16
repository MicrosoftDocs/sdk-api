---
UID: NE:gdiplusenums.EmfType
title: EmfType
author: windows-sdk-content
description: The EmfType enumeration specifies the nature of the records that are placed in an Enhanced Metafile (EMF) file. This enumeration is used by several constructors in the Metafile class.
old-location: gdiplus\_gdiplus_ENUM_EmfType.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\enumerations\emftype.htm
ms.author: windowssdkdev
ms.date: 10/09/2018
ms.keywords: EmfType, EmfType enumeration [GDI+], EmfTypeEmfOnly, EmfTypeEmfPlusDual, EmfTypeEmfPlusOnly, _gdiplus_ENUM_EmfType, gdiplus._gdiplus_ENUM_EmfType, gdiplusenums/EmfType, gdiplusenums/EmfTypeEmfOnly, gdiplusenums/EmfTypeEmfPlusDual, gdiplusenums/EmfTypeEmfPlusOnly
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
 - EmfType
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
req.product: GDI+ 1.0
---

# EmfType enumeration


## -description


The <b>EmfType</b> enumeration specifies the nature of the records that are placed in an Enhanced Metafile (EMF) file. This enumeration is used by several constructors in the 
			<a href="https://msdn.microsoft.com/63b057de-9c4d-488e-ad07-ede52f9175a6">Metafile</a> class.


## -enum-fields




### -field EmfTypeEmfOnly

Specifies that all of the records in the metafile are EMF records, which can be displayed by GDI or GDI+. 


### -field EmfTypeEmfPlusOnly

Specifies that all of the records in the metafile are EMF+ records, which can be displayed by GDI+ but not by GDI. 


### -field EmfTypeEmfPlusDual

Specifies that all EMF+ records in the metafile are associated with an alternate EMF record. Metafiles of type EmfTypeEmfPlusDual can be displayed by GDI or by GDI+. 


## -see-also




<a href="https://msdn.microsoft.com/a9648287-65d9-47d8-b32b-33f74b4fcd07">Metafile Constructors</a>
 

 

