---
UID: NF:dwrite_3.IDWriteFontFace3.IsCharacterLocal
title: IDWriteFontFace3::IsCharacterLocal
author: windows-sdk-content
description: Determines whether the character is locally downloaded from the font.
old-location: directwrite\idwritefontface3_ischaracterlocal.htm
old-project: DirectWrite
ms.assetid: 7a47f73b-9ce7-f7db-688b-291cebad54bb
ms.author: windowssdkdev
ms.date: 08/24/2018
ms.keywords: IDWriteFontFace3 interface [Direct Write],IsCharacterLocal method, IDWriteFontFace3.IsCharacterLocal, IDWriteFontFace3::IsCharacterLocal, IsCharacterLocal, IsCharacterLocal method [Direct Write], IsCharacterLocal method [Direct Write],IDWriteFontFace3 interface, directwrite.idwritefontface3_ischaracterlocal, dwrite_3/IDWriteFontFace3::IsCharacterLocal
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: dwrite_3.h
req.include-header: 
req.redist: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10 [desktop apps only]
req.target-min-winversvr: Windows Server 2016 [desktop apps only]
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
 - COM
api_location:
 - dwrite.dll
api_name:
 - IDWriteFontFace3.IsCharacterLocal
product: Windows
targetos: Windows
req.lib: Dwrite.lib
req.dll: Dwrite.dll
req.irql: 
req.product: Windows Media Format 9 Series or later
---

# IDWriteFontFace3::IsCharacterLocal


## -description


Determines whether the character is locally downloaded from the font.


## -parameters




### -param unicodeValue [in]

Type: <b>UINT32</b>

A Unicode (UCS-4) character value.


## -returns



Type: <b>BOOL</b>

Returns <b>TRUE</b> if the font has the specified character locally available,    
  <b>FALSE</b> if not or if the font does not support that character. 




## -see-also




<a href="https://msdn.microsoft.com/1081A005-E4A8-4EE0-AFE0-10BD8D8471DF">IDWriteFontFace3</a>
 

 

