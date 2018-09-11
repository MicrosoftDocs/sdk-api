---
UID: NF:wmsdkidl.IWMClientConnections.GetClientProperties
title: IWMClientConnections::GetClientProperties
author: windows-sdk-content
description: The GetClientProperties method retrieves information, including the IP address and protocol, about a connected client.
old-location: wmformat\iwmclientconnections_getclientproperties.htm
tech.root: wmformat
ms.assetid: a05d7d1e-21dc-4e2a-a17b-5f04e639b143
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: GetClientProperties, GetClientProperties method [windows Media Format], GetClientProperties method [windows Media Format],IWMClientConnections interface, IWMClientConnections interface [windows Media Format],GetClientProperties method, IWMClientConnections.GetClientProperties, IWMClientConnections::GetClientProperties, IWMClientConnectionsGetClientProperties, wmformat.iwmclientconnections_getclientproperties, wmsdkidl/IWMClientConnections::GetClientProperties
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: wmsdkidl.h
req.include-header: Wmsdk.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only],Windows Media Format 7 SDK, or later versions of the SDK
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Wmvcore.lib; WMStubDRM.lib (if you use DRM)
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Wmvcore.lib
 - Wmvcore.dll
 - WMStubDRM.lib
 - WMStubDRM.dll
api_name:
 - IWMClientConnections.GetClientProperties
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IWMClientConnections::GetClientProperties


## -description



The <b>GetClientProperties</b> method retrieves information, including the IP address and protocol, about a connected client.




## -parameters




### -param dwClientNum [in]

<b>DWORD</b> containing the client's index number.


### -param pClientProperties [out]

Pointer to a <a href="https://msdn.microsoft.com/62a5bafd-cc49-4a60-be03-038920e5b073">WM_CLIENT_PROPERTIES</a> structure.


## -returns



The method returns an <b>HRESULT</b>. Possible values include, but are not limited to, those in the following table.

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
<dt><b>NS_E_INVALID_REQUEST</b></dt>
</dl>
</td>
<td width="60%">
Streaming has not yet begun.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
<i>pcClientProperties</i> has been passed a null value.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>NS_E_INVALID_CLIENT</b></dt>
</dl>
</td>
<td width="60%">
A client number larger than the number of clients has been passed in.

OR

Failed to get client information for unspecified reason.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/fea7cd85-22ab-4f3b-8a0a-301496f0c788">IWMClientConnections Interface</a>
 

 

