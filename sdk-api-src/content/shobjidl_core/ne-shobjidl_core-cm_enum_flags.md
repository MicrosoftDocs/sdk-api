---
UID: NE:shobjidl_core.CM_ENUM_FLAGS
title: CM_ENUM_FLAGS (shobjidl_core.h)
description: Used by members of the IColumnManager interface to specify which set of columns are being requested, either all or only those currently visible.
helpviewer_keywords: ["CM_ENUM_ALL","CM_ENUM_FLAGS","CM_ENUM_FLAGS enumeration [Windows Shell]","CM_ENUM_VISIBLE","shell.CM_ENUM_FLAGS","shell_CM_ENUM_FLAGS","shobjidl_core/CM_ENUM_ALL","shobjidl_core/CM_ENUM_FLAGS","shobjidl_core/CM_ENUM_VISIBLE"]
old-location: shell\CM_ENUM_FLAGS.htm
tech.root: shell
ms.assetid: 9706ae59-d172-4518-8090-375b1a0ff4fb
ms.date: 12/05/2018
ms.keywords: CM_ENUM_ALL, CM_ENUM_FLAGS, CM_ENUM_FLAGS enumeration [Windows Shell], CM_ENUM_VISIBLE, shell.CM_ENUM_FLAGS, shell_CM_ENUM_FLAGS, shobjidl_core/CM_ENUM_ALL, shobjidl_core/CM_ENUM_FLAGS, shobjidl_core/CM_ENUM_VISIBLE
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
req.typenames: CM_ENUM_FLAGS
req.redist: 
ms.custom: 19H1
f1_keywords:
 - CM_ENUM_FLAGS
 - shobjidl_core/CM_ENUM_FLAGS
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
 - CM_ENUM_FLAGS
---

# CM_ENUM_FLAGS enumeration


## -description

Used by members of the <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-icolumnmanager">IColumnManager</a> interface to specify which set of columns are being requested, either all or only those currently visible.

## -enum-fields

### -field CM_ENUM_ALL:0x1

Enumerate all.

### -field CM_ENUM_VISIBLE:0x2

Enumerate visible.
