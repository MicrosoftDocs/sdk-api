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

# MprConfigServerInstall function


## -description


The 
<b>MprConfigServerInstall</b> function configures Routing and Remote Access Service with a default configuration.


## -parameters




### -param dwLevel [in]

This parameter is reserved for future use, and should be zero.


### -param pBuffer [in]

This parameter is reserved for future use, and should be <b>NULL</b>.


## -returns



If the functions succeeds, the return value is ERROR_SUCCESS.

If the function fails, the return value is one of the following error codes.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_PARAMETER</b></dt>
</dl>
</td>
<td width="60%">
One of the following is true: 




<ul>
<li><i>dwLevel</i> is not zero.</li>
<li><i>pBuffer</i> is non-<b>NULL</b>.</li>
</ul>
</td>
</tr>
</table>
 




## -remarks



The 
<b>MprConfigServerInstall</b> function performs the following tasks:

<ul>
<li>Resets the current Router Manager and Interface keys.</li>
<li>Initializes RAS structures for IP.</li>
<li>Sets the router type to include: 


ROUTER_TYPE_RAS

ROUTER_TYPE_WAN

ROUTER_TYPE_LAN

</li>
<li>Sets the error logging level and authorization settings to defaults.</li>
<li>Sets the devices for Routing and RAS.</li>
<li>Adds the RRAS snap-in to the computer management console.</li>
<li>Deletes the router phone book.</li>
<li>Registers the router in the domain.</li>
<li>Writes out the <b>router is configured</b> registry key.</li>
</ul>
The 
<b>MprConfigServerInstall</b> function does not start Routing and RAS or  set the service start type for Routing and RAS.




## -see-also




<a href="https://msdn.microsoft.com/5464c2f7-6bb8-4838-939d-d58508715505">Windows 2000 Registry Layout</a>
 

 

