---
UID: NF:shobjidl_core.IDragSourceHelper.InitializeFromWindow
title: IDragSourceHelper::InitializeFromWindow (shobjidl_core.h)
description: Initializes the drag-image manager for a control with a window.
helpviewer_keywords: ["IDragSourceHelper interface [Windows Shell]","InitializeFromWindow method","IDragSourceHelper.InitializeFromWindow","IDragSourceHelper::InitializeFromWindow","InitializeFromWindow","InitializeFromWindow method [Windows Shell]","InitializeFromWindow method [Windows Shell]","IDragSourceHelper interface","_win32_IDragSourceHelper_InitializeFromWindow","shell.IDragSourceHelper_InitializeFromWindow","shobjidl_core/IDragSourceHelper::InitializeFromWindow"]
old-location: shell\IDragSourceHelper_InitializeFromWindow.htm
tech.root: shell
ms.assetid: 0bcdfe92-cec0-44f3-a345-5b560d52fae9
ms.date: 12/05/2018
ms.keywords: IDragSourceHelper interface [Windows Shell],InitializeFromWindow method, IDragSourceHelper.InitializeFromWindow, IDragSourceHelper::InitializeFromWindow, InitializeFromWindow, InitializeFromWindow method [Windows Shell], InitializeFromWindow method [Windows Shell],IDragSourceHelper interface, _win32_IDragSourceHelper_InitializeFromWindow, shell.IDragSourceHelper_InitializeFromWindow, shobjidl_core/IDragSourceHelper::InitializeFromWindow
req.header: shobjidl_core.h
req.include-header: Shobjidl.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional, Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Shobjidl.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: Shell32.dll (version 5.0 or later)
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IDragSourceHelper::InitializeFromWindow
 - shobjidl_core/IDragSourceHelper::InitializeFromWindow
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Shell32.dll
api_name:
 - IDragSourceHelper.InitializeFromWindow
---

# IDragSourceHelper::InitializeFromWindow


## -description

Initializes the drag-image manager for a control with a window.

## -parameters

### -param hwnd [in]

Type: <b>HWND</b>

A handle to the window that receives the <b>DI_GETDRAGIMAGE</b> message. This value can be <b>NULL</b>.

### -param ppt [in]

Type: <b><a href="/windows/win32/api/windef/ns-windef-point">POINT</a>*</b>

A pointer to a <a href="/windows/win32/api/windef/ns-windef-point">POINT</a> structure that specifies the location of the cursor within the drag image. The structure should contain the offset from the upper-left corner of the drag image to the location of the cursor. This value can be <b>NULL</b>.

### -param pDataObject [in]

Type: <b><a href="/windows/desktop/api/objidl/nn-objidl-idataobject">IDataObject</a>*</b>

A pointer to the data object's <a href="/windows/desktop/api/objidl/nn-objidl-idataobject">IDataObject</a> interface.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

The <b>DI_GETDRAGIMAGE</b> message allows you to source a drag image from a custom control. It is defined in Shlobj.h and must be registered with <a href="/windows/desktop/api/winuser/nf-winuser-registerwindowmessagea">RegisterWindowMessage</a>. When the window specified by <i>hwnd</i> receives the <b>DI_GETDRAGIMAGE</b> message, the <i>lParam</i> value holds a pointer to an <a href="/windows/desktop/api/shobjidl_core/ns-shobjidl_core-shdragimage">SHDRAGIMAGE</a> structure. The handler should fill the structure with the drag image bitmap information.

## -see-also

<a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-idragsourcehelper">IDragSourceHelper</a>