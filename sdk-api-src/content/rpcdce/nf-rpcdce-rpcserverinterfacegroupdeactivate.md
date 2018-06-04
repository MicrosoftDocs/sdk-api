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

# RpcServerInterfaceGroupDeactivate function


## -description


The <b>RpcServerInterfaceGroupDeactivate</b> function tells the RPC runtime to attempt to close the given interface group, optionally aborting the operation if there is outstanding client activity.


## -parameters




### -param IfGroup [in]

A <b>RPC_INTERFACE_GROUP</b> from <a href="https://msdn.microsoft.com/7B648221-8256-42C9-B200-0EFD3B0DBA91">RpcServerInterfaceGroupCreate</a> that defines the interface group to deactivate


### -param ForceDeactivation [in]

If <b>TRUE</b>, the RPC runtime should ignore client activity and unconditionally deactivate the interface group.  If <b>FALSE</b>, the operation should be aborted if new activity takes place.


## -returns



<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>RPC_S_OK</b></dt>
</dl>
</td>
<td width="60%">
The call succeeded.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>RPC_S_SERVER_TOO_BUSY</b></dt>
</dl>
</td>
<td width="60%">
<i>ForceDeactivation</i> is <b>FALSE</b> and there is outstanding client activity.

</td>
</tr>
</table>
 

<div class="alert"><b>Note</b>  For a list of valid error codes, see 
<a href="https://msdn.microsoft.com/0223aa7a-b0cf-49e3-9f08-90be5ccffbd1">RPC Return Values</a>.</div>
<div> </div>



## -remarks



<b>RpcServerInterfaceGroupDeactivate</b> is used by server applications to unregister the interfaces and endpoints in an interface group.  It does the bulk of the shutdown work that RPC server applications need to do.  It performs the following operations:<ul>
<li>Unregisters the endpoints and interfaces from the RPC endpoint mapper.</li>
<li>Unregisters the endpoints from the server runtime.</li>
<li>Unregisters the interfaces from the server runtime.  </li>
<li>Tells the runtime to stop listening for calls if no other interfaces are present.</li>
</ul>


If <i>ForceDeactivation</i> is <b>FALSE</b>, <b>RpcServerInterfaceGroupDeactivate</b> will only deactivate the interface group if there is no outstanding client activity.  If new activity arrives during the deactivation process, <b>RPC_S_SERVER_TOO_BUSY</b> is returned.  In this case, the operation is rolled back and the interface group will continue to receive and dispatch calls.

If <i>ForceDeactivation</i> is <b>TRUE</b>, <b>RpcServerInterfaceGroupDeactivate</b> does not fail.

Service applications can call <b>RpcServerInterfaceGroupDeactivate</b> with <i>ForceDeactivation</i> set to <b>FALSE</b> from their idle callback function <a href="https://msdn.microsoft.com/7B648221-8256-42C9-B200-0EFD3B0DBA91">RpcServerInterfaceGroupCreate</a>.  When used in conjunction with RPC service start triggers, this enables them to safely idle stop without missing calls from potential clients.




## -see-also




<a href="https://msdn.microsoft.com/A467DDEC-BEB1-4050-B540-4A1E819E7373">RpcServerInterfaceGroupActivate</a>



<a href="https://msdn.microsoft.com/DD7F12FC-EDB3-48C3-A87D-9ABAB4EFA009">RpcServerInterfaceGroupClose</a>



<a href="https://msdn.microsoft.com/7B648221-8256-42C9-B200-0EFD3B0DBA91">RpcServerInterfaceGroupCreate</a>



<a href="https://msdn.microsoft.com/90535A05-9835-45F2-A62F-718736A80ED3">RpcServerInterfaceGroupInqBindings</a>
 

 

