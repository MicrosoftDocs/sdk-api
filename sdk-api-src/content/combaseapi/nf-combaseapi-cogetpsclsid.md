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

# CoGetPSClsid function


## -description


Returns the CLSID of the DLL that implements the proxy and stub for the specified interface.


## -parameters




### -param riid [in]

The interface whose proxy/stub CLSID is to be returned.


### -param pClsid [out]

Specifies where to store the proxy/stub CLSID for the interface specified by <i>riid</i>.


## -returns



This function can return the following values.

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
The proxy/stub CLSID was successfully returned.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
One of the parameters is invalid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
There is insufficient memory to complete this operation.

</td>
</tr>
</table>
 




## -remarks



The <b>CoGetPSClsid</b> function looks at the <b>HKEY_CLASSES_ROOT</b>\<b>Interfaces</b>\<i>{string form of riid}</i>\<b>ProxyStubClsid32</b> key in the registry to determine the CLSID of the DLL to load in order to create the proxy and stub for the interface specified by <i>riid</i>. This function also returns the CLSID for any interface IID registered by <a href="https://msdn.microsoft.com/a73dbd6d-d3f2-48d7-b053-b62f2f18f2d6">CoRegisterPSClsid</a> within the current process.




## -see-also




<a href="https://msdn.microsoft.com/a73dbd6d-d3f2-48d7-b053-b62f2f18f2d6">CoRegisterPSClsid</a>
 

 

