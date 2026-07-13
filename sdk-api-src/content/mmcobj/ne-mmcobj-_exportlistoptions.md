---
UID: NE:mmcobj.ExportListOptions
title: _ExportListOptions (mmcobj.h)
description: The ExportListOptions enumeration is used by the View.ExportList method and specifies options when writing list view contents to a file.
helpviewer_keywords: ["EXPORTLISTOPTIONS","ExportListOptions","ExportListOptions enumeration [MMC]","ExportListOptions_Default","ExportListOptions_SelectedItemsOnly","ExportListOptions_TabDelimited","ExportListOptions_Unicode","_ExportListOptions","_ExportListOptions enumeration [MMC]","_slate_exportlistoptions","mmc.exportlistoptions","mmcobj/ExportListOptions","mmcobj/ExportListOptions_Default","mmcobj/ExportListOptions_SelectedItemsOnly","mmcobj/ExportListOptions_TabDelimited","mmcobj/ExportListOptions_Unicode"]
old-location: mmc\exportlistoptions.htm
tech.root: mmc
ms.assetid: cfdb5648-8573-4c5a-85c2-7a5d3d63a5f3
ms.date: 12/05/2018
ms.keywords: EXPORTLISTOPTIONS, ExportListOptions, ExportListOptions enumeration [MMC], ExportListOptions_Default, ExportListOptions_SelectedItemsOnly, ExportListOptions_TabDelimited, ExportListOptions_Unicode, _ExportListOptions, _ExportListOptions enumeration [MMC], _slate_exportlistoptions, mmc.exportlistoptions, mmcobj/ExportListOptions, mmcobj/ExportListOptions_Default, mmcobj/ExportListOptions_SelectedItemsOnly, mmcobj/ExportListOptions_TabDelimited, mmcobj/ExportListOptions_Unicode
req.header: mmcobj.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
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
req.typenames: _ExportListOptions, EXPORTLISTOPTIONS
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ExportListOptions
 - mmcobj/ExportListOptions
 - _ExportListOptions
 - mmcobj/_ExportListOptions
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - MmcObj.h
api_name:
 - _ExportListOptions
---

# _ExportListOptions enumeration


## -description

The 
<b>ExportListOptions</b> enumeration is used by the 
<a href="/previous-versions/windows/desktop/mmc/view-exportlist">View.ExportList</a> method and specifies options when writing list view contents to a file. These values can be combined using a bitwise OR operation. This enumeration applies to the 
<a href="/previous-versions/windows/desktop/mmc/mmc-2-0-automation-object-model">MMC 2.0 Automation Object Model</a>.

## -enum-fields

### -field ExportListOptions_Default:0

Default list export option. If this is the only flag specified in the call to <a href="/previous-versions/windows/desktop/mmc/view-exportlist">View.ExportList</a>, then the list view contents are exported as comma-delimited ANSI text.

### -field ExportListOptions_Unicode:0x1

The list is exported as Unicode text.

### -field ExportListOptions_TabDelimited:0x2

The list is exported as tab-delimited text.

### -field ExportListOptions_SelectedItemsOnly:0x4

The exported list contains only currently selected items.

## -see-also

<a href="/previous-versions/windows/desktop/mmc/view-object">View object</a>



<a href="/previous-versions/windows/desktop/mmc/view-exportlist">View.ExportList</a>
