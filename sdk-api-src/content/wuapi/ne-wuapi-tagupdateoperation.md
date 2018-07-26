---
UID: NE:wuapi.tagUpdateOperation
title: tagUpdateOperation
author: windows-sdk-content
description: Defines operations that can be attempted on an update.
old-location: wua\updateoperation.htm
old-project: wua_sdk
ms.assetid: 93f38d77-fb8c-4d2e-acc2-f4c06cbc04f8
ms.author: windowssdkdev
ms.date: 07/23/2018
ms.keywords: UpdateOperation, UpdateOperation enumeration [Windows Update Agent], tagUpdateOperation, uoInstallation, uoUninstallation, wua.updateoperation, wuapi/UpdateOperation, wuapi/uoInstallation, wuapi/uoUninstallation
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
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
tech.root: 
req.typenames: UpdateOperation
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Wuapi.h
api_name:
 - UpdateOperation
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# tagUpdateOperation enumeration


## -description


Defines operations that can be attempted on an update.


## -enum-fields




### -field uoInstallation

Under the security context of the caller, install the update on the target computer.


### -field uoUninstallation

Under the security context of the caller, uninstall the updates  from the target computer.

