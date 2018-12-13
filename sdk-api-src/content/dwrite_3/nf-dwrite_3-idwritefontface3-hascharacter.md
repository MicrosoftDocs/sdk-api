---
UID: NF:dwrite_3.IDWriteFontFace3.HasCharacter
title: IDWriteFontFace3::HasCharacter
author: windows-sdk-content
description: Determines whether the font supports the specified character.
old-location: directwrite\idwritefontface3_hascharacter.htm
tech.root: DirectWrite
ms.assetid: BCBC382E-C599-429A-9E00-EAB12D675503
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: HasCharacter, HasCharacter method [Direct Write], HasCharacter method [Direct Write],IDWriteFontFace3 interface, IDWriteFontFace3 interface [Direct Write],HasCharacter method, IDWriteFontFace3.HasCharacter, IDWriteFontFace3::HasCharacter, directwrite.idwritefontface3_hascharacter, dwrite_3/IDWriteFontFace3::HasCharacter
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: dwrite_3.h
req.include-header: 
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
req.lib: Dwrite.lib
req.dll: Dwrite.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - dwrite.dll
api_name:
 - IDWriteFontFace3.HasCharacter
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDWriteFontFace3::HasCharacter


## -description


Determines whether the font supports the specified character.


## -parameters




### -param unicodeValue [in]

Type: <b>UINT32</b>

A Unicode (UCS-4) character value.


## -returns



Type: <b>BOOL</b>

Returns whether the font supports the specified character. Returns <b>TRUE</b> if the font has the specified character; otherwise, <b>FALSE</b>.






## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Dn894561(v=VS.85).aspx">IDWriteFontFace3</a>
 

 

