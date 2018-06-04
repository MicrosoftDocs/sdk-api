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

# IEditionUpgradeHelper interface


## -description


Allows the Windows Store to install a Windows product that the user purchased, to perform either an upgrade to the edition of Windows that the user currently has installed, or to replace a non-genuine copy of Windows with a genuine copy of Windows.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IEditionUpgradeHelper</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IEditionUpgradeHelper</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IEditionUpgradeHelper</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/8B2776DC-09DE-4E40-96CC-656C4B09A109">CanUpgrade</a>
</td>
<td align="left" width="63%">
Checks if the user has sufficient permissions to upgrade the operating system, and prompts the user to run as an administrator if needed.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/061AECF0-AC7A-480F-B532-F5D8AC078168">GetGenuineLocalStatus</a>
</td>
<td align="left" width="63%">
Retrieves whether the currently installed operating system is activated.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/79EEDFF2-FDF9-4BC9-968A-3543892AE870">GetOsProductContentId</a>
</td>
<td align="left" width="63%">
Retrieves the content identifier that corresponds to the current installation of the operating system. The content identifier is used to look up the operating system product in the store catalog.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/504B3699-8837-4C14-959A-B3B4385E8932">ShowProductKeyUI</a>
</td>
<td align="left" width="63%">
Displays the user interface through which the user  can provide a product key to upgrade or get a genuine copy of the operating system.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/C7A97C7E-654D-4717-975F-41B05F3BE901">UpdateOperatingSystem</a>
</td>
<td align="left" width="63%">
Upgrades the installed edition of the operating system to the edition that the user purchased in the Windows Store, or gets a genuine copy of the operating system.

</td>
</tr>
</table> 


## -remarks



The methods of this interface do not download the binaries or bits necessary to perform the upgrade.



