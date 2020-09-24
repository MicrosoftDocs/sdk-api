---
UID: NS:shobjidl_core.CM_COLUMNINFO
title: CM_COLUMNINFO (shobjidl_core.h)
description: Defines column information. Used by members of the IColumnManager interface.
helpviewer_keywords: ["CM_COLUMNINFO","CM_COLUMNINFO structure [Windows Shell]","shell.CM_COLUMNINFO","shell_CM_COLUMNINFO","shobjidl_core/CM_COLUMNINFO"]
old-location: shell\CM_COLUMNINFO.htm
tech.root: shell
ms.assetid: b4437aa7-9682-4819-a353-936179e84005
ms.date: 12/05/2018
ms.keywords: CM_COLUMNINFO, CM_COLUMNINFO structure [Windows Shell], shell.CM_COLUMNINFO, shell_CM_COLUMNINFO, shobjidl_core/CM_COLUMNINFO
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
req.typenames: CM_COLUMNINFO
req.redist: 
ms.custom: 19H1
f1_keywords:
 - CM_COLUMNINFO
 - shobjidl_core/CM_COLUMNINFO
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
 - CM_COLUMNINFO
---

# CM_COLUMNINFO structure


## -description

Defines column information. Used by members of the <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-icolumnmanager">IColumnManager</a> interface.

## -struct-fields

### -field cbSize

Type: <b>DWORD</b>

The size of the structure, in bytes.

### -field dwMask

Type: <b>DWORD</b>

One or more values from the <a href="/windows/desktop/api/shobjidl_core/ne-shobjidl_core-cm_mask">CM_MASK</a> enumeration that specify which members of this structure are valid.

### -field dwState

Type: <b>DWORD</b>

One or more values from the <a href="/windows/desktop/api/shobjidl_core/ne-shobjidl_core-cm_state">CM_STATE</a> enumeration that specify the state of the column.

### -field uWidth

Type: <b>UINT</b>

One of the members of the <a href="/windows/desktop/api/shobjidl_core/ne-shobjidl_core-cm_set_width_value">CM_SET_WIDTH_VALUE</a> enumeration that specifies the column width.

### -field uDefaultWidth

Type: <b>UINT</b>

The default width of the column.

### -field uIdealWidth

Type: <b>UINT</b>

The ideal width of the column.

### -field wszName

Type: <b>WCHAR[MAX_COLUMN_NAME_LEN]</b>

A buffer of size MAX_COLUMN_NAME_LEN that contains the name of the column as a null-terminated Unicode string.