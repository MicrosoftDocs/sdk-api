---
UID: NF:textstor.ITextStoreACP2.GetScreenExt
title: ITextStoreACP2::GetScreenExt
author: windows-sdk-content
description: Gets the bounding box screen coordinates of the display surface where the text stream is rendered.
old-location: tsf\itextstoreacp2_getscreenext.htm
tech.root: TSF
ms.assetid: fdc258ab-b692-495c-be76-0b41d75625e2
ms.author: windowssdkdev
ms.date: 10/19/2018
ms.keywords: GetScreenExt, GetScreenExt method [Text Services Framework], GetScreenExt method [Text Services Framework],ITextStoreACP2 interface, ITextStoreACP2 interface [Text Services Framework],GetScreenExt method, ITextStoreACP2.GetScreenExt, ITextStoreACP2::GetScreenExt, textstor/ITextStoreACP2::GetScreenExt, tsf.itextstoreacp2_getscreenext
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: textstor.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2012 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Textstor.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: Msctf.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - msctf.dll
api_name:
 - ITextStoreACP2.GetScreenExt
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ITextStoreACP2::GetScreenExt


## -description


Gets the bounding box screen coordinates of the display surface where the text stream is rendered.


## -parameters




### -param vcView [in]

Specifies the context view.


### -param prc [out]

Receives the bounding box screen coordinates of the display surface of the document.


## -returns



This method can return one of these values.

<table>
<tr>
<th>Value</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The method was successful.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
The specified <i>vcView</i> parameter is invalid.

</td>
</tr>
</table>
 




## -remarks



If the text is not currently displayed, for example, if the document window is minimized, the <i>prc</i> parameter is set to { 0, 0, 0, 0 }.




## -see-also




<a href="https://msdn.microsoft.com/c256f1c2-6b67-4417-8707-3490a2c5cb55">ITextStoreACP2</a>



<a href="https://msdn.microsoft.com/499a446d-1575-4636-b444-dd6078ed8736">ITfContextOwner::GetScreenExt
      </a>



<a href="https://msdn.microsoft.com/86dde611-4c46-418c-aa89-728081a28943">ITfContextView::GetScreenExt
      </a>



<a href="https://msdn.microsoft.com/e649b799-d0d6-4f2d-b9f1-28070eea9b16">TsViewCookie
      </a>
 

 

