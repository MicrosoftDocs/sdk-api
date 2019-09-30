---
UID: NF:dwrite_3.IDWriteFontFace5.Equals
title: IDWriteFontFace5::Equals
author: windows-sdk-content
description: Performs an equality comparison between the font face object on which **Equals** is being called and the font face object passed as a parameter.
tech.root: DirectWrite
ms.author: windowssdkdev
ms.date: 09/10/2019
ms.keywords: IDWriteFontFace5 interface [Direct Write],Equals method, IDWriteFontFace5.Equals, IDWriteFontFace5::Equals, Equals, Equals method [Direct Write], Equals method [Direct Write],IDWriteFontFace5 interface, directwrite.idwritefontface5_equals, dwrite_3/IDWriteFontFace5::Equals
ms.topic: method
f1_keywords: 
 - "dwrite_3/IDWriteFontFace5.Equals"
req.construct-type: function
req.header: dwrite_3.h
req.include-header: 
req.target-type: Windows
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
req.lib: Dwrite.lib
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Dwrite.lib
 - Dwrite.dll
api_name:
 - IDWriteFontFace5::Equals
targetos: Windows
req.typenames: 
req.redist: 
---

## -description

Performs an equality comparison between the font face object on which **Equals** is being called and the font face object passed as a parameter.

## -parameters

### -param fontFace

Type: **[IDWriteFontFace](/windows/win32/api/dwrite/nn-dwrite-idwritefontface)\***

A pointer to a font face object to compare with the font face object on which **Equals** is being called.

## -returns

Type: **[BOOL](/windows/win32/winprog/windows-data-types)**

`true` if the font face objects are equal. Otherwise, `false`.

## -remarks

## -see-also

[IDWriteFontFace](/windows/win32/api/dwrite/nn-dwrite-idwritefontface)