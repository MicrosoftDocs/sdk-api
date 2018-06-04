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

# IBitsPeerCacheAdministration::GetConfigurationFlags


## -description


Gets the configuration flags that determine if the computer serves content to peers and can download content from peers.


## -parameters




### -param pFlags [out]

Flags that determine if the computer serves content to peers and can download content from peers. The following flags can be set:

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="BG_ENABLE_PEERCACHING_CLIENT"></a><a id="bg_enable_peercaching_client"></a><dl>
<dt><b>BG_ENABLE_PEERCACHING_CLIENT</b></dt>
<dt>0x0001</dt>
</dl>
</td>
<td width="60%">
The computer can download content from peers.

</td>
</tr>
<tr>
<td width="40%"><a id="BG_ENABLE_PEERCACHING_SERVER"></a><a id="bg_enable_peercaching_server"></a><dl>
<dt><b>BG_ENABLE_PEERCACHING_SERVER</b></dt>
<dt>0x0002</dt>
</dl>
</td>
<td width="60%">
The computer can serve content to peers.

</td>
</tr>
</table>
 


## -returns



The method returns the following return values.

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
Success

</td>
</tr>
</table>
 




## -remarks



BITS can download from peers only if peercaching is enabled both at the computer level and at the job level; this API affects only the computer level. For details, see <a href="https://msdn.microsoft.com/1ede7c58-bc6d-4930-bca6-e4f26f97c648">IBitsPeerCacheAdministration::SetConfigurationFlags</a>.

Peer caching could have been enabled by Group Policy or by calling the <a href="https://msdn.microsoft.com/1ede7c58-bc6d-4930-bca6-e4f26f97c648">IBitsPeerCacheAdministration::SetConfigurationFlags</a> method.




## -see-also




<a href="https://msdn.microsoft.com/5fa30b4e-f13c-4341-af65-a2e3d2703b96">IBitsPeerCacheAdministration</a>



<a href="https://msdn.microsoft.com/1ede7c58-bc6d-4930-bca6-e4f26f97c648">IBitsPeerCacheAdministration::SetConfigurationFlags</a>
 

 

