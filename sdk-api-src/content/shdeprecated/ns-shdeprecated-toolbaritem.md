---
UID: NS:shdeprecated.SToolbarItem
title: TOOLBARITEM (shdeprecated.h)
description: Deprecated. Data used in IBrowserService2::_GetToolbarItem, IBrowserService2::v_MayGetNextToolbarFocus, and IBrowserService2::_SetFocus to define a toolbar item.
helpviewer_keywords: ["*LPTOOLBARITEM","LPTOOLBARITEM","LPTOOLBARITEM structure pointer [Windows Shell]","TOOLBARITEM","TOOLBARITEM structure [Windows Shell]","_shell_TOOLBARITEM","shdeprecated/LPTOOLBARITEM","shdeprecated/TOOLBARITEM","shell.TOOLBARITEM"]
old-location: shell\TOOLBARITEM.htm
tech.root: shell
ms.assetid: 7378f2f3-c164-46fe-9989-a7a57fceb48a
ms.date: 12/05/2018
ms.keywords: '*LPTOOLBARITEM, LPTOOLBARITEM, LPTOOLBARITEM structure pointer [Windows Shell], TOOLBARITEM, TOOLBARITEM structure [Windows Shell], _shell_TOOLBARITEM, shdeprecated/LPTOOLBARITEM, shdeprecated/TOOLBARITEM, shell.TOOLBARITEM'
req.header: shdeprecated.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Shdeprecated.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: TOOLBARITEM, *LPTOOLBARITEM
req.redist: 
req.product: Internet Explorer 5.0
ms.custom: 19H1
f1_keywords:
 - SToolbarItem
 - shdeprecated/SToolbarItem
 - LPTOOLBARITEM
 - shdeprecated/LPTOOLBARITEM
 - TOOLBARITEM
 - shdeprecated/TOOLBARITEM
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Shdeprecated.h
api_name:
 - TOOLBARITEM
---

# TOOLBARITEM structure


## -description

Deprecated. Data used in <a href="/windows/win32/api/shdeprecated/nf-shdeprecated-ibrowserservice2-_gettoolbaritem">IBrowserService2::_GetToolbarItem</a>, <a href="/windows/desktop/api/shdeprecated/nf-shdeprecated-ibrowserservice2-v_maygetnexttoolbarfocus">IBrowserService2::v_MayGetNextToolbarFocus</a>, and <a href="/windows/win32/api/shdeprecated/nf-shdeprecated-ibrowserservice2-_setfocus">IBrowserService2::_SetFocus</a> to define a toolbar item.

## -struct-fields

### -field ptbar

Type: <b><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-idockingwindow">IDockingWindow</a>*</b>

The <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-idockingwindow">IDockingWindow</a> of the item's particular toolbar.

### -field rcBorderTool

Type: <b><a href="/previous-versions/windows/desktop/legacy/cc136564(v=vs.85)">BORDERWIDTHS</a></b>

A <a href="/previous-versions/windows/desktop/legacy/cc136564(v=vs.85)">BORDERWIDTHS</a> structure that contains the dimensions of the item, including its borders.

### -field pwszItem

Type: <b>LPWSTR</b>

A pointer to a buffer that contains the name of the toolbar item as a Unicode string.

### -field fShow

Type: <b>BOOL</b>

<b>TRUE</b> if the toolbar item is currently visible; otherwise, <b>FALSE</b>.

### -field hMon

Type: <b>HMONITOR</b>

The handle of the monitor on which the toolbar item appears.