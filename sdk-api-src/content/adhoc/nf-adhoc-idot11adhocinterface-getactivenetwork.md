---
UID: NF:adhoc.IDot11AdHocInterface.GetActiveNetwork
title: IDot11AdHocInterface::GetActiveNetwork
author: windows-sdk-content
description: Gets the network that is currently active on the interface.
old-location: nwifi\idot11adhocinterface_getactivenetwork.htm
old-project: NativeWiFi
ms.assetid: aefe605a-720d-40da-8d0f-b1d5dd5b306e
ms.author: windowssdkdev
ms.date: 07/09/2018
ms.keywords: GetActiveNetwork, GetActiveNetwork method [NativeWIFI], GetActiveNetwork method [NativeWIFI],IDot11AdHocInterface interface, IDot11AdHocInterface interface [NativeWIFI],GetActiveNetwork method, IDot11AdHocInterface.GetActiveNetwork, IDot11AdHocInterface::GetActiveNetwork, adhoc/IDot11AdHocInterface::GetActiveNetwork, nwifi.idot11adhocinterface_getactivenetwork
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
tech.root: 
req.typenames: DOT11_ADHOC_NETWORK_CONNECTION_STATUS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - adhoc.h
api_name:
 - IDot11AdHocInterface.GetActiveNetwork
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# IDot11AdHocInterface::GetActiveNetwork


## -description


Gets the network that is currently active on the interface.


## -parameters




### -param ppNetwork [out]

A pointer to an IDot11AdHocNetwork object that represents the active network.


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




<a href="https://msdn.microsoft.com/a4a73ff8-e24a-4f44-9205-c60699d1c27d">IDot11AdHocInterface</a>



<a href="https://msdn.microsoft.com/54e271dc-b710-4229-9682-2919af6cd998">IDot11AdHocInterface::GetStatus</a>
 

 

