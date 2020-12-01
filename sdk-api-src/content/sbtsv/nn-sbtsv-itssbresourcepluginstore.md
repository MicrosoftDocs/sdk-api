---
UID: NN:sbtsv.ITsSbResourcePluginStore
title: ITsSbResourcePluginStore (sbtsv.h)
description: Exposes methods that enable resource plug-ins to store objects such as sessions and targets.
helpviewer_keywords: ["ITsSbResourcePluginStore","ITsSbResourcePluginStore interface [Remote Desktop Services]","ITsSbResourcePluginStore interface [Remote Desktop Services]","described","sbtsv/ITsSbResourcePluginStore","termserv.itssbresourcepluginstore"]
old-location: termserv\itssbresourcepluginstore.htm
tech.root: TermServ
ms.assetid: b8b54827-6c6b-4531-8ae3-73baed6125cd
ms.date: 12/05/2018
ms.keywords: ITsSbResourcePluginStore, ITsSbResourcePluginStore interface [Remote Desktop Services], ITsSbResourcePluginStore interface [Remote Desktop Services],described, sbtsv/ITsSbResourcePluginStore, termserv.itssbresourcepluginstore
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ITsSbResourcePluginStore
 - sbtsv/ITsSbResourcePluginStore
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - sbtsv.h
api_name:
 - ITsSbResourcePluginStore
---

# ITsSbResourcePluginStore interface


## -description

Exposes methods that enable resource plug-ins to store objects such as sessions and targets. 
    These methods add, delete, and query these objects.

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ITsSbResourcePluginStore</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>ITsSbResourcePluginStore</b> also has these types of members:
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
<a href="/windows/desktop/api/sbtsv/nf-sbtsv-itssbresourcepluginstore-acquiretargetlock">AcquireTargetLock</a>
</td>
<td align="left" width="63%">
Locks a target.

<b>Windows Server 2012 R2 and Windows Server 2012:  </b>This method is unavailable prior to Windows Server 2016. This method is available on 
        Windows Server 2012 R2 with 
        <a href="https://support.microsoft.com/help/3091411/user-connection-fails-when-many-connections-are-made-to-windows-server">KB3091411</a> installed in the 
        <a href="/windows/desktop/TermServ/itssbresourcepluginstoreex">ITsSbResourcePluginStoreEx</a> 
        interface.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/sbtsv/nf-sbtsv-itssbresourcepluginstore-addenvironmenttostore">AddEnvironmentToStore</a>
</td>
<td align="left" width="63%">
Adds an environment to the resource plug-in store.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/sbtsv/nf-sbtsv-itssbresourcepluginstore-addsessiontostore">AddSessionToStore</a>
</td>
<td align="left" width="63%">
Adds a new session to the resource plug-in store.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/sbtsv/nf-sbtsv-itssbresourcepluginstore-addtargettostore">AddTargetToStore</a>
</td>
<td align="left" width="63%">
Adds a target to the resource plug-in store.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/sbtsv/nf-sbtsv-itssbresourcepluginstore-deletetarget">DeleteTarget</a>
</td>
<td align="left" width="63%">
Deletes a target.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/sbtsv/nf-sbtsv-itssbresourcepluginstore-enumerateenvironments">EnumerateEnvironments</a>
</td>
<td align="left" width="63%">
Returns an array that contains the environments present in the resource plug-in store.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/sbtsv/nf-sbtsv-itssbresourcepluginstore-enumeratefarms">EnumerateFarms</a>
</td>
<td align="left" width="63%">
Enumerates all the farms that have been added to the resource plug-in store.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/sbtsv/nf-sbtsv-itssbresourcepluginstore-enumeratesessions">EnumerateSessions</a>
</td>
<td align="left" width="63%">
Enumerates a specified set of sessions.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/sbtsv/nf-sbtsv-itssbresourcepluginstore-enumeratetargets">EnumerateTargets</a>
</td>
<td align="left" width="63%">
Returns an array that contains the specified targets that are present in the resource plug-in store. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/sbtsv/nf-sbtsv-itssbresourcepluginstore-getfarmproperty">GetFarmProperty</a>
</td>
<td align="left" width="63%">
Retrieves a property of a farm.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/sbtsv/nf-sbtsv-itssbresourcepluginstore-getserverstate">GetServerState</a>
</td>
<td align="left" width="63%">
Retrieves the state of a specified server.

<b>Windows Server 2012 R2 and Windows Server 2012:  </b>This method is unavailable prior to Windows Server 2016

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/sbtsv/nf-sbtsv-itssbresourcepluginstore-queryenvironment">QueryEnvironment</a>
</td>
<td align="left" width="63%">
Returns the specified environment object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/sbtsv/nf-sbtsv-itssbresourcepluginstore-querysessionbysessionid">QuerySessionBySessionId</a>
</td>
<td align="left" width="63%">
Returns the session object that has the specified session ID.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/sbtsv/nf-sbtsv-itssbresourcepluginstore-querytarget">QueryTarget</a>
</td>
<td align="left" width="63%">
Returns the target that has the specified target name and farm name.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/sbtsv/nf-sbtsv-itssbresourcepluginstore-releasetargetlock">ReleaseTargetLock</a>
</td>
<td align="left" width="63%">
Releases a lock on a target.

<b>Windows Server 2012 R2 and Windows Server 2012:  </b>This method is unavailable prior to Windows Server 2016. This method is available on 
        Windows Server 2012 R2 with 
        <a href="https://support.microsoft.com/help/3091411/user-connection-fails-when-many-connections-are-made-to-windows-server">KB3091411</a> installed in the 
        <a href="/windows/desktop/TermServ/itssbresourcepluginstoreex">ITsSbResourcePluginStoreEx</a> 
        interface.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/sbtsv/nf-sbtsv-itssbresourcepluginstore-removeenvironmentfromstore">RemoveEnvironmentFromStore</a>
</td>
<td align="left" width="63%">
Removes the specified environment from the resource plug-in store.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/sbtsv/nf-sbtsv-itssbresourcepluginstore-saveenvironment">SaveEnvironment</a>
</td>
<td align="left" width="63%">
Saves an environment.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/sbtsv/nf-sbtsv-itssbresourcepluginstore-savesession">SaveSession</a>
</td>
<td align="left" width="63%">
Saves a session.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/sbtsv/nf-sbtsv-itssbresourcepluginstore-savetarget">SaveTarget</a>
</td>
<td align="left" width="63%">
Saves a target.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/sbtsv/nf-sbtsv-itssbresourcepluginstore-setenvironmentproperty">SetEnvironmentProperty</a>
</td>
<td align="left" width="63%">
Sets a property on an environment.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/sbtsv/nf-sbtsv-itssbresourcepluginstore-setenvironmentpropertywithversioncheck">SetEnvironmentPropertyWithVersionCheck</a>
</td>
<td align="left" width="63%">
Sets a property on an environment.

<b>Windows Server 2012 R2 and Windows Server 2012:  </b>This method is unavailable prior to Windows Server 2016

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/sbtsv/nf-sbtsv-itssbresourcepluginstore-setserverwaitingtostart">SetServerWaitingToStart</a>
</td>
<td align="left" width="63%">
Indicates to the session host that the server is waiting to start.

<b>Windows Server 2012 R2 and Windows Server 2012:  </b>This method is unavailable prior to Windows Server 2016

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/sbtsv/nf-sbtsv-itssbresourcepluginstore-setsessionstate">SetSessionState</a>
</td>
<td align="left" width="63%">
Sets the state of a session.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/sbtsv/nf-sbtsv-itssbresourcepluginstore-settargetproperty">SetTargetProperty</a>
</td>
<td align="left" width="63%">
Sets a property on a target.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/sbtsv/nf-sbtsv-itssbresourcepluginstore-settargetpropertywithversioncheck">SetTargetPropertyWithVersionCheck</a>
</td>
<td align="left" width="63%">
Sets a property on a target.

<b>Windows Server 2012 R2 and Windows Server 2012:  </b>This method is unavailable prior to Windows Server 2016

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/sbtsv/nf-sbtsv-itssbresourcepluginstore-settargetstate">SetTargetState</a>
</td>
<td align="left" width="63%">
Sets the state of a target.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/sbtsv/nf-sbtsv-itssbresourcepluginstore-testandsetserverstate">TestAndSetServerState</a>
</td>
<td align="left" width="63%">
Conditionally sets a new state on a server. 

<b>Windows Server 2012 R2 and Windows Server 2012:  </b>This method is unavailable prior to Windows Server 2016

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/TermServ/remote-desktop-virtualization-interfaces">Remote Desktop Virtualization Interfaces</a>