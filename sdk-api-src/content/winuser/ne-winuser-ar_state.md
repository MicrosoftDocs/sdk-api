---
UID: NE:winuser.tagAR_STATE
title: AR_STATE (winuser.h)
description: Indicates the state of screen auto-rotation for the system. For example, whether auto-rotation is supported, and whether it is enabled by the user.
helpviewer_keywords: ["*PAR_STATE","AR_DISABLED","AR_DOCKED","AR_ENABLED","AR_LAPTOP","AR_MULTIMON","AR_NOSENSOR","AR_NOT_SUPPORTED","AR_REMOTESESSION","AR_STATE","AR_STATE enumeration","AR_SUPPRESSED","PAR_STATE","PAR_STATE enumeration pointer","base.ar_state","winuser/AR_DISABLED","winuser/AR_DOCKED","winuser/AR_ENABLED","winuser/AR_LAPTOP","winuser/AR_MULTIMON","winuser/AR_NOSENSOR","winuser/AR_NOT_SUPPORTED","winuser/AR_REMOTESESSION","winuser/AR_STATE","winuser/AR_SUPPRESSED","winuser/PAR_STATE"]
old-location: base\ar_state.htm
tech.root: backup
ms.assetid: 55BCB2EB-524D-478A-8DCE-53E59DD0822D
ms.date: 12/05/2018
ms.keywords: '*PAR_STATE, AR_DISABLED, AR_DOCKED, AR_ENABLED, AR_LAPTOP, AR_MULTIMON, AR_NOSENSOR, AR_NOT_SUPPORTED, AR_REMOTESESSION, AR_STATE, AR_STATE enumeration, AR_SUPPRESSED, PAR_STATE, PAR_STATE enumeration pointer, base.ar_state, winuser/AR_DISABLED, winuser/AR_DOCKED, winuser/AR_ENABLED, winuser/AR_LAPTOP, winuser/AR_MULTIMON, winuser/AR_NOSENSOR, winuser/AR_NOT_SUPPORTED, winuser/AR_REMOTESESSION, winuser/AR_STATE, winuser/AR_SUPPRESSED, winuser/PAR_STATE'
req.header: winuser.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
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
req.typenames: AR_STATE, *PAR_STATE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tagAR_STATE
 - winuser/tagAR_STATE
 - PAR_STATE
 - winuser/PAR_STATE
 - AR_STATE
 - winuser/AR_STATE
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - WinUser.h
api_name:
 - AR_STATE
---

# AR_STATE enumeration


## -description

Indicates the state of screen auto-rotation for the system. For example, whether auto-rotation is supported, and whether it is enabled by the user. This enum is a bitwise OR of one or more of the following values.

## -enum-fields

### -field AR_ENABLED:0x0

            Auto-rotation is enabled by the user.

### -field AR_DISABLED:0x1

Auto-rotation is disabled by the user.

### -field AR_SUPPRESSED:0x2

Auto-rotation is currently suppressed by one or more process auto-rotation preferences.

### -field AR_REMOTESESSION:0x4

The session is remote, and auto-rotation is temporarily disabled as a result.

### -field AR_MULTIMON:0x8

The system has multiple monitors attached, and auto-rotation is temporarily disabled as a result.

### -field AR_NOSENSOR:0x10

The system does not have an auto-rotation sensor.

### -field AR_NOT_SUPPORTED:0x20

Auto-rotation is not supported with the current system configuration.

### -field AR_DOCKED:0x40

The device is docked, and auto-rotation is temporarily disabled as a result.

### -field AR_LAPTOP:0x80

The device is in laptop mode, and auto-rotation is temporarily disabled as a result.

