---
UID: NS:wingdi.tagDIBSECTION
title: tagDIBSECTION
author: windows-sdk-content
description: The DIBSECTION structure contains information about a DIB created by calling the CreateDIBSection function.
old-location: gdi\dibsection.htm
tech.root: gdi
ms.assetid: 76e84c90-6553-46c6-9ab9-afa022e0b2e5
ms.author: windowssdkdev
ms.date: 10/10/2018
ms.keywords: "*LPDIBSECTION, *PDIBSECTION, DIBSECTION, DIBSECTION structure [Windows GDI], PDIBSECTION, PDIBSECTION structure pointer [Windows GDI], _win32_DIBSECTION_str, gdi.dibsection, tagDIBSECTION, wingdi/DIBSECTION, wingdi/PDIBSECTION"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: wingdi.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
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
 - Wingdi.h
api_name:
 - DIBSECTION
product: Windows
targetos: Windows
req.typenames: DIBSECTION, *LPDIBSECTION, *PDIBSECTION
req.redist: 
---

# tagDIBSECTION structure


## -description



The <b>DIBSECTION</b> structure contains information about a DIB created by calling the <a href="https://msdn.microsoft.com/9276ec84-2860-42be-a9f8-d4efb8d25eec">CreateDIBSection</a> function. A <b>DIBSECTION</b> structure includes information about the bitmap's dimensions, color format, color masks, optional file mapping object, and optional bit values storage offset. An application can obtain a filled-in <b>DIBSECTION</b> structure for a given DIB by calling the <a href="https://msdn.microsoft.com/555ab876-d990-426d-915c-f98df82a10aa">GetObject</a> function.




## -struct-fields




### -field dsBm

A <a href="https://msdn.microsoft.com/6ee382da-dd63-442b-80c3-59472defb41f">BITMAP</a> data structure that contains information about the DIB: its type, its dimensions, its color capacities, and a pointer to its bit values.


### -field dsBmih

A <a href="https://msdn.microsoft.com/02f8ed65-8fed-4dda-9b94-7343a0cfa8c1">BITMAPINFOHEADER</a> structure that contains information about the color format of the DIB.


### -field dsBitfields

Specifies three color masks for the DIB. This field is only valid when the <b>BitCount</b> member of the <a href="https://msdn.microsoft.com/02f8ed65-8fed-4dda-9b94-7343a0cfa8c1">BITMAPINFOHEADER</a> structure has a value greater than 8. Each color mask indicates the bits that are used to encode one of the three color channels (red, green, and blue).


### -field dshSection

Contains a handle to the file mapping object that the <a href="https://msdn.microsoft.com/9276ec84-2860-42be-a9f8-d4efb8d25eec">CreateDIBSection</a> function used to create the DIB. 
			 If <b>CreateDIBSection</b> was called with a <b>NULL</b> value for its <i>hSection</i> parameter, 
			 causing the system to allocate memory for the bitmap, the <i>dshSection</i> member will be <b>NULL</b>.


### -field dsOffset

The offset to the bitmap's bit values within the file mapping object referenced by <i>dshSection</i>. 
			 If <i>dshSection</i> is <b>NULL</b>, the <i>dsOffset</i> value has no meaning.


## -see-also




<a href="https://msdn.microsoft.com/6ee382da-dd63-442b-80c3-59472defb41f">BITMAP</a>



<a href="https://msdn.microsoft.com/02f8ed65-8fed-4dda-9b94-7343a0cfa8c1">BITMAPINFOHEADER</a>



<a href="https://msdn.microsoft.com/29f8237f-9c7e-41a7-90b1-5f048fcc74a6">Bitmap Structures</a>



<a href="https://msdn.microsoft.com/ff0a5ae3-ae2e-4417-b5e5-0f9871c03964">Bitmaps Overview</a>



<a href="https://msdn.microsoft.com/9276ec84-2860-42be-a9f8-d4efb8d25eec">CreateDIBSection</a>



<a href="https://msdn.microsoft.com/3e3319be-8a3d-4ac2-ba36-9dbf18243472">GetDIBColorTable</a>



<a href="https://msdn.microsoft.com/555ab876-d990-426d-915c-f98df82a10aa">GetObject</a>
 

 

