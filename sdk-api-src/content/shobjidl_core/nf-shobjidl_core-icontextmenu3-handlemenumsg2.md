---
UID: NF:shobjidl_core.IContextMenu3.HandleMenuMsg2
title: IContextMenu3::HandleMenuMsg2 (shobjidl_core.h)
description: Allows client objects of the IContextMenu3 interface to handle messages associated with owner-drawn menu items.
helpviewer_keywords: ["HandleMenuMsg2","HandleMenuMsg2 method [Windows Shell]","HandleMenuMsg2 method [Windows Shell]","IContextMenu3 interface","IContextMenu3 interface [Windows Shell]","HandleMenuMsg2 method","IContextMenu3.HandleMenuMsg2","IContextMenu3::HandleMenuMsg2","_win32_IContextMenu3_HandleMenuMsg2","shell.IContextMenu3_HandleMenuMsg2","shobjidl_core/IContextMenu3::HandleMenuMsg2"]
old-location: shell\IContextMenu3_HandleMenuMsg2.htm
tech.root: shell
ms.assetid: d258edb1-9489-4cdf-b398-16af37a1cb38
ms.date: 12/05/2018
ms.keywords: HandleMenuMsg2, HandleMenuMsg2 method [Windows Shell], HandleMenuMsg2 method [Windows Shell],IContextMenu3 interface, IContextMenu3 interface [Windows Shell],HandleMenuMsg2 method, IContextMenu3.HandleMenuMsg2, IContextMenu3::HandleMenuMsg2, _win32_IContextMenu3_HandleMenuMsg2, shell.IContextMenu3_HandleMenuMsg2, shobjidl_core/IContextMenu3::HandleMenuMsg2
req.header: shobjidl_core.h
req.include-header: Shobjidl.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional, Windows XP [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
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
req.dll: Shell32.dll (version 4.71 or later)
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IContextMenu3::HandleMenuMsg2
 - shobjidl_core/IContextMenu3::HandleMenuMsg2
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
 - IContextMenu3.HandleMenuMsg2
---

# IContextMenu3::HandleMenuMsg2


## -description

Allows client objects of the <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-icontextmenu3">IContextMenu3</a> interface to handle messages associated with owner-drawn menu items.

## -parameters

### -param uMsg

Type: <b>UINT</b>

The message to be processed. In the case of some messages, such as WM_INITMENUPOPUP, WM_DRAWITEM, WM_MENUCHAR, or WM_MEASUREITEM, the client object being called may provide owner-drawn menu items.

### -param wParam

Type: <b>WPARAM</b>

Additional message information. The value of this parameter depends on the value of the <i>uMsg</i> parameter.

### -param lParam

Type: <b>LPARAM</b>

Additional message information. The value of this parameter depends on the value of the <i>uMsg</i> parameter.

### -param plResult

Type: <b>LRESULT*</b>

The address of an <b>LRESULT</b> value that the owner of the menu will return from the message. This parameter can be <b>NULL</b>.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

<b>IContextMenu3::HandleMenuMsg2</b> generally replaces <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu2-handlemenumsg">IContextMenu2::HandleMenuMsg</a>, and is called when <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-icontextmenu">IContextMenu</a> determines that <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-icontextmenu3">IContextMenu3</a> is supported and one of the supported messages (see <i>uMsg</i>) has been received. However, in some cases, <b>IContextMenu2::HandleMenuMsg</b> is still called. Context menu hosts may dispatch menu messages through either or both methods. Consequently, if a Shell extension implements both <b>IContextMenu2::HandleMenuMsg</b> and <b>IContextMenu3::HandleMenuMsg2</b>, it must be prepared for menu messages to arrive through either method.

<div class="alert"><b>Note</b>  If <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-icontextmenu3">IContextMenu3</a> is not implemented, there is no guarantee that <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-icontextmenu2">IContextMenu2</a> will be called in its place. In some cases, the absence of <b>IContextMenu3</b> is determined and then the process is halted.</div>
<div> </div>