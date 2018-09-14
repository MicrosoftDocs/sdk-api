---
UID: NF:adhoc.IDot11AdHocInterface.GetStatus
title: IDot11AdHocInterface::GetStatus
author: windows-sdk-content
description: Gets the connection status of the active network associated with this NIC.
old-location: nwifi\idot11adhocinterface_getstatus.htm
tech.root: NativeWiFi
ms.assetid: 54e271dc-b710-4229-9682-2919af6cd998
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: GetStatus, GetStatus method [NativeWIFI], GetStatus method [NativeWIFI],IDot11AdHocInterface interface, IDot11AdHocInterface interface [NativeWIFI],GetStatus method, IDot11AdHocInterface.GetStatus, IDot11AdHocInterface::GetStatus, adhoc/IDot11AdHocInterface::GetStatus, nwifi.idot11adhocinterface_getstatus
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
 - IDot11AdHocInterface.GetStatus
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDot11AdHocInterface::GetStatus


## -description


Gets the connection status of the active network associated with this NIC. You can determine the active network by calling <a href="https://msdn.microsoft.com/aefe605a-720d-40da-8d0f-b1d5dd5b306e">IDot11AdHocInterface::GetActiveNetwork</a>.


## -parameters




### -param pState [in, out]

A pointer to a  <a href="https://msdn.microsoft.com/194179b9-9bd2-4c2f-ab22-c6b95eebfb43">DOT11_ADHOC_NETWORK_CONNECTION_STATUS</a> value that specifies the connection state.


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



<a href="https://msdn.microsoft.com/aefe605a-720d-40da-8d0f-b1d5dd5b306e">IDot11AdHocInterface::GetActiveNetwork</a>
 

 

