---
UID: NE:shellscalingapi.__unnamed_enum_1
title: SCALE_CHANGE_FLAGS (shellscalingapi.h)
description: Flags that are used to indicate the scaling change that occurred.
helpviewer_keywords: ["SCALE_CHANGE_FLAGS","SCALE_CHANGE_FLAGS enumeration [Windows Shell]","SCF_PHYSICAL","SCF_SCALE","SCF_VALUE_NONE","shell.scale_change_flags","shellscalingapi/SCALE_CHANGE_FLAGS","shellscalingapi/SCF_PHYSICAL","shellscalingapi/SCF_SCALE","shellscalingapi/SCF_VALUE_NONE"]
old-location: shell\scale_change_flags.htm
tech.root: shell
ms.assetid: 18B3E8F1-C9A9-4CE4-8982-C552486EA9B1
ms.date: 12/05/2018
ms.keywords: SCALE_CHANGE_FLAGS, SCALE_CHANGE_FLAGS enumeration [Windows Shell], SCF_PHYSICAL, SCF_SCALE, SCF_VALUE_NONE, shell.scale_change_flags, shellscalingapi/SCALE_CHANGE_FLAGS, shellscalingapi/SCF_PHYSICAL, shellscalingapi/SCF_SCALE, shellscalingapi/SCF_VALUE_NONE
req.header: shellscalingapi.h
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: SCALE_CHANGE_FLAGS
req.redist: 
ms.custom: 19H1
f1_keywords:
 - SCALE_CHANGE_FLAGS
 - shellscalingapi/SCALE_CHANGE_FLAGS
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - ShellScalingAPI.h
api_name:
 - SCALE_CHANGE_FLAGS
---

# SCALE_CHANGE_FLAGS enumeration


## -description

Flags that are used to indicate the scaling change that occurred.

## -enum-fields

### -field SCF_VALUE_NONE:0x00

No change.

### -field SCF_SCALE:0x01

The scale factor has changed.

### -field SCF_PHYSICAL:0x02

The physical dpi of the device has changed. A change in the physical dpi is generally caused either by switching display devices or switching display resolutions.

