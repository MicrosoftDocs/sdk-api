---
UID: NF:shlobj_core.DAD_DragMove
title: DAD_DragMove function (shlobj_core.h)
description: Moves the image that is being dragged during a drag-and-drop operation.
helpviewer_keywords: ["DAD_DragMove","DAD_DragMove function [Windows Shell]","shell.DAD_DragMove","shell_DAD_DragMove","shlobj_core/DAD_DragMove"]
old-location: shell\DAD_DragMove.htm
tech.root: shell
ms.assetid: 7cd9f5ba-e14f-4c0c-8cde-2e7c4926b509
ms.date: 12/05/2018
ms.keywords: DAD_DragMove, DAD_DragMove function [Windows Shell], shell.DAD_DragMove, shell_DAD_DragMove, shlobj_core/DAD_DragMove
f1_keywords:
- shlobj_core/DAD_DragMove
dev_langs:
- c++
req.header: shlobj_core.h
req.include-header: Shlobj.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Shell32.lib
req.dll: Shell32.dll (version 5.00 or later)
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- DllExport
api_location:
- Shell32.dll
- ext-ms-win-shell-shell32-l1-2-1.dll
- Ext-MS-Win-Shell-Shell32-L1-2-2.dll
api_name:
- DAD_DragMove
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# DAD_DragMove function


## -description


<p class="CCE_Message">[<b>DAD_DragMove</b> is available in Windows 2000 and Windows XP. It might be altered or unavailable in subsequent versions. Use <a href="https://docs.microsoft.com/windows/desktop/api/commctrl/nf-commctrl-imagelist_dragmove">ImageList_DragMove</a> instead.
      ]

Moves the image that is being dragged during a drag-and-drop operation.


## -parameters




### -param pt

Type: <b><a href="https://docs.microsoft.com/previous-versions/dd162805(v=vs.85)">POINT</a></b>

The coordinates at which to display the drag image. The coordinates are relative to the upper-left corner of the window, not the client area.  


## -returns



Type: <b>BOOL</b>

Returns nonzero if successful, or zero otherwise.



