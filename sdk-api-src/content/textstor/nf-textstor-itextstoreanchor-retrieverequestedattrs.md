---
UID: NF:textstor.ITextStoreAnchor.RetrieveRequestedAttrs
title: ITextStoreAnchor::RetrieveRequestedAttrs (textstor.h)
author: windows-sdk-content
description: ITextStoreAnchor::RetrieveRequestedAttrs method
old-location: tsf\itextstoreanchor_retrieverequestedattrs.htm
tech.root: TSF
ms.assetid: 36847680-bcf2-4db5-a587-90518f60cf5b
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: ITextStoreAnchor interface [Text Services Framework],RetrieveRequestedAttrs method, ITextStoreAnchor.RetrieveRequestedAttrs, ITextStoreAnchor::RetrieveRequestedAttrs, RetrieveRequestedAttrs, RetrieveRequestedAttrs method [Text Services Framework], RetrieveRequestedAttrs method [Text Services Framework],ITextStoreAnchor interface, textstor/ITextStoreAnchor::RetrieveRequestedAttrs, tsf.itextstoreanchor_retrieverequestedattrs
ms.topic: method
req.header: textstor.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps \| UWP apps]
req.target-min-winversvr: Windows 2000 Server [desktop apps \| UWP apps]
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
 - ITextStoreAnchor.RetrieveRequestedAttrs
product: Windows
targetos: Windows
req.typenames: 
req.redist: TSF 1.0 on Windows 2000 Professional
---

# ITextStoreAnchor::RetrieveRequestedAttrs


## -description




## -parameters




### -param ulCount [in]

Specifies the number of supported attributes to obtain.


### -param paAttrVals [out]

Pointer to the <a href="https://msdn.microsoft.com/9209ef60-6a1d-4aad-9f9f-775534116f37">TS_ATTRVAL</a> structure that receives the supported attributes. The members of this structure depend upon the <i>dwFlags</i> parameter of the calling method.


### -param pcFetched [out]

Receives the number of supported attributes.


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
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/62730a6d-4dc8-4207-9818-ab95e6537854">ITextStoreAnchor</a>



<a href="https://msdn.microsoft.com/d0f20507-005b-409d-90d5-5817b7d95f19">ITextStoreAnchor::RequestAttrsAtPosition
      </a>



<a href="https://msdn.microsoft.com/f0f43237-8c26-4e0c-8717-908884229b7b">ITextStoreAnchor::RequestAttrsTransitioningAtPosition
      </a>



<a href="https://msdn.microsoft.com/ab81d79d-e991-4c2d-9fb7-95393e002828">ITextStoreAnchor::RequestSupportedAttrs
      </a>



<a href="https://msdn.microsoft.com/9209ef60-6a1d-4aad-9f9f-775534116f37">TS_ATTRVAL
      </a>
 

 

