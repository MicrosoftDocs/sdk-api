---
UID: NE:mmcobj.ListViewMode
title: _ListViewMode (mmcobj.h)
description: The ListViewMode enumeration is used by the View.ListViewMode property to define the list view.
helpviewer_keywords: ["*PLISTVIEWMODE","LISTVIEWMODE","ListMode_Detail","ListMode_Filtered","ListMode_Large_Icons","ListMode_List","ListMode_Small_Icons","ListViewMode","ListViewMode enumeration [MMC]","PLISTVIEWMODE","PLISTVIEWMODE enumeration pointer [MMC]","PPLISTVIEWMODE","PPLISTVIEWMODE enumeration pointer [MMC]","_ListViewMode","_ListViewMode enumeration [MMC]","_slate_listviewmode","mmc.listviewmode","mmcobj/ListMode_Detail","mmcobj/ListMode_Filtered","mmcobj/ListMode_Large_Icons","mmcobj/ListMode_List","mmcobj/ListMode_Small_Icons","mmcobj/ListViewMode","mmcobj/PLISTVIEWMODE","mmcobj/PPLISTVIEWMODE"]
old-location: mmc\listviewmode.htm
tech.root: mmc
ms.assetid: 4f9bcc24-676b-4697-ae11-0d97a6ed4a71
ms.date: 12/05/2018
ms.keywords: '*PLISTVIEWMODE, LISTVIEWMODE, ListMode_Detail, ListMode_Filtered, ListMode_Large_Icons, ListMode_List, ListMode_Small_Icons, ListViewMode, ListViewMode enumeration [MMC], PLISTVIEWMODE, PLISTVIEWMODE enumeration pointer [MMC], PPLISTVIEWMODE, PPLISTVIEWMODE enumeration pointer [MMC], _ListViewMode, _ListViewMode enumeration [MMC], _slate_listviewmode, mmc.listviewmode, mmcobj/ListMode_Detail, mmcobj/ListMode_Filtered, mmcobj/ListMode_Large_Icons, mmcobj/ListMode_List, mmcobj/ListMode_Small_Icons, mmcobj/ListViewMode, mmcobj/PLISTVIEWMODE, mmcobj/PPLISTVIEWMODE'
req.header: mmcobj.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: MmcObj.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: _ListViewMode, LISTVIEWMODE, *PLISTVIEWMODE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ListViewMode
 - mmcobj/ListViewMode
 - PLISTVIEWMODE
 - mmcobj/PLISTVIEWMODE
 - _ListViewMode
 - mmcobj/_ListViewMode
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
 - _ListViewMode
---

# _ListViewMode enumeration


## -description

The 
<b>ListViewMode</b> enumeration is used by the 
<a href="/previous-versions/windows/desktop/mmc/view-listviewmode">View.ListViewMode</a> property to define the list view. The list view can contain small icons, large icons, a simple list, a detailed list, or a filtered list. This enumeration applies to the 
<a href="/previous-versions/windows/desktop/mmc/mmc-2-0-automation-object-model">MMC 2.0 Automation Object Model</a>.

## -enum-fields

### -field ListMode_Small_Icons:0

The list view is displayed with small icons.

### -field ListMode_Large_Icons

The list view is displayed with large icons.

### -field ListMode_List

A simple list view is displayed.

### -field ListMode_Detail

A detailed list view is displayed.

### -field ListMode_Filtered

A filtered list view is displayed.

## -see-also

<a href="/previous-versions/windows/desktop/mmc/view-object">View object</a>



<a href="/previous-versions/windows/desktop/mmc/view-listviewmode">View.ListViewMode</a>
