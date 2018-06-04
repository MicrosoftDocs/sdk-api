---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
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
---

# IWCNDevice::GetVendorExtension


## -description


The <b>GetVendorExtension</b> method gets a cached vendor extension from the device.


## -parameters




### -param pVendorExtSpec




### -param dwMaxBufferSize [in]

The size, in bytes, of <i>pbBuffer</i>.


### -param pbBuffer [out]

An allocated buffer that,  on return, contains the contents of the  vendor extension.



### -param pdwBufferUsed [out]

On return, contains the size of the vendor extension in bytes.


#### - const [in]

A pointer to a user-defined <b>WCN_VENDOR_EXTENSION_SPEC</b> structure that describes the vendor extension to query for.


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
The vendor extension was retrieved successfully.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>HRESULT_FROM_WIN32(ERROR_NOT_FOUND)</b></dt>
</dl>
</td>
<td width="60%">
The vendor extension specified is not available.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>HRESULT_FROM_WIN32(ERROR_INSUFFICIENT_BUFFER)</b></dt>
</dl>
</td>
<td width="60%">
The buffer specified by <i>pbBuffer</i> is not large enough to contain the returned vendor extension.

</td>
</tr>
</table>
 




## -remarks



 To query the size of a vendor extension, you can pass a value of 0 with the <i>dwMaxBufferSize</i> parameter, and <i>pdwBufferUsed</i> will receive the size.




## -see-also




<a href="https://msdn.microsoft.com/a092406d-7af4-436d-9755-5a9b87aa6ca9">IWCNDevice</a>
 

 

