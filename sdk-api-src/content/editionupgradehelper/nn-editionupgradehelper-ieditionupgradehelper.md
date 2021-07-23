---
UID: NN:editionupgradehelper.IEditionUpgradeHelper
title: IEditionUpgradeHelper (editionupgradehelper.h)
description: Allows the Windows Store to install a Windows product that the user purchased, to perform either an upgrade to the edition of Windows that the user currently has installed, or to replace a non-genuine copy of Windows with a genuine copy of Windows.
helpviewer_keywords: ["IEditionUpgradeHelper","IEditionUpgradeHelper interface [Windows API]","IEditionUpgradeHelper interface [Windows API]","described","editionupgradehelper/IEditionUpgradeHelper","winprog.ieditionupgradehelper"]
old-location: winprog\ieditionupgradehelper.htm
tech.root: winprog
ms.assetid: 2A243B2F-F7A1-448F-B16D-143514725658
ms.date: 12/05/2018
ms.keywords: IEditionUpgradeHelper, IEditionUpgradeHelper interface [Windows API], IEditionUpgradeHelper interface [Windows API],described, editionupgradehelper/IEditionUpgradeHelper, winprog.ieditionupgradehelper
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IEditionUpgradeHelper
 - editionupgradehelper/IEditionUpgradeHelper
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
 - IEditionUpgradeHelper
---

# IEditionUpgradeHelper interface


## -description

Allows the Windows Store to install a Windows product that the user purchased, to perform either an upgrade to the edition of Windows that the user currently has installed, or to replace a non-genuine copy of Windows with a genuine copy of Windows.

## -inheritance

The <b>IEditionUpgradeHelper</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IEditionUpgradeHelper</b> also has these types of members:

## -remarks

The methods of this interface do not download the binaries or bits necessary to perform the upgrade.
