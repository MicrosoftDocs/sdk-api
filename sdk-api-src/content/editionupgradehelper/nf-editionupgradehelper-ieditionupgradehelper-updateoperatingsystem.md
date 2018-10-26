---
UID: NF:editionupgradehelper.IEditionUpgradeHelper.UpdateOperatingSystem
title: IEditionUpgradeHelper::UpdateOperatingSystem
author: windows-sdk-content
description: Upgrades the installed edition of the operating system to the edition that the user purchased in the Windows Store, or gets a genuine copy of the operating system.
old-location: winprog\ieditionupgradehelper_updateoperatingsystem.htm
tech.root: devnotes
ms.assetid: C7A97C7E-654D-4717-975F-41B05F3BE901
ms.author: windowssdkdev
ms.date: 10/25/2018
ms.keywords: IEditionUpgradeHelper interface [Windows API],UpdateOperatingSystem method, IEditionUpgradeHelper.UpdateOperatingSystem, IEditionUpgradeHelper::UpdateOperatingSystem, UpdateOperatingSystem, UpdateOperatingSystem method [Windows API], UpdateOperatingSystem method [Windows API],IEditionUpgradeHelper interface, editionupgradehelper/IEditionUpgradeHelper::UpdateOperatingSystem, winprog.ieditionupgradehelper_updateoperatingsystem
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: editionupgradehelper.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10 [desktop apps only]
req.target-min-winversvr: Windows Server 2016 [desktop apps only]
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
 - IEditionUpgradeHelper.UpdateOperatingSystem
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IEditionUpgradeHelper::UpdateOperatingSystem


## -description


Upgrades the installed edition of the operating system to the edition that the user purchased in the Windows Store, or gets a genuine copy of the operating system.


## -parameters




### -param contentId [in]

The content identifier of the edition of the operating system that the user purchased and which the method should install.

If this edition is a higher edition that the currently installed edition of Windows, this method performs an upgrade to that edition, If this edition is the same edition as the currently installed edition, this method installs a genuine copy of that edition.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



When this method performs an upgrade from the currently installed edition, the method takes the following steps:

<ul>
<li>Upgrades the edition of the operating system to the product that the user purchased from the Windows Store.</li>
<li>Displays a user interface that informs the user of the progress of the upgrade.</li>
<li>Restarts the computer when the upgrade is complete.</li>
<li>Relies on other system components to check the license to when the computer restarts.</li>
</ul>
When this method installs a genuine copy of the operating system, the method takes the following steps:

<ul>
<li>Checks the license that was download from the store before <b>UpdateOperatingSystem</b> was called.</li>
<li>Turns off any user experience that is not genuine for the current edition of Windows.</li>
</ul>



## -see-also




<a href="https://msdn.microsoft.com/8B2776DC-09DE-4E40-96CC-656C4B09A109">CanUpgrade</a>



<a href="https://msdn.microsoft.com/061AECF0-AC7A-480F-B532-F5D8AC078168">GetGenuineLocalStatus</a>



<a href="https://msdn.microsoft.com/79EEDFF2-FDF9-4BC9-968A-3543892AE870">GetOsProductContentId</a>



<a href="https://msdn.microsoft.com/2A243B2F-F7A1-448F-B16D-143514725658">IEditionUpgradeHelper</a>
 

 

