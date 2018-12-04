---
UID: NF:dwrite_2.IDWriteTextLayout2.SetFontFallback
title: IDWriteTextLayout2::SetFontFallback
author: windows-sdk-content
description: Apply a custom font fallback onto layout.
old-location: directwrite\idwritetextlayout2_setfontfallback.htm
tech.root: DirectWrite
ms.assetid: 63B86AE4-92D4-4748-A6E2-987B740080EB
ms.author: windowssdkdev
ms.date: 11/30/2018
ms.keywords: IDWriteTextLayout2 interface [Direct Write],SetFontFallback method, IDWriteTextLayout2.SetFontFallback, IDWriteTextLayout2::SetFontFallback, SetFontFallback, SetFontFallback method [Direct Write], SetFontFallback method [Direct Write],IDWriteTextLayout2 interface, directwrite.idwritetextlayout2_setfontfallback, dwrite_2/IDWriteTextLayout2::SetFontFallback
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: dwrite_2.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8.1 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 R2 [desktop apps only]
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
 - IDWriteTextLayout2.SetFontFallback
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDWriteTextLayout2::SetFontFallback


## -description


Apply a custom font fallback onto layout. If none is specified, the layout uses the system fallback list.
      


## -parameters




### -param fontFallback

Custom font fallback created from <a href="https://msdn.microsoft.com/933CB690-879E-480E-A0C6-179FA84187F5">IDWriteFontFallbackBuilder::CreateFontFallback</a> or <a href="https://msdn.microsoft.com/7F2BDB39-2CB4-4DB7-BBBA-74B0C07E7420">IDWriteFactory2::GetSystemFontFallback</a>.
          


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/034D795B-016A-401E-AD75-D5B0D1E87806">IDWriteTextLayout2</a>
 

 

