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

# IWMWriterNetworkSink::GetNetworkProtocol


## -description



The <b>GetNetworkProtocol</b> method retrieves the network protocol that the network sink uses. Currently, HTTP is the only protocol the network sink supports.




## -parameters




### -param pProtocol [out]

Pointer to a variable that receives a member of the <a href="https://msdn.microsoft.com/dc8b67a9-33fe-408b-b0b5-62a2b219b6b5">WMT_NET_PROTOCOL</a> enumeration type.


## -returns



The method returns an <b>HRESULT</b>. Possible values include, but are not limited to, the values shown in the following table.

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
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
<i>pProtocol</i> is <b>NULL</b>.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/3204c360-f407-4cf3-bb21-7e6094587fb0">IWMWriterNetworkSink Interface</a>



<a href="https://msdn.microsoft.com/8ad6b2a4-b50b-45a0-8aa0-cabfc1e59bb7">IWMWriterNetworkSink::SetNetworkProtocol</a>



<a href="https://msdn.microsoft.com/dc8b67a9-33fe-408b-b0b5-62a2b219b6b5">WMT_NET_PROTOCOL</a>
 

 

