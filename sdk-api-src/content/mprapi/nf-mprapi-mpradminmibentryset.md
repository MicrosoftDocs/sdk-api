---
UID: NF:mprapi.MprAdminMIBEntrySet
title: MprAdminMIBEntrySet function (mprapi.h)
author: windows-sdk-content
description: The MprAdminMIBEntrySet function sets the value of one of the variables exported by a routing protocol or router manager.
old-location: rras\mpradminmibentryset.htm
tech.root: RRAS
ms.assetid: 53dabf73-b9c5-4245-9269-bd7c6ce00026
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: MprAdminMIBEntrySet, MprAdminMIBEntrySet function [RAS], _mpr_mpradminmibentryset, mprapi/MprAdminMIBEntrySet, rras.mpradminmibentryset
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
req.lib: Mprapi.lib
req.dll: Mprapi.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Mprapi.dll
api_name:
 - MprAdminMIBEntrySet
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# MprAdminMIBEntrySet function


## -description


The 
<b>MprAdminMIBEntrySet</b> function sets the value of one of the variables exported by a routing protocol or router manager.


## -parameters




### -param hMibServer [in]

Handle to the router on which to execute this call. Obtain this handle by calling 
<a href="https://msdn.microsoft.com/8d8cba34-e5d3-42ae-9724-361802f21410">MprAdminMIBServerConnect</a>.


### -param dwProtocolId [in]

Specifies the 
<a href="https://msdn.microsoft.com/7720c34f-0558-49de-8f82-13a67e2c8c69">router manager</a> that exported the variable.


### -param dwRoutingPid [in]

Specifies the 
<a href="https://msdn.microsoft.com/f67138b8-de5d-4907-a464-672d57864ebf">routing protocol</a> that exported the variable.


### -param lpEntry [in]

Pointer to an opaque data 
<a href="https://msdn.microsoft.com/811a1e41-efce-4e9c-8329-1c6929e12a8d">structure</a>. The data structure's format is determined by the module that services the call. The data structure should contain information that specifies the variable being set and the value to be assigned to the variable.


### -param dwEntrySize [in]

Specifies the size, in bytes, of the data pointed to by the <i>lpEntry</i> parameter.


## -returns



If the function succeeds, the return value is NO_ERROR.

If the function fails, the return value is one of the following values.

<table>
<tr>
<th>Value</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_ACCESS_DENIED</b></dt>
</dl>
</td>
<td width="60%">
The caller does not have sufficient privileges.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_CANNOT_COMPLETE</b></dt>
</dl>
</td>
<td width="60%">
The <i>dwRoutingPid</i> variable does not match any installed routing protocol.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_UNKNOWN_PROTOCOL_ID</b></dt>
</dl>
</td>
<td width="60%">
The <i>dwTransportId</i> value does not match any installed router manager.

</td>
</tr>
</table>
 




## -remarks



Do not pass in <b>NULL</b> for the <i>lpEntry</i> parameter because the resulting behavior is undefined.




## -see-also




<a href="https://msdn.microsoft.com/811a1e41-efce-4e9c-8329-1c6929e12a8d">MIB Structures</a>



<a href="https://msdn.microsoft.com/98e88364-4757-4b43-8316-6d4d9b3c2f29">MprAdminMIBEntryGet</a>



<a href="https://msdn.microsoft.com/8d8cba34-e5d3-42ae-9724-361802f21410">MprAdminMIBServerConnect</a>



<a href="https://msdn.microsoft.com/f67138b8-de5d-4907-a464-672d57864ebf">Protocol Identifiers</a>



<a href="https://msdn.microsoft.com/c911daa4-4f3d-4944-9dc0-695a4efbcb1b">Router Management MIB Functions</a>



<a href="https://msdn.microsoft.com/a7a28ac0-c6f9-450c-9925-67990a62ba08">Router Management MIB Reference</a>



<a href="https://msdn.microsoft.com/7720c34f-0558-49de-8f82-13a67e2c8c69">Transport Identifiers</a>
 

 

