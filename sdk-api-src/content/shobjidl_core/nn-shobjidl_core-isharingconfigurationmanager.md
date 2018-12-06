---
UID: NN:shobjidl_core.ISharingConfigurationManager
title: ISharingConfigurationManager
author: windows-sdk-content
description: Exposes methods that set and retrieve information about a computer's default sharing settings for the Users (C:\Users) or Public (C:\Users\Public) folder. Also exposes a set of methods that allow control of printer sharing.
old-location: shell\ISharingConfigurationManager.htm
tech.root: shell
ms.assetid: 64bf628d-4e9b-42a8-a9cf-04d321645d9a
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: ISharingConfigurationManager, ISharingConfigurationManager interface [Windows Shell], ISharingConfigurationManager interface [Windows Shell],described, _shell_ISharingConfigurationManager, shell.ISharingConfigurationManager, shobjidl_core/ISharingConfigurationManager
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: interface
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ISharingConfigurationManager interface


## -description


Exposes methods that set and retrieve information about a computer's default sharing settings for the <b>Users</b> (<code>C:\Users</code>) or <b>Public</b> (<code>C:\Users\Public</code>) folder. Also exposes a set of methods that allow control of printer sharing.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ISharingConfigurationManager</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>ISharingConfigurationManager</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/331ccf4d-c769-43b9-a2db-c464ffaef58e">ArePrintersShared</a>
</td>
<td align="left" width="63%">
Determines whether any printers connected to this computer are shared.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/81bcd470-3fb8-4c6d-af4f-6f11206fa40a">CreateShare</a>
</td>
<td align="left" width="63%">
Shares the <b>Users</b> or <b>Public</b> folder. If the folder is already shared, this method updates its sharing status.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/8b78d321-0da6-4b7e-8408-34784d309a1b">DeleteShare</a>
</td>
<td align="left" width="63%">
Removes sharing from either the <b>Users</b> or <b>Public</b> folder.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d9ca5acf-2dd1-4fbe-a67f-91578d68b955">GetSharePermissions</a>
</td>
<td align="left" width="63%">
Gets the access permissions currently associated with the <b>User</b> or <b>Public</b> folder for the <i>Everyone</i> ACE.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d15d40a1-fdde-430a-bb8c-537ce58536dd">ShareExists</a>
</td>
<td align="left" width="63%">
Queries whether the <b>Users</b> or <b>Public</b> folder is shared.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/bc8d3b2b-88b6-4c2d-a3c2-94bba245708c">SharePrinters</a>
</td>
<td align="left" width="63%">
Shares all local printers connected to a computer, enabling them to be discovered by other computers on the network.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/dfb5a6a6-3530-4925-bbe8-d67c2537ef4e">StopSharingPrinters</a>
</td>
<td align="left" width="63%">
Stops sharing all local, shared printers connected to a computer.

</td>
</tr>
</table> 


## -remarks



<h3><a id="When_to_Implement"></a><a id="when_to_implement"></a><a id="WHEN_TO_IMPLEMENT"></a>When to Implement</h3>
An implementation of this interface is included in the <b>CSharingConfiguration</b> class. Third parties do not provide their own implementation.



