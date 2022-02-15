---
UID: NF:editionupgradehelper.IEditionUpgradeHelper.GetGenuineLocalStatus
title: IEditionUpgradeHelper::GetGenuineLocalStatus (editionupgradehelper.h)
description: Retrieves whether the currently installed operating system is activated.
helpviewer_keywords: ["GetGenuineLocalStatus","GetGenuineLocalStatus method [Windows API]","GetGenuineLocalStatus method [Windows API]","IEditionUpgradeHelper interface","IEditionUpgradeHelper interface [Windows API]","GetGenuineLocalStatus method","IEditionUpgradeHelper.GetGenuineLocalStatus","IEditionUpgradeHelper::GetGenuineLocalStatus","editionupgradehelper/IEditionUpgradeHelper::GetGenuineLocalStatus","winprog.ieditionupgradehelper_getgenuinelocalstatus"]
old-location: winprog\ieditionupgradehelper_getgenuinelocalstatus.htm
tech.root: winprog
ms.assetid: 061AECF0-AC7A-480F-B532-F5D8AC078168
ms.date: 12/05/2018
ms.keywords: GetGenuineLocalStatus, GetGenuineLocalStatus method [Windows API], GetGenuineLocalStatus method [Windows API],IEditionUpgradeHelper interface, IEditionUpgradeHelper interface [Windows API],GetGenuineLocalStatus method, IEditionUpgradeHelper.GetGenuineLocalStatus, IEditionUpgradeHelper::GetGenuineLocalStatus, editionupgradehelper/IEditionUpgradeHelper::GetGenuineLocalStatus, winprog.ieditionupgradehelper_getgenuinelocalstatus
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
 - IEditionUpgradeHelper::GetGenuineLocalStatus
 - editionupgradehelper/IEditionUpgradeHelper::GetGenuineLocalStatus
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
 - IEditionUpgradeHelper.GetGenuineLocalStatus
---

# IEditionUpgradeHelper::GetGenuineLocalStatus


## -description

Retrieves whether the currently installed operating system is activated.

## -parameters

### -param isGenuine [out]

TRUE is the currently installed operating system is activated; otherwise, FALSE.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/editionupgradehelper/nn-editionupgradehelper-ieditionupgradehelper">IEditionUpgradeHelper</a>