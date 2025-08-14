---
UID: NF:shlobj_core.SHDoDragDrop
title: SHDoDragDrop function (shlobj_core.h)
description: Executes a drag-and-drop operation. Supports drag source creation on demand, as well as drag images.
helpviewer_keywords: ["SHDoDragDrop","SHDoDragDrop function [Windows Shell]","_win32_SHDoDragDrop","shell.SHDoDragDrop","shlobj_core/SHDoDragDrop"]
old-location: shell\SHDoDragDrop.htm
tech.root: shell
ms.assetid: 76c98516-ede9-47de-b4ad-257a162775b9
ms.date: 12/05/2018
ms.keywords: SHDoDragDrop, SHDoDragDrop function [Windows Shell], _win32_SHDoDragDrop, shell.SHDoDragDrop, shlobj_core/SHDoDragDrop
req.header: shlobj_core.h
req.include-header: Shlobj.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
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
req.lib: Shell32.lib
req.dll: Shell32.dll (version 6.0 or later)
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - SHDoDragDrop
 - shlobj_core/SHDoDragDrop
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
 - SHDoDragDrop
req.apiset: ext-ms-win-shell-shell32-l1-2-1 (introduced in Windows 10, version 10.0.10240)
---

# SHDoDragDrop function


## -description

Executes a drag-and-drop operation. Supports drag source creation on demand, as well as drag images.

## -parameters

### -param hwnd [in]

Type: <b>HWND</b>

The handle of the window used to obtain the drag image. This value can be <b>NULL</b>. See Remarks for more details.

### -param pdata [in]

Type: <b><a href="/windows/desktop/api/objidl/nn-objidl-idataobject">IDataObject</a>*</b>

A pointer to the <a href="/windows/desktop/api/objidl/nn-objidl-idataobject">IDataObject</a> interface on a data object that contains the data being dragged.

### -param pdsrc [in]

Type: <b><a href="/windows/desktop/api/oleidl/nn-oleidl-idropsource">IDropSource</a>*</b>

A pointer to an implementation of the <a href="/windows/desktop/api/oleidl/nn-oleidl-idropsource">IDropSource</a> interface, which is used to communicate with the source during the drag operation.
        
                        

As of Windows Vista, if this value is <b>NULL</b>, the Shell creates a drop source object for you.

### -param dwEffect [in]

Type: <b>DWORD</b>

The effects that the source allows in the drag-and-drop operation. The most significant effect is whether the drag-and-drop operation permits a move. For a list of possible values, see <a href="/windows/desktop/com/dropeffect-constants">DROPEFFECT</a>.

### -param pdwEffect [out]

Type: <b>DWORD*</b>

A pointer to a value that indicates how the drag-and-drop operation affected the source data. The <i>pdwEffect</i> parameter is set only if the operation is not canceled. For a list of possible values, see <a href="/windows/desktop/com/dropeffect-constants">DROPEFFECT</a>.

## -returns

Type: <b>HRESULT</b>

This function supports the standard return value E_OUTOFMEMORY, as well as the following values:

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>DRAGDROP_S_DROP</b></dt>
</dl>
</td>
<td width="60%">
The drag-and-drop operation was successful.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>DRAGDROP_S_CANCEL</b></dt>
</dl>
</td>
<td width="60%">
The drag-and-drop operation was canceled.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_UNSPEC</b></dt>
</dl>
</td>
<td width="60%">
Unexpected error occurred.

</td>
</tr>
</table>

## -remarks

As of Windows Vista, if a drag image is not already stored in the data object <i>pdtobj</i> and a drag image cannot be obtained from the window specified by <i>hwnd</i>, the Shell provides a generic drag image. A drag image can fail to be obtained from the specified window either because <i>hwnd</i> is <b>NULL</b> or the specified window does not support the DI_GETDRAGIMAGE message.
