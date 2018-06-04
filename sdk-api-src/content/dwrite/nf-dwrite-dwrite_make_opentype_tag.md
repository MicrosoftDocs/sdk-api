---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# DWRITE_MAKE_OPENTYPE_TAG macro


## -description


 Creates an OpenType tag as a 32-bit integer, such that
 the first character in the tag is the lowest byte
 (least significant on little endian architectures),
 which can be used to compare with tags in the font file.
 This macro is compatible with <a href="https://msdn.microsoft.com/31f0d1b5-36f2-4bde-b39c-b1392f9d925f">DWRITE_FONT_FEATURE_TAG</a>.


## -parameters




### -param a

Type: <b>char</b>

The first character in the tag.


### -param b

Type: <b>char</b>

The second character in the tag.


### -param c

Type: <b>char</b>

The third character in the tag.


### -param d

Type: <b>char</b>

The fourth character in the tag.


## -remarks



<div class="alert"><b>Note</b>  The OpenType language (such as "ROM ", "URD ", and "FAR " for Romanian, Urdu, and Persian) are determined from the locale, and the script ("latn" and "arab" for Latin and Arabic) is determined from the script analyzer. That's why these are not listed under OpenType tags, only the feature tags</div>
<div> </div>

#### Examples

Example: <b>DWRITE_MAKE_OPENTYPE_TAG</b>('c','c','m','p')
 

Dword:   0x706D6363

<div class="code"></div>


