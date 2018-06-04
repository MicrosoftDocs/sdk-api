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

# _USE_INFO_3 structure


## -description


The
				<b>USE_INFO_3</b> structure contains information about a connection between a local computer and a shared resource, including connection type, connection status, user name, domain name, and specific flags that describe connection behavior.


## -struct-fields




### -field ui3_ui2


<a href="https://msdn.microsoft.com/4cc36108-085a-47c4-9dfa-b46f7e208c8b">USE_INFO_2</a> structure that contains 


### -field ui3_flags

 




#### - flags


					A set of bit flags that describe connection behavior and credential handling.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="CREATE_NO_CONNECT"></a><a id="create_no_connect"></a><dl>
<dt><b>CREATE_NO_CONNECT</b></dt>
</dl>
</td>
<td width="60%">
Do not connect to the server.

</td>
</tr>
<tr>
<td width="40%"><a id="CREATE_BYPASS_CSC"></a><a id="create_bypass_csc"></a><dl>
<dt><b>CREATE_BYPASS_CSC</b></dt>
</dl>
</td>
<td width="60%">
Force a connection to the server, bypassing the CSC.

</td>
</tr>
<tr>
<td width="40%"><a id="USE_DEFAULT_CREDENTIALS"></a><a id="use_default_credentials"></a><dl>
<dt><b>USE_DEFAULT_CREDENTIALS</b></dt>
</dl>
</td>
<td width="60%">
No explicit credentials are supplied in the call to <a href="https://msdn.microsoft.com/22550c17-003a-4f59-80f0-58fa3e286844">NetUseAdd</a>.

</td>
</tr>
</table>
 


## -see-also




<a href="https://msdn.microsoft.com/fb527f85-baea-48e8-b837-967870834ec5">NetUseEnum</a>



<a href="https://msdn.microsoft.com/257875db-5ed9-4569-8dbb-5dcc7a6af95c">NetUseGetInfo</a>



<a href="https://msdn.microsoft.com/426c7b2e-027c-4a88-97b7-eba5201d0f0d">Network Management Overview</a>



<a href="https://msdn.microsoft.com/a4b05054-bef2-4cab-89f6-725d92ee75b8">Network Management Structures</a>



<a href="https://msdn.microsoft.com/ddf1b8dc-f13b-402a-9e4e-e4944a29ac31">Use Functions</a>
 

 

