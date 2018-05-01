---
UID: NF:adhoc.IDot11AdHocNetwork.GetSSID
title: IDot11AdHocNetwork::GetSSID method
author: windows-driver-content
description: Gets the SSID of the network.
old-location: nwifi\idot11adhocnetwork_getssid.htm
old-project: NativeWiFi
ms.assetid: a1a190a2-038b-4353-8dc9-76950b1da9ff
ms.author: windowsdriverdev
ms.date: 4/13/2018
ms.keywords: GetSSID method [NativeWIFI], GetSSID method [NativeWIFI], IDot11AdHocNetwork interface, GetSSID,IDot11AdHocNetwork.GetSSID, IDot11AdHocNetwork, IDot11AdHocNetwork interface [NativeWIFI], GetSSID method, IDot11AdHocNetwork::GetSSID, adhoc/IDot11AdHocNetwork::GetSSID, nwifi.idot11adhocnetwork_getssid
ms.prod: windows-hardware
ms.technology: windows-devices
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
-	IDot11AdHocNetwork.GetSSID
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# IDot11AdHocNetwork::GetSSID method


## -description


Gets the SSID of the network.


## -parameters




### -param ppszwSSID [out]

The SSID of the network.

You must free this string using <a href="_com_CoTaskMemFree">CoTaskMemFree</a>.




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
 

 

