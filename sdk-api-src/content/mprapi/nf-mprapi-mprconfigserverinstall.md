---
UID: NF:mprapi.MprConfigServerInstall
title: MprConfigServerInstall function
author: windows-driver-content
description: The MprConfigServerInstall function configures Routing and Remote Access Service with a default configuration.
old-location: rras\mprconfigserverinstall.htm
old-project: RRAS
ms.assetid: a261aaf8-abb0-4580-850b-f447017e07b9
ms.author: windowsdriverdev
ms.date: 4/16/2018
ms.keywords: MprConfigServerInstall, MprConfigServerInstall function [RAS], _mpr_mprconfigserverinstall, mprapi/MprConfigServerInstall, rras.mprconfigserverinstall
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: mprapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
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
req.typenames: ROUTER_INTERFACE_TYPE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	Mprapi.dll
api_name:
-	MprConfigServerInstall
product: Windows
targetos: Windows
req.lib: Mprapi.lib
req.dll: Mprapi.dll
req.irql: 
req.product: GDI+ 1.1
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
 

 

