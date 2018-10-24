---
UID: NE:winuser.tagAR_STATE
title: tagAR_STATE
author: windows-sdk-content
description: Indicates the state of screen auto-rotation for the system. For example, whether auto-rotation is supported, and whether it is enabled by the user.
old-location: base\ar_state.htm
tech.root: ProcThread
ms.assetid: 55BCB2EB-524D-478A-8DCE-53E59DD0822D
ms.author: windowssdkdev
ms.date: 10/19/2018
ms.keywords: "*PAR_STATE, AR_DISABLED, AR_DOCKED, AR_ENABLED, AR_LAPTOP, AR_MULTIMON, AR_NOSENSOR, AR_NOT_SUPPORTED, AR_REMOTESESSION, AR_STATE, AR_STATE enumeration, AR_SUPPRESSED, PAR_STATE, PAR_STATE enumeration pointer, base.ar_state, tagAR_STATE, winuser/AR_DISABLED, winuser/AR_DOCKED, winuser/AR_ENABLED, winuser/AR_LAPTOP, winuser/AR_MULTIMON, winuser/AR_NOSENSOR, winuser/AR_NOT_SUPPORTED, winuser/AR_REMOTESESSION, winuser/AR_STATE, winuser/AR_SUPPRESSED, winuser/PAR_STATE"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - WinUser.h
api_name:
 - AR_STATE
product: Windows
targetos: Windows
req.typenames: AR_STATE, *PAR_STATE
req.redist: 
---

# tagAR_STATE enumeration


## -description


Indicates the state of screen auto-rotation for the system. For example, whether auto-rotation is supported, and whether it is enabled by the user. This enum is a bitwise OR of one or more of the following values.


## -enum-fields




### -field AR_ENABLED

            Auto-rotation is enabled by the user.


### -field AR_DISABLED

Auto-rotation is disabled by the user.


### -field AR_SUPPRESSED

Auto-rotation is currently suppressed by one or more process auto-rotation preferences.


### -field AR_REMOTESESSION

The session is remote, and auto-rotation is temporarily disabled as a result.


### -field AR_MULTIMON

The system has multiple monitors attached, and auto-rotation is temporarily disabled as a result.


### -field AR_NOSENSOR

The system does not have an auto-rotation sensor.


### -field AR_NOT_SUPPORTED

Auto-rotation is not supported with the current system configuration.


### -field AR_DOCKED

The device is docked, and auto-rotation is temporarily disabled as a result.


### -field AR_LAPTOP

The device is in laptop mode, and auto-rotation is temporarily disabled as a result.

