---
UID: NF:textstor.ITextStoreAnchor.RequestAttrsAtPosition
title: ITextStoreAnchor::RequestAttrsAtPosition
author: windows-sdk-content
description: ITextStoreAnchor::RequestAttrsAtPosition method
old-location: tsf\itextstoreanchor_requestattrsatposition.htm
old-project: TSF
ms.assetid: d0f20507-005b-409d-90d5-5817b7d95f19
ms.author: windowssdkdev
ms.date: 06/01/2018
ms.keywords: ITextStoreAnchor interface [Text Services Framework],RequestAttrsAtPosition method, ITextStoreAnchor.RequestAttrsAtPosition, ITextStoreAnchor::RequestAttrsAtPosition, RequestAttrsAtPosition, RequestAttrsAtPosition method [Text Services Framework], RequestAttrsAtPosition method [Text Services Framework],ITextStoreAnchor interface, textstor/ITextStoreAnchor::RequestAttrsAtPosition, tsf.itextstoreanchor_requestattrsatposition
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: textstor.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps | UWP apps]
req.target-min-winversvr: Windows 2000 Server [desktop apps | UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Textstor.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: TsRunType
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - msctf.dll
api_name:
 - ITextStoreAnchor.RequestAttrsAtPosition
product: Windows
targetos: Windows
req.lib: 
req.dll: Msctf.dll
req.irql: 
req.product: Windows XP with SP1 and later
---

# ITextStoreAnchor::RequestAttrsAtPosition


## -description




## -parameters




### -param paPos [in]

Pointer to the anchor.


### -param cFilterAttrs [in]

Specifies the number of attributes to obtain.


### -param paFilterAttrs [in]

Pointer to the <a href="https://msdn.microsoft.com/5e375609-3d3c-4c12-ae05-dcaa70779162">TS_ATTRID</a> data type that specifies the attribute to verify.


### -param dwFlags [in]

Must be zero.


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
The <i>paPos</i> anchor is invalid.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/62730a6d-4dc8-4207-9818-ab95e6537854">ITextStoreAnchor</a>



<a href="https://msdn.microsoft.com/36847680-bcf2-4db5-a587-90518f60cf5b">ITextStoreAnchor::RetrieveRequestedAttrs
      </a>



<a href="https://msdn.microsoft.com/5e375609-3d3c-4c12-ae05-dcaa70779162">
        TS_ATTRID
      </a>
 

 

