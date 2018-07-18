---
UID: NF:wmsdkidl.IWMClientConnections.GetClientCount
title: IWMClientConnections::GetClientCount
author: windows-sdk-content
description: The GetClientCount method retrieves the number of connected clients.
old-location: wmformat\iwmclientconnections_getclientcount.htm
old-project: wmformat
ms.assetid: 208b40cd-c138-4311-8702-18a61713b71a
ms.author: windowssdkdev
ms.date: 07/16/2018
ms.keywords: GetClientCount, GetClientCount method [windows Media Format], GetClientCount method [windows Media Format],IWMClientConnections interface, IWMClientConnections interface [windows Media Format],GetClientCount method, IWMClientConnections.GetClientCount, IWMClientConnections::GetClientCount, IWMClientConnectionsGetClientCount, wmformat.iwmclientconnections_getclientcount, wmsdkidl/IWMClientConnections::GetClientCount
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: WM_AETYPE
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
 - IWMClientConnections.GetClientCount
product: Windows
targetos: Windows
req.lib: Wmvcore.lib; WMStubDRM.lib (if you use DRM)
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IWMClientConnections::GetClientCount


## -description



The <b>GetClientCount</b> method retrieves the number of connected clients.




## -parameters




### -param pcClients [out]

Pointer to a count of the clients that are connected.


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
<i>pcClients</i> has been passed a null value.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/fea7cd85-22ab-4f3b-8a0a-301496f0c788">IWMClientConnections Interface</a>
 

 

