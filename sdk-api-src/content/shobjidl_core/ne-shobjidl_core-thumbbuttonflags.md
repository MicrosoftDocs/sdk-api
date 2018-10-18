---
UID: NE:shobjidl_core.THUMBBUTTONFLAGS
title: THUMBBUTTONFLAGS
author: windows-sdk-content
description: Used by THUMBBUTTON to control specific states and behaviors of the button.
old-location: shell\THUMBBUTTONFLAGS.htm
tech.root: shell
ms.assetid: 601a2517-cfce-4edb-b2ca-e2ed8a365a0d
ms.author: windowssdkdev
ms.date: 10/17/2018
ms.keywords: THBF_DISABLED, THBF_DISMISSONCLICK, THBF_ENABLED, THBF_HIDDEN, THBF_NOBACKGROUND, THBF_NONINTERACTIVE, THUMBBUTTONFLAGS, THUMBBUTTONFLAGS enumeration [Windows Shell], _shell_THUMBBUTTONFLAGS, shell.THUMBBUTTONFLAGS, shobjidl_core/THBF_DISABLED, shobjidl_core/THBF_DISMISSONCLICK, shobjidl_core/THBF_ENABLED, shobjidl_core/THBF_HIDDEN, shobjidl_core/THBF_NOBACKGROUND, shobjidl_core/THBF_NONINTERACTIVE, shobjidl_core/THUMBBUTTONFLAGS
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
req.header: shobjidl_core.h
req.include-header: Shobjidl.h
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Shobjidl.idl
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
 - shobjidl_core.h
api_name:
 - THUMBBUTTONFLAGS
product: Windows
targetos: Windows
req.typenames: THUMBBUTTONFLAGS
req.redist: 
---

# THUMBBUTTONFLAGS enumeration


## -description


Used by <a href="https://msdn.microsoft.com/c13657b2-5b96-45ae-b339-b06b13aca65d">THUMBBUTTON</a> to control specific states and behaviors of the button.


## -enum-fields




### -field THBF_ENABLED

The button is active and available to the user.


### -field THBF_DISABLED

The button is disabled. It is present, but has a visual state that indicates that it will not respond to user action.


### -field THBF_DISMISSONCLICK

When the button is clicked, the taskbar button's flyout closes immediately.


### -field THBF_NOBACKGROUND

Do not draw a button border, use only the image.


### -field THBF_HIDDEN

The button is not shown to the user.


### -field THBF_NONINTERACTIVE

The button is enabled but not interactive; no pressed button state is drawn. This value is intended for instances where the button is used in a notification.


## -see-also




<a href="https://msdn.microsoft.com/c13657b2-5b96-45ae-b339-b06b13aca65d">THUMBBUTTON</a>



<a href="https://msdn.microsoft.com/12c6a535-6a23-4b41-b4fd-4ed4e192d629">THUMBBUTTONMASK</a>
 

 

