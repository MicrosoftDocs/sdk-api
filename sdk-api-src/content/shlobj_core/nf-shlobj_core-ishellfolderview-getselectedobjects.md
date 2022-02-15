---
UID: NF:shlobj_core.IShellFolderView.GetSelectedObjects
title: IShellFolderView::GetSelectedObjects (shlobj_core.h)
description: Gets an array of the objects in the view that are selected and the number of those objects.
helpviewer_keywords: ["GetSelectedObjects","GetSelectedObjects method [Windows Shell]","GetSelectedObjects method [Windows Shell]","IShellFolderView interface","IShellFolderView interface [Windows Shell]","GetSelectedObjects method","IShellFolderView.GetSelectedObjects","IShellFolderView::GetSelectedObjects","_shell_IShellFolderView_GetSelectedObjects","shell.IShellFolderView_GetSelectedObjects","shlobj_core/IShellFolderView::GetSelectedObjects"]
old-location: shell\IShellFolderView_GetSelectedObjects.htm
tech.root: shell
ms.assetid: 9cb41312-a401-4d24-a7a7-7b03478cf684
ms.date: 12/05/2018
ms.keywords: GetSelectedObjects, GetSelectedObjects method [Windows Shell], GetSelectedObjects method [Windows Shell],IShellFolderView interface, IShellFolderView interface [Windows Shell],GetSelectedObjects method, IShellFolderView.GetSelectedObjects, IShellFolderView::GetSelectedObjects, _shell_IShellFolderView_GetSelectedObjects, shell.IShellFolderView_GetSelectedObjects, shlobj_core/IShellFolderView::GetSelectedObjects
req.header: shlobj_core.h
req.include-header: 
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IShellFolderView::GetSelectedObjects
 - shlobj_core/IShellFolderView::GetSelectedObjects
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - shlobj_core.h
api_name:
 - IShellFolderView.GetSelectedObjects
---

# IShellFolderView::GetSelectedObjects


## -description

<p class="CCE_Message">[This method has been deprecated. Use <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ifolderview2-getselection">IFolderView2::GetSelection</a> instead.]

Gets an array of the objects in the view that are selected and the number of those objects.

## -parameters

### -param pppidl [out]

Type: <b>PCUITEMID_CHILD**</b>

The address of a pointer that, when this method returns successfully, points to an array of the currently selected items in the view. The calling application is expected to free the array at <i>pppidl</i> using <a href="/windows/desktop/api/winbase/nf-winbase-localfree">LocalFree</a>. The calling application must not free the individual items contained in the array.

### -param puItems [out]

Type: <b>UINT*</b>

A pointer to a value that, when this method returns successfully, receives the number of items in the <i>pppidl</i> array.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

This method provides constant pointers to internal data structures. The calling application is expected to act on them immediately and not cache them.