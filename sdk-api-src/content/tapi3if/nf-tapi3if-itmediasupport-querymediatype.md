---
UID: NF:tapi3if.ITMediaSupport.QueryMediaType
title: ITMediaSupport::QueryMediaType
author: windows-sdk-content
description: The QueryMediaType method indicates whether the service provider associated with the current address supports the media type or types indicated by lMediaType.
old-location: tapi3\itmediasupport_querymediatype.htm
tech.root: tapi
ms.assetid: 684bfd94-5bef-415b-b548-49f564ce8a83
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: ITMediaSupport interface [TAPI 2.2],QueryMediaType method, ITMediaSupport.QueryMediaType, ITMediaSupport::QueryMediaType, QueryMediaType, QueryMediaType method [TAPI 2.2], QueryMediaType method [TAPI 2.2],ITMediaSupport interface, _tapi3_itmediasupport_querymediatype, tapi3.itmediasupport_querymediatype, tapi3if/ITMediaSupport::QueryMediaType
ms.topic: method
req.header: tapi3if.h
req.include-header: Tapi3.h
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
req.lib: Uuid.lib
req.dll: Tapi3.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Tapi3.dll
api_name:
 - ITMediaSupport.QueryMediaType
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ITMediaSupport::QueryMediaType


## -description


The 
<b>QueryMediaType</b> method indicates whether the service provider associated with the current address supports the 
<a href="https://msdn.microsoft.com/3e418c9a-a008-4b94-b5d2-7c2eccb3bf87">media type</a> or types indicated by <i>lMediaType</i>.


## -parameters




### -param lMediaType [in]


<a href="https://msdn.microsoft.com/3e418c9a-a008-4b94-b5d2-7c2eccb3bf87">Media type</a> or types being queried.


### -param pfSupport [out]

Pointer to a VARIANT_BOOL indicating whether the media type is supported. If the returned value is VARIANT_TRUE, the media is supported; if it is VARIANT_FALSE, the media is not supported.


## -returns



This method can return one of these values.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
Method succeeded.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
The <i>pfSupport</i> parameter is not a valid pointer.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
Insufficient memory exists to perform the operation.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/ab6db262-f99e-4027-9525-7597fcf02e72">Address Object</a>



<a href="https://msdn.microsoft.com/196995f1-b8d0-4ec1-b94e-61a02a258087">ITMediaSupport</a>
 

 

