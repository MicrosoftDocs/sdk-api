---
UID: NE:shobjidl_core.CM_MASK
title: CM_MASK (shobjidl_core.h)
description: Indicates which values in the CM_COLUMNINFO structure should be set during calls to IColumnManager::SetColumnInfo.
helpviewer_keywords: ["CM_MASK","CM_MASK enumeration [Windows Shell]","CM_MASK_DEFAULTWIDTH","CM_MASK_IDEALWIDTH","CM_MASK_NAME","CM_MASK_STATE","CM_MASK_WIDTH","shell.CM_MASK","shell_CM_MASK","shobjidl_core/CM_MASK","shobjidl_core/CM_MASK_DEFAULTWIDTH","shobjidl_core/CM_MASK_IDEALWIDTH","shobjidl_core/CM_MASK_NAME","shobjidl_core/CM_MASK_STATE","shobjidl_core/CM_MASK_WIDTH"]
old-location: shell\CM_MASK.htm
tech.root: shell
ms.assetid: c6ba9410-7c56-428c-9ad9-4e769c047863
ms.date: 12/05/2018
ms.keywords: CM_MASK, CM_MASK enumeration [Windows Shell], CM_MASK_DEFAULTWIDTH, CM_MASK_IDEALWIDTH, CM_MASK_NAME, CM_MASK_STATE, CM_MASK_WIDTH, shell.CM_MASK, shell_CM_MASK, shobjidl_core/CM_MASK, shobjidl_core/CM_MASK_DEFAULTWIDTH, shobjidl_core/CM_MASK_IDEALWIDTH, shobjidl_core/CM_MASK_NAME, shobjidl_core/CM_MASK_STATE, shobjidl_core/CM_MASK_WIDTH
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
req.typenames: CM_MASK
req.redist: 
ms.custom: 19H1
f1_keywords:
 - CM_MASK
 - shobjidl_core/CM_MASK
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
 - CM_MASK
---

# CM_MASK enumeration


## -description

Indicates which values in the <a href="/windows/desktop/api/shobjidl_core/ns-shobjidl_core-cm_columninfo">CM_COLUMNINFO</a> structure should be set during calls to <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icolumnmanager-setcolumninfo">IColumnManager::SetColumnInfo</a>.

## -enum-fields

### -field CM_MASK_WIDTH:0x1

The <b>uWidth</b> member is specified.

### -field CM_MASK_DEFAULTWIDTH:0x2

The <b>uDefaultWidth</b> member is specified.

### -field CM_MASK_IDEALWIDTH:0x4

The <b>uIdealWidth</b> member is specified.

### -field CM_MASK_NAME:0x8

The <b>wszName</b> member is specified.

### -field CM_MASK_STATE:0x10

The <b>dwState</b> member is specified.
