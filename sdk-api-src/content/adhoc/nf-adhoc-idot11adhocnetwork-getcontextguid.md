---
UID: NF:adhoc.IDot11AdHocNetwork.GetContextGuid
title: IDot11AdHocNetwork::GetContextGuid (adhoc.h)
author: windows-sdk-content
description: Gets the context identifier associated with the network.
old-location: nwifi\idot11adhocnetwork_getcontextguid.htm
tech.root: NativeWiFi
ms.assetid: 6a7e7a75-b070-4d57-ae88-6bfc3568c3c9
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: GetContextGuid, GetContextGuid method [NativeWIFI], GetContextGuid method [NativeWIFI],IDot11AdHocNetwork interface, IDot11AdHocNetwork interface [NativeWIFI],GetContextGuid method, IDot11AdHocNetwork.GetContextGuid, IDot11AdHocNetwork::GetContextGuid, adhoc/IDot11AdHocNetwork::GetContextGuid, nwifi.idot11adhocnetwork_getcontextguid
ms.topic: method
req.header: adhoc.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Adhoc.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - adhoc.h
api_name:
 - IDot11AdHocNetwork.GetContextGuid
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IDot11AdHocNetwork::GetContextGuid


## -description


Gets the context identifier associated with the network. This GUID identifies the application that created the network.


## -parameters




### -param pContextGuid [in, out]

The context identifier associated with the network. If no ContextGuid was specified when the <a href="https://msdn.microsoft.com/1d9930b3-7bc4-4015-b096-a21fe01f54f5">CreateNetwork</a> call was made, the GUID returned consists of all zeros. 


## -returns



Possible return values include, but are not limited to, the following.

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
The method completed successfully.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_FAIL</b></dt>
</dl>
</td>
<td width="60%">
The method failed.

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
The method could not allocate the memory required to perform this operation.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
A pointer passed as a parameter is not valid.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/2736bb81-b66f-4c09-8c76-ca16f3eab192">IDot11AdHocNetwork</a>
 

 

