---
UID: NF:tapi3if.ITMediaSupport.get_MediaTypes
title: ITMediaSupport::get_MediaTypes
author: windows-sdk-content
description: The get_MediaTypes method gets the media type or types supported on the current address.
old-location: tapi3\itmediasupport_get_mediatypes.htm
tech.root: tapi
ms.assetid: 8fc3d82e-6d6f-4442-9232-87f8d7605870
ms.author: windowssdkdev
ms.date: 11/08/2018
ms.keywords: ITMediaSupport interface [TAPI 2.2],get_MediaTypes method, ITMediaSupport.get_MediaTypes, ITMediaSupport::get_MediaTypes, _tapi3_itmediasupport_get_mediatypes, get_MediaTypes, get_MediaTypes method [TAPI 2.2], get_MediaTypes method [TAPI 2.2],ITMediaSupport interface, tapi3.itmediasupport_get_mediatypes, tapi3if/ITMediaSupport::get_MediaTypes
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - ITMediaSupport.get_MediaTypes
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ITMediaSupport::get_MediaTypes


## -description


The 
<b>get_MediaTypes</b> method gets the 
<a href="https://msdn.microsoft.com/3e418c9a-a008-4b94-b5d2-7c2eccb3bf87">media type</a> or types supported on the current address.


## -parameters




### -param plMediaTypes [out]

Pointer to bitmask of ORed of 
<a href="https://msdn.microsoft.com/3e418c9a-a008-4b94-b5d2-7c2eccb3bf87">media type</a>.


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
The <i>plMediaTypes</i> parameter is not a valid pointer.

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
 

 

