---
UID: NN:editionupgradehelper.IEditionUpgradeHelper
title: IEditionUpgradeHelper (editionupgradehelper.h)
description: Allows the Windows Store to install a Windows product that the user purchased, to perform either an upgrade to the edition of Windows that the user currently has installed, or to replace a non-genuine copy of Windows with a genuine copy of Windows.helpviewer_keywords: ["IEditionUpgradeHelper","IEditionUpgradeHelper interface [Windows API]","IEditionUpgradeHelper interface [Windows API]","described","editionupgradehelper/IEditionUpgradeHelper","winprog.ieditionupgradehelper"]
old-location: winprog\ieditionupgradehelper.htm
tech.root: DevNotes
ms.assetid: 2A243B2F-F7A1-448F-B16D-143514725658
ms.date: 12/05/2018
ms.keywords: IEditionUpgradeHelper, IEditionUpgradeHelper interface [Windows API], IEditionUpgradeHelper interface [Windows API],described, editionupgradehelper/IEditionUpgradeHelper, winprog.ieditionupgradehelper
f1_keywords:
- editionupgradehelper/IEditionUpgradeHelper
dev_langs:
- c++
req.header: editionupgradehelper.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2016 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Editionupgradehelper.idl
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
- editionupgradehelper.h
api_name:
- IEditionUpgradeHelper
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IEditionUpgradeHelper interface


## -description


Allows the Windows Store to install a Windows product that the user purchased, to perform either an upgrade to the edition of Windows that the user currently has installed, or to replace a non-genuine copy of Windows with a genuine copy of Windows.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IEditionUpgradeHelper</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IEditionUpgradeHelper</b> also has these types of members:
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
<a href="https://docs.microsoft.com/windows/desktop/api/editionupgradehelper/nf-editionupgradehelper-ieditionupgradehelper-canupgrade">CanUpgrade</a>
</td>
<td align="left" width="63%">
Checks if the user has sufficient permissions to upgrade the operating system, and prompts the user to run as an administrator if needed.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/editionupgradehelper/nf-editionupgradehelper-ieditionupgradehelper-getgenuinelocalstatus">GetGenuineLocalStatus</a>
</td>
<td align="left" width="63%">
Retrieves whether the currently installed operating system is activated.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/editionupgradehelper/nf-editionupgradehelper-ieditionupgradehelper-getosproductcontentid">GetOsProductContentId</a>
</td>
<td align="left" width="63%">
Retrieves the content identifier that corresponds to the current installation of the operating system. The content identifier is used to look up the operating system product in the store catalog.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/editionupgradehelper/nf-editionupgradehelper-ieditionupgradehelper-showproductkeyui">ShowProductKeyUI</a>
</td>
<td align="left" width="63%">
Displays the user interface through which the user  can provide a product key to upgrade or get a genuine copy of the operating system.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/editionupgradehelper/nf-editionupgradehelper-ieditionupgradehelper-updateoperatingsystem">UpdateOperatingSystem</a>
</td>
<td align="left" width="63%">
Upgrades the installed edition of the operating system to the edition that the user purchased in the Windows Store, or gets a genuine copy of the operating system.

</td>
</tr>
</table> 


## -remarks



The methods of this interface do not download the binaries or bits necessary to perform the upgrade.



