---
UID: NF:winuser.GID_ROTATE_ANGLE_TO_ARGUMENT
title: GID_ROTATE_ANGLE_TO_ARGUMENT macro (winuser.h)
description: Converts a radian value to an argument for rotation gesture messages.
helpviewer_keywords: ["GID_ROTATE_ANGLE_TO_ARGUMENT","GID_ROTATE_ANGLE_TO_ARGUMENT macro [Windows Touch]","wintouch.gci_rotate_angle_to_argument","winuser/GID_ROTATE_ANGLE_TO_ARGUMENT"]
old-location: wintouch\gci_rotate_angle_to_argument.htm
tech.root: wintouch
ms.assetid: 058c914e-82c7-40f9-8d0d-2a6a8e77cee0
ms.date: 12/05/2018
ms.keywords: GID_ROTATE_ANGLE_TO_ARGUMENT, GID_ROTATE_ANGLE_TO_ARGUMENT macro [Windows Touch], wintouch.gci_rotate_angle_to_argument, winuser/GID_ROTATE_ANGLE_TO_ARGUMENT
req.header: winuser.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
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
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - GID_ROTATE_ANGLE_TO_ARGUMENT
 - winuser/GID_ROTATE_ANGLE_TO_ARGUMENT
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - winuser.h
api_name:
 - GID_ROTATE_ANGLE_TO_ARGUMENT
---

# GID_ROTATE_ANGLE_TO_ARGUMENT macro


## -description

Converts a radian value to an argument for rotation gesture messages.

## -parameters

### -param _arg_

The angle of rotation as a double in radians.

## -remarks

<div class="alert"><b>Note</b>  The macro assumes that the input value for the radian value is between -2*pi and 2*pi.</div>
<div> </div>

## -see-also

<a href="/windows/desktop/wintouch/macros">Macros</a>