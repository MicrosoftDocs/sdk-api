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

# IMFInputTrustAuthority::GetDecrypter


## -description



Retrieves a decrypter transform.




## -parameters




### -param riid [in]

Interface identifier (IID) of the interface being requested. Currently this value must be IID_IMFTransform, which requests the <a href="https://msdn.microsoft.com/3cc502d8-d364-43b9-b0b6-d9474c002b20">IMFTransform</a> interface.


### -param ppv [out]

Receives a pointer to the interface. The caller must release the interface.


## -returns



The method returns an HRESULT. Possible values include, but are not limited to, those in the following table.

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
The method succeeded.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_NOINTERFACE</b></dt>
</dl>
</td>
<td width="60%">
The decrypter does not support the requested interface.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MF_E_NOT_PROTECTED</b></dt>
</dl>
</td>
<td width="60%">
This input trust authority (ITA) does not provide a decrypter.

</td>
</tr>
</table>
 




## -remarks



The decrypter should be created in a disabled state, where any calls to <a href="https://msdn.microsoft.com/dc58cc75-7e01-4f47-a572-8e3ca1bc43b4">IMFTransform::ProcessOutput</a> automatically fail. After the input trust authority (ITA) has verified that it is running inside the protected media path (PMP), the ITA should enable the decrypter.

An ITA is not required to provide a decrypter. If the source content is not encrypted, the method should return MF_E_NOT_PROTECTED. The PMP will then proceed without using a decrypter for that stream.

The ITA must create a new instance of its decrypter for each call to <b>GetDecrypter</b>. Do not return multiple references to the same decrypter. They must be separate instances because the Media Session might place them in two different branches of the topology.




## -see-also




<a href="https://msdn.microsoft.com/637e0225-6fd8-4b83-b4fb-119e7a5ef5d2">IMFInputTrustAuthority</a>
 

 

