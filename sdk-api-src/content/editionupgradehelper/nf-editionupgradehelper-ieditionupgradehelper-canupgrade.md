---
UID: NF:editionupgradehelper.IEditionUpgradeHelper.CanUpgrade
title: IEditionUpgradeHelper::CanUpgrade (editionupgradehelper.h)
description: Checks if the user has sufficient permissions to upgrade the operating system, and prompts the user to run as an administrator if needed.
helpviewer_keywords: ["CanUpgrade","CanUpgrade method [Windows API]","CanUpgrade method [Windows API]","IEditionUpgradeHelper interface","IEditionUpgradeHelper interface [Windows API]","CanUpgrade method","IEditionUpgradeHelper.CanUpgrade","IEditionUpgradeHelper::CanUpgrade","editionupgradehelper/IEditionUpgradeHelper::CanUpgrade","winprog.ieditionupgradehelper_canupgrade"]
old-location: winprog\ieditionupgradehelper_canupgrade.htm
tech.root: winprog
ms.assetid: 8B2776DC-09DE-4E40-96CC-656C4B09A109
ms.date: 12/05/2018
ms.keywords: CanUpgrade, CanUpgrade method [Windows API], CanUpgrade method [Windows API],IEditionUpgradeHelper interface, IEditionUpgradeHelper interface [Windows API],CanUpgrade method, IEditionUpgradeHelper.CanUpgrade, IEditionUpgradeHelper::CanUpgrade, editionupgradehelper/IEditionUpgradeHelper::CanUpgrade, winprog.ieditionupgradehelper_canupgrade
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IEditionUpgradeHelper::CanUpgrade
 - editionupgradehelper/IEditionUpgradeHelper::CanUpgrade
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - editionupgradehelper.h
api_name:
 - IEditionUpgradeHelper.CanUpgrade
---

# IEditionUpgradeHelper::CanUpgrade


## -description

Checks if the user has sufficient permissions to upgrade the operating system, and prompts the user to run as an administrator if needed.

## -parameters

### -param isAllowed [out]

TRUE if the user has sufficient permissions to upgrade the operating system; otherwise FALSE.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/editionupgradehelper/nn-editionupgradehelper-ieditionupgradehelper">IEditionUpgradeHelper</a>