---
UID: NF:dwmapi.DwmTetherContact
title: DwmTetherContact function (dwmapi.h)
description: Enables the graphical feedback of touch and drag interactions to the user.
helpviewer_keywords: ["DwmTetherContact","DwmTetherContact function [Desktop Window Manager]","dwm.dwmtethercontact","dwmapi/DwmTetherContact"]
old-location: dwm\dwmtethercontact.htm
tech.root: dwm
ms.assetid: 9F7EFFD4-A69A-435B-8B73-A789F7BDE7BB
ms.date: 12/05/2018
ms.keywords: DwmTetherContact, DwmTetherContact function [Desktop Window Manager], dwm.dwmtethercontact, dwmapi/DwmTetherContact
req.header: dwmapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Dwmapi.lib
req.dll: Dwmapi.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - DwmTetherContact
 - dwmapi/DwmTetherContact
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Dwmapi.dll
 - ext-ms-win-dwmapi-ext-l1-1-0.dll
api_name:
 - DwmTetherContact
---

# DwmTetherContact function


## -description

Enables the graphical feedback of touch and drag interactions to the user.

## -parameters

### -param dwPointerID [in]

The pointer ID.

### -param fEnable [in]

Indicates whether the contact is enabled.

### -param ptTether [in]

The tether.

