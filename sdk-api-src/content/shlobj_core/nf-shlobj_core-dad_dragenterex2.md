---
UID: NF:shlobj_core.DAD_DragEnterEx2
title: DAD_DragEnterEx2 function (shlobj_core.h)
description: Locks updates to the specified window during a drag-and-drop operation and displays the drag image at the specified position within the window.
helpviewer_keywords: ["DAD_DragEnterEx2","DAD_DragEnterEx2 function [Windows Shell]","_shell_DAD_DragEnterEx2","shell.DAD_DragEnterEx2","shlobj_core/DAD_DragEnterEx2"]
old-location: shell\DAD_DragEnterEx2.htm
tech.root: shell
ms.assetid: d9d902c5-c488-4e23-a749-bae42c6cb719
ms.date: 12/05/2018
ms.keywords: DAD_DragEnterEx2, DAD_DragEnterEx2 function [Windows Shell], _shell_DAD_DragEnterEx2, shell.DAD_DragEnterEx2, shlobj_core/DAD_DragEnterEx2
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
req.dll: Shell32.dll (version 5.0 or later)
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - DAD_DragEnterEx2
 - shlobj_core/DAD_DragEnterEx2
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - ext-ms-win-shell-shell32-l1-5-0.dll
 - ext-ms-win-shell-shell32-l1-4-0.dll
 - ext-ms-win-shell-shell32-l1-3-0.dll
 - ext-ms-win-shell-shell32-l1-2-3.dll
 - Shell32.dll
 - ext-ms-win-shell-shell32-l1-2-1.dll
 - Ext-MS-Win-Shell-Shell32-L1-2-2.dll
api_name:
 - DAD_DragEnterEx2
req.apiset: ext-ms-win-shell-shell32-l1-2-1 (introduced in Windows 10, version 10.0.10240)
---

# DAD_DragEnterEx2 function


## -description

<p class="CCE_Message">[<b>DAD_DragEnterEx2</b> is available in Windows 2000 and Windows XP. It might be altered or unavailable in subsequent versions. Use <a href="/windows/desktop/api/commctrl/nf-commctrl-imagelist_dragenter">ImageList_DragEnter</a> instead.]

Locks updates to the specified window during a drag-and-drop operation and displays the drag image at the specified position within the window.

## -parameters

### -param hwndTarget [in]

Type: <b>HWND</b>

A handle to the window that owns the drag image.

### -param ptStart

Type: <b>const <a href="/windows/win32/api/windef/ns-windef-point">POINT</a></b>

Specifies the coordinates at which to begin displaying the drag image. The coordinates are relative to the upper-left corner of the window, not the client area.

### -param pdtObject [in, optional]

Type: <b><a href="/windows/desktop/api/objidl/nn-objidl-idataobject">IDataObject</a>*</b>

A pointer to the <a href="/windows/desktop/api/objidl/nn-objidl-idataobject">IDataObject</a> interface on the data object. This data object contains the data being transferred in the drag-and-drop operation. If the drop occurs, this data object will be incorporated into the target. This parameter may be <b>NULL</b>.

## -returns

Type: <b>BOOL</b>

Returns <b>TRUE</b> if successful, <b>FALSE</b> otherwise.

## -see-also

<a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-dad_dragenterex">DAD_DragEnterEx</a>



<a href="/windows/desktop/api/commctrl/nf-commctrl-imagelist_dragenter">ImageList_DragEnter</a>
