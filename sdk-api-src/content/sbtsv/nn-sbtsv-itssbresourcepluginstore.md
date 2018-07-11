---
UID: NN:sbtsv.ITsSbResourcePluginStore
title: ITsSbResourcePluginStore
author: windows-sdk-content
description: Exposes methods that enable resource plug-ins to store objects such as sessions and targets.
old-location: termserv\itssbresourcepluginstore.htm
old-project: TermServ
ms.assetid: b8b54827-6c6b-4531-8ae3-73baed6125cd
ms.author: windowssdkdev
ms.date: 07/09/2018
ms.keywords: ITsSbResourcePluginStore, ITsSbResourcePluginStore interface [Remote Desktop Services], ITsSbResourcePluginStore interface [Remote Desktop Services],described, sbtsv/ITsSbResourcePluginStore, termserv.itssbresourcepluginstore
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: sbtsv.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2012
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Sbtsv.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: TS_SB_SORT_BY
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - sbtsv.h
api_name:
 - ITsSbResourcePluginStore
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: ADAM
---

# ITsSbResourcePluginStore interface


## -description


Exposes methods that enable resource plug-ins to store objects such as sessions and targets. 
    These methods add, delete, and query these objects.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ITsSbResourcePluginStore</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>ITsSbResourcePluginStore</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ITsSbResourcePluginStore</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ee6f22cf-c111-4a11-ab84-b52904a148b6">AcquireTargetLock</a>
</td>
<td align="left" width="63%">
Locks a target.

<b>Windows Server 2012 R2 and Windows Server 2012:  </b>This method is unavailable prior to Windows Server 2016. This method is available on 
        Windows Server 2012 R2 with 
        <a href="https://support.microsoft.com/en-us/kb/3091411">KB3091411</a> installed in the 
        <a href="https://msdn.microsoft.com/768a5a4e-8221-417a-ad65-9a213a176eca">ITsSbResourcePluginStoreEx</a> 
        interface.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/5f1d995b-10de-4754-9160-fb93a9d8f263">AddEnvironmentToStore</a>
</td>
<td align="left" width="63%">
Adds an environment to the resource plug-in store.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/354ca945-cefe-42f6-a255-9918b8ffc339">AddSessionToStore</a>
</td>
<td align="left" width="63%">
Adds a new session to the resource plug-in store.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/207761eb-b87a-44e5-9101-84d77f95fc23">AddTargetToStore</a>
</td>
<td align="left" width="63%">
Adds a target to the resource plug-in store.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d8114126-f518-4a43-8f6e-900fe84052e5">DeleteTarget</a>
</td>
<td align="left" width="63%">
Deletes a target.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/5c9d2fb4-05e7-449d-8326-b983701b3302">EnumerateEnvironments</a>
</td>
<td align="left" width="63%">
Returns an array that contains the environments present in the resource plug-in store.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/54ed82b2-531c-468b-a4d3-ad299ae1f2d8">EnumerateFarms</a>
</td>
<td align="left" width="63%">
Enumerates all the farms that have been added to the resource plug-in store.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/217b5c28-b0f8-4a8f-8695-8c8e0895b508">EnumerateSessions</a>
</td>
<td align="left" width="63%">
Enumerates a specified set of sessions.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/bb05847a-e7fb-481b-ad84-9f6dc15f9be0">EnumerateTargets</a>
</td>
<td align="left" width="63%">
Returns an array that contains the specified targets that are present in the resource plug-in store. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/83cf8f54-99c2-46fb-b882-e2f3c31240e9">GetFarmProperty</a>
</td>
<td align="left" width="63%">
Retrieves a property of a farm.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/287863fe-55b3-456e-9488-09ee85af2e15">GetServerState</a>
</td>
<td align="left" width="63%">
Retrieves the state of a specified server.

<b>Windows Server 2012 R2 and Windows Server 2012:  </b>This method is unavailable prior to Windows Server 2016

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/1497c638-ba9d-467e-8fbb-8467a43666cc">QueryEnvironment</a>
</td>
<td align="left" width="63%">
Returns the specified environment object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/51a1e876-09fb-4b1c-bb86-028afc46f31e">QuerySessionBySessionId</a>
</td>
<td align="left" width="63%">
Returns the session object that has the specified session ID.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ef78c055-edf6-4f0c-b47c-836ef85310bf">QueryTarget</a>
</td>
<td align="left" width="63%">
Returns the target that has the specified target name and farm name.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/37c22f94-c00d-471b-bd6c-067b3229f99b">ReleaseTargetLock</a>
</td>
<td align="left" width="63%">
Releases a lock on a target.

<b>Windows Server 2012 R2 and Windows Server 2012:  </b>This method is unavailable prior to Windows Server 2016. This method is available on 
        Windows Server 2012 R2 with 
        <a href="https://support.microsoft.com/en-us/kb/3091411">KB3091411</a> installed in the 
        <a href="https://msdn.microsoft.com/768a5a4e-8221-417a-ad65-9a213a176eca">ITsSbResourcePluginStoreEx</a> 
        interface.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/b1922ff2-6322-4868-ab7b-2f18386d7d08">RemoveEnvironmentFromStore</a>
</td>
<td align="left" width="63%">
Removes the specified environment from the resource plug-in store.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/941d5040-e6e4-4f7e-be31-2b52eb16fa9f">SaveEnvironment</a>
</td>
<td align="left" width="63%">
Saves an environment.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/a4f29a99-8478-425d-91d7-c771c35bb2fa">SaveSession</a>
</td>
<td align="left" width="63%">
Saves a session.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/323ac6ee-6a50-433b-85b3-a4409be08226">SaveTarget</a>
</td>
<td align="left" width="63%">
Saves a target.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/a120ff15-2d78-4bca-b470-0eb03933a4d9">SetEnvironmentProperty</a>
</td>
<td align="left" width="63%">
Sets a property on an environment.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/9c4caee8-85fb-4d8f-9c5a-b82eea02a1d0">SetEnvironmentPropertyWithVersionCheck</a>
</td>
<td align="left" width="63%">
Sets a property on an environment.

<b>Windows Server 2012 R2 and Windows Server 2012:  </b>This method is unavailable prior to Windows Server 2016

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/cf677be1-387b-4a63-902b-bacda8729b23">SetServerWaitingToStart</a>
</td>
<td align="left" width="63%">
Indicates to the session host that the server is waiting to start.

<b>Windows Server 2012 R2 and Windows Server 2012:  </b>This method is unavailable prior to Windows Server 2016

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/e6cb83d4-9d85-43d0-812d-ad6e2bdcb067">SetSessionState</a>
</td>
<td align="left" width="63%">
Sets the state of a session.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/11d03b69-a7d0-4930-ba9c-a9373706580c">SetTargetProperty</a>
</td>
<td align="left" width="63%">
Sets a property on a target.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/51b5e267-da1a-4d83-81bc-0cf8fb525fa9">SetTargetPropertyWithVersionCheck</a>
</td>
<td align="left" width="63%">
Sets a property on a target.

<b>Windows Server 2012 R2 and Windows Server 2012:  </b>This method is unavailable prior to Windows Server 2016

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/5ba5c4c6-b644-45f7-8942-ee8ea543138d">SetTargetState</a>
</td>
<td align="left" width="63%">
Sets the state of a target.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/5b209587-090e-4338-95b3-542e50412587">TestAndSetServerState</a>
</td>
<td align="left" width="63%">
Conditionally sets a new state on a server. 

<b>Windows Server 2012 R2 and Windows Server 2012:  </b>This method is unavailable prior to Windows Server 2016

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/150a3c9a-d504-4854-adaa-92e3a7e8ea70">Remote Desktop Virtualization Interfaces</a>
 

 

