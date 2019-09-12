---
UID: NF:dwrite_1.IDWriteTextLayout1.SetCharacterSpacing
title: IDWriteTextLayout1::SetCharacterSpacing (dwrite_1.h)
author: windows-sdk-content
description: Sets the spacing between characters.
old-location: directwrite\idwritetextlayout1_setcharacterspacing.htm
tech.root: DirectWrite
ms.assetid: 88B210CB-ED37-48F1-92F4-40BA591E7952
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IDWriteTextLayout1 interface [Direct Write],SetCharacterSpacing method, IDWriteTextLayout1.SetCharacterSpacing, IDWriteTextLayout1::SetCharacterSpacing, SetCharacterSpacing, SetCharacterSpacing method [Direct Write], SetCharacterSpacing method [Direct Write],IDWriteTextLayout1 interface, directwrite.idwritetextlayout1_setcharacterspacing, dwrite_1/IDWriteTextLayout1::SetCharacterSpacing
ms.topic: method
f1_keywords: 
 - "dwrite_1/IDWriteTextLayout1.SetCharacterSpacing"
req.header: dwrite_1.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 and Platform Update for Windows 7 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2012 and Platform Update for Windows Server 2008 R2 [desktop apps \| UWP apps]
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
 - IDWriteTextLayout1.SetCharacterSpacing
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IDWriteTextLayout1::SetCharacterSpacing


## -description


Sets the spacing between characters.


## -parameters




### -param leadingSpacing

Type: <b>FLOAT</b>

The spacing before each character, in reading order.


### -param trailingSpacing

Type: <b>FLOAT</b>

The spacing after each character, in reading order.


### -param minimumAdvanceWidth

Type: <b>FLOAT</b>

The minimum advance of each character, to prevent characters from becoming too thin or zero-width. This
    must be zero or greater.


### -param textRange

Type: <b><a href="/windows/win32/api/dwrite/ns-dwrite-dwrite_text_range">DWRITE_TEXT_RANGE</a></b>

Text range to which this change applies.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="/windows/win32/api/dwrite_1/nn-dwrite_1-idwritetextlayout1">IDWriteTextLayout1</a>
 

 

