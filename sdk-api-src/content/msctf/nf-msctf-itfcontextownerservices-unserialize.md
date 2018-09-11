---
UID: NF:msctf.ITfContextOwnerServices.Unserialize
title: ITfContextOwnerServices::Unserialize
author: windows-sdk-content
description: ITfContextOwnerServices::Unserialize method
old-location: tsf\itfcontextownerservices_unserialize.htm
tech.root: TSF
ms.assetid: b02ffedf-83c5-48ff-8116-801aaec6dc71
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: ITfContextOwnerServices interface [Text Services Framework],Unserialize method, ITfContextOwnerServices.Unserialize, ITfContextOwnerServices::Unserialize, Unserialize, Unserialize method [Text Services Framework], Unserialize method [Text Services Framework],ITfContextOwnerServices interface, _tsf_itfcontextownerservices_unserialize_ref, msctf/ITfContextOwnerServices::Unserialize, tsf.itfcontextownerservices_unserialize
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: msctf.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps \| UWP apps]
req.target-min-winversvr: Windows 2000 Server [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Msctf.idl
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
 - ITfContextOwnerServices.Unserialize
product: Windows
targetos: Windows
req.typenames: 
req.redist: TSF 1.0 on Windows 2000 Professional
---

# ITfContextOwnerServices::Unserialize


## -description




## -parameters




### -param pProp [in]

Pointer to an <a href="https://msdn.microsoft.com/72bd92f9-d82e-4994-82ad-0989e987903b">ITfProperty</a> object that receives the property data.


### -param pHdr [in]

Pointer to a <a href="https://msdn.microsoft.com/9c5cb193-d18e-4d91-b9be-b8a61a56d3a3">TF_PERSISTENT_PROPERTY_HEADER_ACP</a> structure that contains the header data for the property.


### -param pStream [in]

Pointer to an <b>IStream</b> object that contains the property data. This parameter can be <b>NULL</b> if <i>pLoader</i> is not <b>NULL</b>. This parameter is ignored if <i>pLoader</i> is not <b>NULL</b>.


### -param pLoader [in]

Pointer to an <a href="https://msdn.microsoft.com/7d7af737-6241-43a9-946e-6a03a423b20f">ITfPersistentPropertyLoaderACP</a> object that the TSF manager uses to obtain the property data. This parameter can be <b>NULL</b> if <i>pStream</i> is not <b>NULL</b>.


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
<dt><b>TF_S_ASYNC</b></dt>
</dl>
</td>
<td width="60%">
The property data is obtained asynchronously.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>TF_E_SYNCHRONOUS</b></dt>
</dl>
</td>
<td width="60%">
A synchronous read-only lock cannot be obtained.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_FAIL</b></dt>
</dl>
</td>
<td width="60%">
An unspecified error occurred.

</td>
</tr>
</table>
 




## -remarks



If <i>pStream</i> is specified rather than <i>pLoader</i>, the property data is read from <i>pStream</i> during the call to this method. If <i>pLoader</i> is specified rather than <i>pStream</i>, the property data is read from <i>pLoader</i> asynchronously. Using <i>pStream</i> can cause long delays if the property data is large.

When calling this method, the application must be able to grant a synchronous read-only lock.




## -see-also




<a href="https://msdn.microsoft.com/fb77bd6a-ae34-4e21-8f09-fc8c6a1ade86">ITfContextOwnerServices</a>



<a href="https://msdn.microsoft.com/e67b6fa7-610d-426f-a290-36c0da4068f4">ITfContextOwnerServices::Serialize
      </a>



<a href="https://msdn.microsoft.com/7d7af737-6241-43a9-946e-6a03a423b20f">ITfPersistentPropertyLoaderACP
      </a>



<a href="https://msdn.microsoft.com/72bd92f9-d82e-4994-82ad-0989e987903b">ITfProperty
      </a>



<a href="https://msdn.microsoft.com/9c5cb193-d18e-4d91-b9be-b8a61a56d3a3">TF_PERSISTENT_PROPERTY_HEADER_ACP
      </a>
 

 

