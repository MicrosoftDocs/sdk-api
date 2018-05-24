---
UID: NF:sensapi.IsNetworkAlive
title: IsNetworkAlive function
author: windows-driver-content
description: The IsNetworkAlive function determines whether or not a local system is connected to a network, and identifies the type of network connection, for example, a LAN, WAN, or both.
old-location: sens\isnetworkalive.htm
old-project: Sens
ms.assetid: 1a2f3acd-0626-4fb2-8c5f-f3a0704cc0b4
ms.author: windowsdriverdev
ms.date: 2/15/2018
ms.keywords: IsNetworkAlive, IsNetworkAlive function [SENS], _zaw_isnetworkalive, sens.isnetworkalive, sensapi/IsNetworkAlive, syncmgr.isnetworkalive
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: sensapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: SourceSizeList
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	Sensapi.dll
api_name:
-	IsNetworkAlive
product: Windows
targetos: Windows
req.lib: Sensapi.lib
req.dll: Sensapi.dll
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# IsNetworkAlive function


## -description


The 
<b>IsNetworkAlive</b> function determines whether or not a   local system is connected to a network, and identifies the type of network connection, for example, a LAN, WAN, or both.


## -parameters




### -param lpdwFlags [out]

The type of network connection that is available. This parameter can be one of the following values: 







#### NETWORK_ALIVE_LAN

The computer has one or more LAN cards that are active.



#### NETWORK_ALIVE_WAN

The computer has one or more active RAS connections.


## -returns



Always call <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a> before checking the return code of this function.  If the last error is not 0, the <b>IsNetworkAlive</b> function has failed and the following <b>TRUE</b> and <b>FALSE</b> values do not apply.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>TRUE</b></dt>
</dl>
</td>
<td width="60%">
If the last error is 0 and the function returns <b>TRUE</b>, SENS has determined that a  local system is connected to a network. 

For information about the type of connection, see the <i>lpdwFlags</i> parameter.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>FALSE</b></dt>
</dl>
</td>
<td width="60%">
If the last error is 0 and the function returns <b>FALSE</b>, SENS has determined there is no connection. 

</td>
</tr>
</table>
 




## -remarks



Starting with applications designed for Windows Vista and Windows Server 2008, developers should consider using the <a href="https://msdn.microsoft.com/a30741ff-5d9a-4ebb-8373-97e9116fc64b">Network List Manager</a> instead of this function.

This function can be used by an application to determine whether or not there is network connectivity before proceeding with network operations. A directory service type of application, e-mail client, or Internet browser can adapt to various types of network connectivity. For example, a printing operation can be deferred until a network connection is available.

It may not always be practical for an application to call 
<b>IsNetworkAlive</b> to determine whether or not a  local system is disconnected from a LAN, because <b>IsNetworkAlive</b> can be slow, and it may take too much time for the function to detect that a local system is disconnected. 
However, <b>IsNetworkAlive</b> can always identify a WAN connectivity at the moment.

<div class="alert"><b>Note</b>  This function is only available for TCP/IP connections.</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/f313588f-6257-4a0d-b95a-aabc0bc64b53">About System Event Notification Service</a>



<a href="https://msdn.microsoft.com/377af331-8494-4a3d-b822-78c2b568239c">IsDestinationReachable</a>
 

 

