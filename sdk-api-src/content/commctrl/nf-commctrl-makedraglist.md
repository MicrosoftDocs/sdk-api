---
UID: NF:commctrl.MakeDragList
title: MakeDragList function (commctrl.h)
description: Changes the specified single-selection list box to a drag list box.
helpviewer_keywords: ["MakeDragList","MakeDragList function [Windows Controls]","_win32_MakeDragList","_win32_MakeDragList_cpp","commctrl/MakeDragList","controls.MakeDragList","controls._win32_MakeDragList"]
old-location: controls\MakeDragList.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\draglb\functions\makedraglist.htm
ms.date: 12/05/2018
ms.keywords: MakeDragList, MakeDragList function [Windows Controls], _win32_MakeDragList, _win32_MakeDragList_cpp, commctrl/MakeDragList, controls.MakeDragList, controls._win32_MakeDragList
req.header: commctrl.h
req.include-header: 
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
req.lib: Comctl32.lib
req.dll: Comctl32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - MakeDragList
 - commctrl/MakeDragList
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Comctl32.dll
api_name:
 - MakeDragList
---

# MakeDragList function


## -description

Changes the specified single-selection list box to a drag list box.

## -parameters

### -param hLB

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HWND</a></b>

A handle to the single-selection list box.

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">BOOL</a></b>

Returns nonzero if successful, or zero otherwise.