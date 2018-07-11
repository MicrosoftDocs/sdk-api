---
UID: NF:iwstdec.IAMWstDecoder.SetHoldPage
title: IAMWstDecoder::SetHoldPage
author: windows-sdk-content
description: Downstream filters use the SetHoldPage method to tell the WST decoder to hold the current WST page. When the WST decoder holds a page, any updates from the TV stream are turned off. It is as though the page was paused in real time.
old-location: dshow\iamwstdecoder_setholdpage.htm
old-project: DirectShow
ms.assetid: 2fea6f52-bae3-4679-a89b-fe85f1232d34
ms.author: windowssdkdev
ms.date: 07/09/2018
ms.keywords: IAMWstDecoder interface [DirectShow],SetHoldPage method, IAMWstDecoder.SetHoldPage, IAMWstDecoder::SetHoldPage, IAMWstDecoderSetHoldPage, SetHoldPage, SetHoldPage method [DirectShow], SetHoldPage method [DirectShow],IAMWstDecoder interface, dshow.iamwstdecoder_setholdpage, iwstdec/IAMWstDecoder::SetHoldPage
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: iwstdec.h
req.include-header: 
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
 - IAMWstDecoder.SetHoldPage
product: Windows
targetos: Windows
req.lib: Strmiids.lib
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IAMWstDecoder::SetHoldPage


## -description



Downstream filters use the <code>SetHoldPage</code> method to tell the WST decoder to hold the current WST page. When the WST decoder holds a page, any updates from the TV stream are turned off. It is as though the page was paused in real time.




## -parameters




### -param bHoldPage [in]

Specifies whether to hold the current page.

<table>
<tr>
<th>
                  Value
                </th>
<th>
                  Description
                </th>
</tr>
<tr>
<td><b>TRUE</b></td>
<td>Hold the current page</td>
</tr>
<tr>
<td><b>FALSE</b></td>
<td>Release the current page.</td>
</tr>
</table>
 


## -returns



When the method succeeds, it returns S_OK. Otherwise, it returns an <b>HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/f2f5a459-14de-4be1-909c-3c23e4cfd737">IAMWstDecoder Interface</a>
 

 

