---
UID: NF:winuser.GetListBoxInfo
title: GetListBoxInfo function (winuser.h)
description: Retrieves the number of items per column in a specified list box.
helpviewer_keywords: ["GetListBoxInfo","GetListBoxInfo function [Windows Controls]","_win32_GetListBoxInfo","_win32_GetListBoxInfo_cpp","controls.GetListBoxInfo","controls._win32_GetListBoxInfo","winuser/GetListBoxInfo"]
old-location: controls\GetListBoxInfo.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\listboxes\listboxreference\listboxfunctions\getlistboxinfo.htm
ms.date: 12/05/2018
ms.keywords: GetListBoxInfo, GetListBoxInfo function [Windows Controls], _win32_GetListBoxInfo, _win32_GetListBoxInfo_cpp, controls.GetListBoxInfo, controls._win32_GetListBoxInfo, winuser/GetListBoxInfo
req.header: winuser.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: User32.lib
req.dll: User32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: Service Pack 6
ms.custom: 19H1
f1_keywords:
 - GetListBoxInfo
 - winuser/GetListBoxInfo
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - User32.dll
api_name:
 - GetListBoxInfo
---

# GetListBoxInfo function


## -description

Retrieves the number of items per column in a specified list box.

## -parameters

### -param hwnd [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HWND</a></b>

A handle to the list box whose number of items per column is to be retrieved.

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">DWORD</a></b>

The return value is the number of items per column.

## -see-also

<a href="/windows/desktop/api/winuser/nf-winuser-getcomboboxinfo">GetComboBoxInfo</a>