---
UID: NF:iwstdec.IAMWstDecoder.SetCurrentPage
title: IAMWstDecoder::SetCurrentPage
author: windows-sdk-content
description: Downstream filters use the SetCurrentPage method to assign the current page.
old-location: dshow\iamwstdecoder_setcurrentpage.htm
old-project: DirectShow
ms.assetid: 84f8854d-77a7-4ae3-9fec-c4d6fce7eead
ms.author: windowssdkdev
ms.date: 08/02/2018
ms.keywords: IAMWstDecoder interface [DirectShow],SetCurrentPage method, IAMWstDecoder.SetCurrentPage, IAMWstDecoder::SetCurrentPage, IAMWstDecoderSetCurrentPage, SetCurrentPage, SetCurrentPage method [DirectShow], SetCurrentPage method [DirectShow],IAMWstDecoder interface, dshow.iamwstdecoder_setcurrentpage, iwstdec/IAMWstDecoder::SetCurrentPage
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: iwstdec.h
req.include-header: 
req.redist: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
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
req.typenames: AM_WST_STYLE, *PAM_WST_STYLE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Strmiids.lib
 - Strmiids.dll
api_name:
 - IAMWstDecoder.SetCurrentPage
product: Windows
targetos: Windows
req.lib: Strmiids.lib
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IAMWstDecoder::SetCurrentPage


## -description



Downstream filters use the <code>SetCurrentPage</code> method to assign the current page.




## -parameters




### -param WstPage [in]

Specifies an <a href="https://msdn.microsoft.com/6bed254f-35e4-40d0-9a59-0a2575aa61e1">AM_WST_PAGE</a> structure that is used to assign the current page.


## -returns



When the method succeeds, it returns S_OK. Otherwise, it returns an <b>HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/f2f5a459-14de-4be1-909c-3c23e4cfd737">IAMWstDecoder Interface</a>
 

 

