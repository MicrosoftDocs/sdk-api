---
UID: NF:textstor.ITextStoreACP.GetScreenExt
title: ITextStoreACP::GetScreenExt method
author: windows-driver-content
description: The ITextStoreACP::GetScreenExt method returns the bounding box screen coordinates of the display surface where the text stream is rendered.
old-location: tsf\itextstoreacp_getscreenext.htm
old-project: TSF
ms.assetid: bd542dd1-79a5-47ec-a563-cd37a8c36b1a
ms.author: windowsdriverdev
ms.date: 3/26/2018
ms.keywords: GetScreenExt method [Text Services Framework], GetScreenExt method [Text Services Framework], ITextStoreACP interface, GetScreenExt,ITextStoreACP.GetScreenExt, ITextStoreACP, ITextStoreACP interface [Text Services Framework], GetScreenExt method, ITextStoreACP::GetScreenExt, _tsf_itextstoreacp_getscreenext_ref, textstor/ITextStoreACP::GetScreenExt, tsf.itextstoreacp_getscreenext
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: textstor.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Textstor.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: TsRunType
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	msctf.dll
api_name:
-	ITextStoreACP.GetScreenExt
product: Windows
targetos: Windows
req.lib: 
req.dll: Msctf.dll
req.irql: 
req.product: Windows XP with SP1 and later
---

# ITextStoreACP::GetScreenExt method


## -description


The <b>ITextStoreACP::GetScreenExt</b> method returns the bounding box screen coordinates of the display surface where the text stream is rendered.


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




<a href="https://msdn.microsoft.com/21e011f7-6791-4eb9-85c9-18bd10107119">ITextStoreACP</a>



<a href="https://msdn.microsoft.com/499a446d-1575-4636-b444-dd6078ed8736">ITfContextOwner::GetScreenExt
      </a>



<a href="https://msdn.microsoft.com/86dde611-4c46-418c-aa89-728081a28943">
        ITfContextView::GetScreenExt
      </a>



<a href="https://msdn.microsoft.com/e649b799-d0d6-4f2d-b9f1-28070eea9b16">
        TsViewCookie
      </a>
 

 

