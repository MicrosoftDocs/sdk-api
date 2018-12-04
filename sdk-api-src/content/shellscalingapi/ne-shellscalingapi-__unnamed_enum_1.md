---
UID: NE:shellscalingapi.__unnamed_enum_1
title: SCALE_CHANGE_FLAGS
author: windows-sdk-content
description: Flags that are used to indicate the scaling change that occured.
old-location: shell\scale_change_flags.htm
tech.root: shell
ms.assetid: 18B3E8F1-C9A9-4CE4-8982-C552486EA9B1
ms.author: windowssdkdev
ms.date: 11/30/2018
ms.keywords: SCALE_CHANGE_FLAGS, SCALE_CHANGE_FLAGS enumeration [Windows Shell], SCF_PHYSICAL, SCF_SCALE, SCF_VALUE_NONE, shell.scale_change_flags, shellscalingapi/SCALE_CHANGE_FLAGS, shellscalingapi/SCF_PHYSICAL, shellscalingapi/SCF_SCALE, shellscalingapi/SCF_VALUE_NONE
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: enum
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - ShellScalingAPI.h
api_name:
 - SCALE_CHANGE_FLAGS
product: Windows
targetos: Windows
req.typenames: SCALE_CHANGE_FLAGS
req.redist: 
---

# SCALE_CHANGE_FLAGS enumeration


## -description


Flags that are used to indicate the scaling change that occured.


## -enum-fields




### -field SCF_VALUE_NONE

No change.


### -field SCF_SCALE

The scale factor has changed.


### -field SCF_PHYSICAL

The physical dpi of the device has changed. A change in the physical dpi is generally caused either by switching display devices or switching display resolutions.

