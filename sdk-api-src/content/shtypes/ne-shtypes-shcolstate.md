---
UID: NE:shtypes.tagSHCOLSTATE
title: SHCOLSTATE (shtypes.h)
description: Describes how a property should be treated. These values are defined in Shtypes.h.
helpviewer_keywords: ["SHCOLSTATE","SHCOLSTATE enumeration [Windows Shell]","SHCOLSTATE_BATCHREAD","SHCOLSTATE_DEFAULT","SHCOLSTATE_DISPLAYMASK","SHCOLSTATE_EXTENDED","SHCOLSTATE_FIXED_RATIO","SHCOLSTATE_FIXED_WIDTH","SHCOLSTATE_HIDDEN","SHCOLSTATE_NODPISCALE","SHCOLSTATE_NOSORTBYFOLDERNESS","SHCOLSTATE_NO_GROUPBY","SHCOLSTATE_ONBYDEFAULT","SHCOLSTATE_PREFER_FMTCMP","SHCOLSTATE_PREFER_VARCMP","SHCOLSTATE_SECONDARYUI","SHCOLSTATE_SLOW","SHCOLSTATE_TYPEMASK","SHCOLSTATE_TYPE_DATE","SHCOLSTATE_TYPE_INT","SHCOLSTATE_TYPE_STR","SHCOLSTATE_VIEWONLY","shell.SHCOLSTATE","shell_SHCOLSTATE","shtypes/SHCOLSTATE","shtypes/SHCOLSTATE_BATCHREAD","shtypes/SHCOLSTATE_DEFAULT","shtypes/SHCOLSTATE_DISPLAYMASK","shtypes/SHCOLSTATE_EXTENDED","shtypes/SHCOLSTATE_FIXED_RATIO","shtypes/SHCOLSTATE_FIXED_WIDTH","shtypes/SHCOLSTATE_HIDDEN","shtypes/SHCOLSTATE_NODPISCALE","shtypes/SHCOLSTATE_NOSORTBYFOLDERNESS","shtypes/SHCOLSTATE_NO_GROUPBY","shtypes/SHCOLSTATE_ONBYDEFAULT","shtypes/SHCOLSTATE_PREFER_FMTCMP","shtypes/SHCOLSTATE_PREFER_VARCMP","shtypes/SHCOLSTATE_SECONDARYUI","shtypes/SHCOLSTATE_SLOW","shtypes/SHCOLSTATE_TYPEMASK","shtypes/SHCOLSTATE_TYPE_DATE","shtypes/SHCOLSTATE_TYPE_INT","shtypes/SHCOLSTATE_TYPE_STR","shtypes/SHCOLSTATE_VIEWONLY"]
old-location: shell\SHCOLSTATE.htm
tech.root: shell
ms.assetid: 0dee8474-0ae2-41fc-ad58-02d900039ff6
ms.date: 12/05/2018
ms.keywords: SHCOLSTATE, SHCOLSTATE enumeration [Windows Shell], SHCOLSTATE_BATCHREAD, SHCOLSTATE_DEFAULT, SHCOLSTATE_DISPLAYMASK, SHCOLSTATE_EXTENDED, SHCOLSTATE_FIXED_RATIO, SHCOLSTATE_FIXED_WIDTH, SHCOLSTATE_HIDDEN, SHCOLSTATE_NODPISCALE, SHCOLSTATE_NOSORTBYFOLDERNESS, SHCOLSTATE_NO_GROUPBY, SHCOLSTATE_ONBYDEFAULT, SHCOLSTATE_PREFER_FMTCMP, SHCOLSTATE_PREFER_VARCMP, SHCOLSTATE_SECONDARYUI, SHCOLSTATE_SLOW, SHCOLSTATE_TYPEMASK, SHCOLSTATE_TYPE_DATE, SHCOLSTATE_TYPE_INT, SHCOLSTATE_TYPE_STR, SHCOLSTATE_VIEWONLY, shell.SHCOLSTATE, shell_SHCOLSTATE, shtypes/SHCOLSTATE, shtypes/SHCOLSTATE_BATCHREAD, shtypes/SHCOLSTATE_DEFAULT, shtypes/SHCOLSTATE_DISPLAYMASK, shtypes/SHCOLSTATE_EXTENDED, shtypes/SHCOLSTATE_FIXED_RATIO, shtypes/SHCOLSTATE_FIXED_WIDTH, shtypes/SHCOLSTATE_HIDDEN, shtypes/SHCOLSTATE_NODPISCALE, shtypes/SHCOLSTATE_NOSORTBYFOLDERNESS, shtypes/SHCOLSTATE_NO_GROUPBY, shtypes/SHCOLSTATE_ONBYDEFAULT, shtypes/SHCOLSTATE_PREFER_FMTCMP, shtypes/SHCOLSTATE_PREFER_VARCMP, shtypes/SHCOLSTATE_SECONDARYUI, shtypes/SHCOLSTATE_SLOW, shtypes/SHCOLSTATE_TYPEMASK, shtypes/SHCOLSTATE_TYPE_DATE, shtypes/SHCOLSTATE_TYPE_INT, shtypes/SHCOLSTATE_TYPE_STR, shtypes/SHCOLSTATE_VIEWONLY
req.header: shtypes.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista, Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Shtypes.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: SHCOLSTATE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tagSHCOLSTATE
 - shtypes/tagSHCOLSTATE
 - SHCOLSTATE
 - shtypes/SHCOLSTATE
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Shtypes.h
api_name:
 - SHCOLSTATE
---

# SHCOLSTATE enumeration


## -description

Describes how a property should be treated. These values are defined in Shtypes.h.

## -enum-fields

### -field SHCOLSTATE_DEFAULT:0

The value is displayed according to default settings for the column.

### -field SHCOLSTATE_TYPE_STR:0x1

The value is displayed as a string.

### -field SHCOLSTATE_TYPE_INT:0x2

The value is displayed as an integer.

### -field SHCOLSTATE_TYPE_DATE:0x3

The value is displayed as a date/time.

### -field SHCOLSTATE_TYPEMASK:0xf

A mask for display type values SHCOLSTATE_TYPE_STR, SHCOLSTATE_TYPE_STR, and SHCOLSTATE_TYPE_DATE.

### -field SHCOLSTATE_ONBYDEFAULT:0x10

The column should be on by default in Details view.

### -field SHCOLSTATE_SLOW:0x20

Will be slow to compute. Perform on a background thread.

### -field SHCOLSTATE_EXTENDED:0x40

Provided by a handler, not the folder.

### -field SHCOLSTATE_SECONDARYUI:0x80

Not displayed in the context menu, but is listed in the <b>More...</b> dialog.

### -field SHCOLSTATE_HIDDEN:0x100

Not displayed in the UI.

### -field SHCOLSTATE_PREFER_VARCMP:0x200

<b>VarCmp</b> produces same result as <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-compareids">IShellFolder::CompareIDs</a>.

### -field SHCOLSTATE_PREFER_FMTCMP:0x400

<a href="/windows/desktop/api/propsys/nf-propsys-psformatfordisplay">PSFormatForDisplay</a> produces same result as <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-compareids">IShellFolder::CompareIDs</a>.

### -field SHCOLSTATE_NOSORTBYFOLDERNESS:0x800

Do not sort folders separately.

### -field SHCOLSTATE_VIEWONLY:0x10000

Only displayed in the UI.

### -field SHCOLSTATE_BATCHREAD:0x20000

Marks columns with values that should be read in a batch.

### -field SHCOLSTATE_NO_GROUPBY:0x40000

Grouping is disabled for this column.

### -field SHCOLSTATE_FIXED_WIDTH:0x1000

Can't resize the column.

### -field SHCOLSTATE_NODPISCALE:0x2000

The width is the same in all dpi.

### -field SHCOLSTATE_FIXED_RATIO:0x4000

Fixed width and height ratio.

### -field SHCOLSTATE_DISPLAYMASK:0xf000

Filters out new display flags.
