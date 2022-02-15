---
UID: NF:shobjidl_core.IContextMenu2.HandleMenuMsg
title: IContextMenu2::HandleMenuMsg (shobjidl_core.h)
description: Enables client objects of the IContextMenu interface to handle messages associated with owner-drawn menu items.
helpviewer_keywords: ["HandleMenuMsg","HandleMenuMsg method [Windows Shell]","HandleMenuMsg method [Windows Shell]","IContextMenu2 interface","IContextMenu2 interface [Windows Shell]","HandleMenuMsg method","IContextMenu2.HandleMenuMsg","IContextMenu2::HandleMenuMsg","_win32_IContextMenu2_HandleMenuMsg","shell.IContextMenu2_HandleMenuMsg","shobjidl_core/IContextMenu2::HandleMenuMsg"]
old-location: shell\IContextMenu2_HandleMenuMsg.htm
tech.root: shell
ms.assetid: 06ea4563-a299-4587-906f-4f312c21498a
ms.date: 12/05/2018
ms.keywords: HandleMenuMsg, HandleMenuMsg method [Windows Shell], HandleMenuMsg method [Windows Shell],IContextMenu2 interface, IContextMenu2 interface [Windows Shell],HandleMenuMsg method, IContextMenu2.HandleMenuMsg, IContextMenu2::HandleMenuMsg, _win32_IContextMenu2_HandleMenuMsg, shell.IContextMenu2_HandleMenuMsg, shobjidl_core/IContextMenu2::HandleMenuMsg
req.header: shobjidl_core.h
req.include-header: Shobjidl.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
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
req.dll: Shell32.dll (version 4.0 or later)
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IContextMenu2::HandleMenuMsg
 - shobjidl_core/IContextMenu2::HandleMenuMsg
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
 - IContextMenu2.HandleMenuMsg
---

# IContextMenu2::HandleMenuMsg


## -description

Enables client objects of the <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-icontextmenu">IContextMenu</a> interface to handle messages associated with owner-drawn menu items.

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

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

<b>IContextMenu2::HandleMenuMsg</b> is generally replaced by <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu3-handlemenumsg2">HandleMenuMsg2</a>. <b>HandleMenuMsg2</b> is called when <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-icontextmenu">IContextMenu</a> determines that <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-icontextmenu3">IContextMenu3</a> is supported and receives one of the messages specified in the description of the <i>uMsg</i> parameter. However, in some cases, <b>IContextMenu2::HandleMenuMsg</b> is still called.

If <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-icontextmenu2">IContextMenu2</a> or <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-icontextmenu3">IContextMenu3</a> is needed, the best implementation for new context menus is to implement all their logic in <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu3-handlemenumsg2">HandleMenuMsg2</a> and have their <b>IContextMenu2::HandleMenuMsg</b> implementation simply delegate the call to <b>HandleMenuMsg2</b> and pass <b>NULL</b> as the <i>plResult</i> parameter.


<div class="alert"><b>Note</b>  If <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-icontextmenu3">IContextMenu3</a> is not implemented, there is no guarantee that <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-icontextmenu2">IContextMenu2</a> will be called in its place. In some cases, the absence of <b>IContextMenu3</b> is determined and then the process is halted.
      </div>
<div> </div>

## -see-also

<a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu3-handlemenumsg2">HandleMenuMsg2</a>



<a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-icontextmenu2">IContextMenu2</a>