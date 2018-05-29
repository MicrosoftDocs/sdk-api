---
UID: NF:adhoc.IDot11AdHocNetwork.GetInterface
title: IDot11AdHocNetwork::GetInterface
author: windows-sdk-content
description: Gets the interface associated with a network.
old-location: nwifi\idot11adhocnetwork_getinterface.htm
old-project: NativeWiFi
ms.assetid: 3c14c7fd-625b-48f7-b404-50da0db170f9
ms.author: windowssdkdev
ms.date: 04/13/2018
ms.keywords: GetInterface, GetInterface method [NativeWIFI], GetInterface method [NativeWIFI],IDot11AdHocNetwork interface, IDot11AdHocNetwork interface [NativeWIFI],GetInterface method, IDot11AdHocNetwork.GetInterface, IDot11AdHocNetwork::GetInterface, adhoc/IDot11AdHocNetwork::GetInterface, nwifi.idot11adhocnetwork_getinterface
ms.prod: windows
ms.technology: windows-sdk
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
req.typenames: DOT11_ADHOC_NETWORK_CONNECTION_STATUS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	adhoc.h
api_name:
-	IDot11AdHocNetwork.GetInterface
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# IDot11AdHocNetwork::GetInterface


## -description


Gets the interface associated with a network.


## -parameters




### -param pAdHocInterface [out]

A pointer to an <a href="https://msdn.microsoft.com/a4a73ff8-e24a-4f44-9205-c60699d1c27d">IDot11AdHocInterface</a>.


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
 

 

