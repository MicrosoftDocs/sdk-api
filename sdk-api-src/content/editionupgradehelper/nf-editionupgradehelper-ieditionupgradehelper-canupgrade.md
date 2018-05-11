---
UID: NF:editionupgradehelper.IEditionUpgradeHelper.CanUpgrade
title: IEditionUpgradeHelper::CanUpgrade
author: windows-driver-content
description: Checks if the user has sufficient permissions to upgrade the operating system, and prompts the user to run as an administrator if needed.
old-location: winprog\ieditionupgradehelper_canupgrade.htm
old-project: DevNotes
ms.assetid: 8B2776DC-09DE-4E40-96CC-656C4B09A109
ms.author: windowsdriverdev
ms.date: 5/9/2018
ms.keywords: CanUpgrade, CanUpgrade method [Windows API], CanUpgrade method [Windows API],IEditionUpgradeHelper interface, IEditionUpgradeHelper interface [Windows API],CanUpgrade method, IEditionUpgradeHelper.CanUpgrade, IEditionUpgradeHelper::CanUpgrade, editionupgradehelper/IEditionUpgradeHelper::CanUpgrade, winprog.ieditionupgradehelper_canupgrade
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
req.typenames: EAP_TYPE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	editionupgradehelper.h
api_name:
-	IEditionUpgradeHelper.CanUpgrade
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Media Format 9 Series or later
---

# IEditionUpgradeHelper::CanUpgrade


## -description


Checks if the user has sufficient permissions to upgrade the operating system, and prompts the user to run as an administrator if needed.


## -parameters




### -param isAllowed [out]

TRUE if the user has sufficient permissions to upgrade the operating system; otherwise FALSE.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/2A243B2F-F7A1-448F-B16D-143514725658">IEditionUpgradeHelper</a>
 

 

