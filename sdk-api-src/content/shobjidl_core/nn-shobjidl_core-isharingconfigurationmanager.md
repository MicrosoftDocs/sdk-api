---
UID: NN:shobjidl_core.ISharingConfigurationManager
title: ISharingConfigurationManager (shobjidl_core.h)
description: Exposes methods that set and retrieve information about a computer's default sharing settings for the Users (C:\Users) or Public (C:\Users\Public) folder. Also exposes a set of methods that allow control of printer sharing.helpviewer_keywords: ["ISharingConfigurationManager","ISharingConfigurationManager interface [Windows Shell]","ISharingConfigurationManager interface [Windows Shell]","described","_shell_ISharingConfigurationManager","shell.ISharingConfigurationManager","shobjidl_core/ISharingConfigurationManager"]
old-location: shell\ISharingConfigurationManager.htm
tech.root: shell
ms.assetid: 64bf628d-4e9b-42a8-a9cf-04d321645d9a
ms.date: 12/05/2018
ms.keywords: ISharingConfigurationManager, ISharingConfigurationManager interface [Windows Shell], ISharingConfigurationManager interface [Windows Shell],described, _shell_ISharingConfigurationManager, shell.ISharingConfigurationManager, shobjidl_core/ISharingConfigurationManager
f1_keywords:
- shobjidl_core/ISharingConfigurationManager
dev_langs:
- c++
req.header: shobjidl_core.h
req.include-header: Shobjidl.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Shobjidl.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- shobjidl_core.h
api_name:
- ISharingConfigurationManager
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ISharingConfigurationManager interface


## -description


Exposes methods that set and retrieve information about a computer's default sharing settings for the <b>Users</b> (<code>C:\Users</code>) or <b>Public</b> (<code>C:\Users\Public</code>) folder. Also exposes a set of methods that allow control of printer sharing.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ISharingConfigurationManager</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>ISharingConfigurationManager</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ISharingConfigurationManager</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-isharingconfigurationmanager-areprintersshared">ArePrintersShared</a>
</td>
<td align="left" width="63%">
Determines whether any printers connected to this computer are shared.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-isharingconfigurationmanager-createshare">CreateShare</a>
</td>
<td align="left" width="63%">
Shares the <b>Users</b> or <b>Public</b> folder. If the folder is already shared, this method updates its sharing status.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-isharingconfigurationmanager-deleteshare">DeleteShare</a>
</td>
<td align="left" width="63%">
Removes sharing from either the <b>Users</b> or <b>Public</b> folder.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-isharingconfigurationmanager-getsharepermissions">GetSharePermissions</a>
</td>
<td align="left" width="63%">
Gets the access permissions currently associated with the <b>User</b> or <b>Public</b> folder for the <i>Everyone</i> ACE.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-isharingconfigurationmanager-shareexists">ShareExists</a>
</td>
<td align="left" width="63%">
Queries whether the <b>Users</b> or <b>Public</b> folder is shared.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-isharingconfigurationmanager-shareprinters">SharePrinters</a>
</td>
<td align="left" width="63%">
Shares all local printers connected to a computer, enabling them to be discovered by other computers on the network.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nf-shobjidl_core-isharingconfigurationmanager-stopsharingprinters">StopSharingPrinters</a>
</td>
<td align="left" width="63%">
Stops sharing all local, shared printers connected to a computer.

</td>
</tr>
</table> 


## -remarks



<h3><a id="When_to_Implement"></a><a id="when_to_implement"></a><a id="WHEN_TO_IMPLEMENT"></a>When to Implement</h3>
An implementation of this interface is included in the <b>CSharingConfiguration</b> class. Third parties do not provide their own implementation.



