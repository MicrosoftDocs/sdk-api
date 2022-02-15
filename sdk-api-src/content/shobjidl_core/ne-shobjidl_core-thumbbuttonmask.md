---
UID: NE:shobjidl_core.THUMBBUTTONMASK
title: THUMBBUTTONMASK (shobjidl_core.h)
description: Used by the THUMBBUTTON structure to specify which members of that structure contain valid data.
helpviewer_keywords: ["THB_BITMAP","THB_FLAGS","THB_ICON","THB_TOOLTIP","THUMBBUTTONMASK","THUMBBUTTONMASK enumeration [Windows Shell]","_shell_THUMBBUTTONMASK","shell.THUMBBUTTONMASK","shobjidl_core/THB_BITMAP","shobjidl_core/THB_FLAGS","shobjidl_core/THB_ICON","shobjidl_core/THB_TOOLTIP","shobjidl_core/THUMBBUTTONMASK"]
old-location: shell\THUMBBUTTONMASK.htm
tech.root: shell
ms.assetid: 12c6a535-6a23-4b41-b4fd-4ed4e192d629
ms.date: 12/05/2018
ms.keywords: THB_BITMAP, THB_FLAGS, THB_ICON, THB_TOOLTIP, THUMBBUTTONMASK, THUMBBUTTONMASK enumeration [Windows Shell], _shell_THUMBBUTTONMASK, shell.THUMBBUTTONMASK, shobjidl_core/THB_BITMAP, shobjidl_core/THB_FLAGS, shobjidl_core/THB_ICON, shobjidl_core/THB_TOOLTIP, shobjidl_core/THUMBBUTTONMASK
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
targetos: Windows
req.typenames: THUMBBUTTONMASK
req.redist: 
ms.custom: 19H1
f1_keywords:
 - THUMBBUTTONMASK
 - shobjidl_core/THUMBBUTTONMASK
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - shobjidl_core.h
api_name:
 - THUMBBUTTONMASK
---

# THUMBBUTTONMASK enumeration


## -description

Used by the <a href="/windows/desktop/api/shobjidl_core/ns-shobjidl_core-thumbbutton">THUMBBUTTON</a> structure to specify which members of that structure contain valid data.

## -enum-fields

### -field THB_BITMAP:0x1

The <b>iBitmap</b> member contains valid information.

### -field THB_ICON:0x2

The <b>hIcon</b> member contains valid information.

### -field THB_TOOLTIP:0x4

The <b>szTip</b> member contains valid information.

### -field THB_FLAGS:0x8

The <b>dwFlags</b> member contains valid information.

## -see-also

<a href="/windows/desktop/api/shobjidl_core/ns-shobjidl_core-thumbbutton">THUMBBUTTON</a>



<a href="/windows/desktop/api/shobjidl_core/ne-shobjidl_core-thumbbuttonflags">THUMBBUTTONFLAGS</a>
