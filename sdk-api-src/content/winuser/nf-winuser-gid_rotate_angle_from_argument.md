---
UID: NF:winuser.GID_ROTATE_ANGLE_FROM_ARGUMENT
title: GID_ROTATE_ANGLE_FROM_ARGUMENT macro (winuser.h)
description: The GID_ROTATE_ANGLE_FROM_ARGUMENT macro is used to interpret the GID_ROTATE ullArgument value when receiving the value in the WM_GESTURE structure.
helpviewer_keywords: ["GID_ROTATE_ANGLE_FROM_ARGUMENT","GID_ROTATE_ANGLE_FROM_ARGUMENT macro [Windows Touch]","wintouch.gci_rotate_angle_from_argument","winuser/GID_ROTATE_ANGLE_FROM_ARGUMENT"]
old-location: wintouch\gci_rotate_angle_from_argument.htm
tech.root: wintouch
ms.assetid: 8967e870-b444-402e-a343-9ac427ce1f07
ms.date: 12/05/2018
ms.keywords: GID_ROTATE_ANGLE_FROM_ARGUMENT, GID_ROTATE_ANGLE_FROM_ARGUMENT macro [Windows Touch], wintouch.gci_rotate_angle_from_argument, winuser/GID_ROTATE_ANGLE_FROM_ARGUMENT
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
 - GID_ROTATE_ANGLE_FROM_ARGUMENT
 - winuser/GID_ROTATE_ANGLE_FROM_ARGUMENT
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
 - GID_ROTATE_ANGLE_FROM_ARGUMENT
---

# GID_ROTATE_ANGLE_FROM_ARGUMENT macro


## -description

The <b>GID_ROTATE_ANGLE_FROM_ARGUMENT</b> macro is used to interpret the 
        <b>GID_ROTATE</b> <i>ullArgument</i> value when receiving
  the value in the <a href="/windows/desktop/wintouch/wm-gesture">WM_GESTURE</a> structure.

## -parameters

### -param _arg_

A value from a <a href="/windows/desktop/wintouch/wm-gesture">WM_GESTURE</a> message.

## -see-also

<a href="/windows/desktop/wintouch/macros">Macros</a>