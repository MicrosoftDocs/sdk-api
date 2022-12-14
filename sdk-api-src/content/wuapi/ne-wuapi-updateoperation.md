---
UID: NE:wuapi.tagUpdateOperation
title: UpdateOperation (wuapi.h)
description: Defines operations that can be attempted on an update.
helpviewer_keywords: ["UpdateOperation","UpdateOperation enumeration [Windows Update Agent]","uoInstallation","uoUninstallation","wua.updateoperation","wuapi/UpdateOperation","wuapi/uoInstallation","wuapi/uoUninstallation"]
old-location: wua\updateoperation.htm
tech.root: wua
ms.assetid: 93f38d77-fb8c-4d2e-acc2-f4c06cbc04f8
ms.date: 12/05/2018
ms.keywords: UpdateOperation, UpdateOperation enumeration [Windows Update Agent], uoInstallation, uoUninstallation, wua.updateoperation, wuapi/UpdateOperation, wuapi/uoInstallation, wuapi/uoUninstallation
req.header: wuapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP, Windows 2000 Professional with SP3 [desktop apps only]
req.target-min-winversvr: Windows Server 2003, Windows 2000 Server with SP3 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Wuapi.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: UpdateOperation
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tagUpdateOperation
 - wuapi/tagUpdateOperation
 - UpdateOperation
 - wuapi/UpdateOperation
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Wuapi.h
api_name:
 - UpdateOperation
---

# UpdateOperation enumeration


## -description

Defines operations that can be attempted on an update.

## -enum-fields

### -field uoInstallation:1

Under the security context of the caller, install the update on the target computer.

### -field uoUninstallation:2

Under the security context of the caller, uninstall the updates  from the target computer.

