---
UID: NE:shobjidl_core.CM_STATE
title: CM_STATE (shobjidl_core.h)
description: Specifies column state values. Used by members of the IColumnManager interface through the CM_COLUMNINFO structure.
helpviewer_keywords: ["CM_STATE","CM_STATE enumeration [Windows Shell]","CM_STATE_ALWAYSVISIBLE","CM_STATE_FIXEDWIDTH","CM_STATE_NONE","CM_STATE_NOSORTBYFOLDERNESS","CM_STATE_VISIBLE","shell.CM_STATE","shell_CM_STATE","shobjidl_core/CM_STATE","shobjidl_core/CM_STATE_ALWAYSVISIBLE","shobjidl_core/CM_STATE_FIXEDWIDTH","shobjidl_core/CM_STATE_NONE","shobjidl_core/CM_STATE_NOSORTBYFOLDERNESS","shobjidl_core/CM_STATE_VISIBLE"]
old-location: shell\CM_STATE.htm
tech.root: shell
ms.assetid: a614dfdc-9535-40c4-9a17-5ab032113508
ms.date: 12/05/2018
ms.keywords: CM_STATE, CM_STATE enumeration [Windows Shell], CM_STATE_ALWAYSVISIBLE, CM_STATE_FIXEDWIDTH, CM_STATE_NONE, CM_STATE_NOSORTBYFOLDERNESS, CM_STATE_VISIBLE, shell.CM_STATE, shell_CM_STATE, shobjidl_core/CM_STATE, shobjidl_core/CM_STATE_ALWAYSVISIBLE, shobjidl_core/CM_STATE_FIXEDWIDTH, shobjidl_core/CM_STATE_NONE, shobjidl_core/CM_STATE_NOSORTBYFOLDERNESS, shobjidl_core/CM_STATE_VISIBLE
req.header: shobjidl_core.h
req.include-header: Shobjidl.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
req.typenames: CM_STATE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - CM_STATE
 - shobjidl_core/CM_STATE
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
 - CM_STATE
---

# CM_STATE enumeration


## -description

Specifies column state values. Used by members of the <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-icolumnmanager">IColumnManager</a> interface through the <a href="/windows/desktop/api/shobjidl_core/ns-shobjidl_core-cm_columninfo">CM_COLUMNINFO</a> structure.

## -enum-fields

### -field CM_STATE_NONE:0

The column is not currently displayed.

### -field CM_STATE_VISIBLE:0x1

The column is currently displayed.

### -field CM_STATE_FIXEDWIDTH:0x2

The column cannot be resized.

### -field CM_STATE_NOSORTBYFOLDERNESS:0x4

Do not sort folders separately.

### -field CM_STATE_ALWAYSVISIBLE:0x8

The column cannot be hidden.
