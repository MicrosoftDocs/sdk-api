---
UID: NF:dwrite_2.IDWriteTextFormat1.SetFontFallback
title: IDWriteTextFormat1::SetFontFallback
author: windows-sdk-content
description: Applies the custom font fallback onto the layout. If none is set, it uses the default system fallback list.
old-location: directwrite\idwritetextformat1_setfontfallback.htm
tech.root: DirectWrite
ms.assetid: 56B577C0-2B18-409E-ADEC-0B93355586A0
ms.author: windowssdkdev
ms.date: 11/02/2018
ms.keywords: IDWriteTextFormat1 interface [Direct Write],SetFontFallback method, IDWriteTextFormat1.SetFontFallback, IDWriteTextFormat1::SetFontFallback, SetFontFallback, SetFontFallback method [Direct Write], SetFontFallback method [Direct Write],IDWriteTextFormat1 interface, directwrite.idwritetextformat1_setfontfallback, dwrite_2/IDWriteTextFormat1::SetFontFallback
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: dwrite_2.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8.1 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2012 R2 [desktop apps \| UWP apps]
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
 - IDWriteTextFormat1.SetFontFallback
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDWriteTextFormat1::SetFontFallback


## -description


Applies the custom font fallback onto the layout. If none is set, it uses the default system fallback list.
        


## -parameters




### -param fontFallback

Type: <b><a href="https://msdn.microsoft.com/CBC4100A-756B-429E-8368-D5D018A2B0AC">IDWriteFontFallback</a>*</b>

The font fallback to apply to the layout.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/15295A17-E542-4071-AE38-02014A1235D5">IDWriteTextFormat1</a>
 

 

