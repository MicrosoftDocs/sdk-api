---
UID: NF:shobjidl_core.IContextMenuCB.CallBack
title: IContextMenuCB::CallBack (shobjidl_core.h)
description: Enables the callback function for a context menu.
helpviewer_keywords: ["CallBack","CallBack method [Windows Shell]","CallBack method [Windows Shell]","IContextMenuCB interface","IContextMenuCB interface [Windows Shell]","CallBack method","IContextMenuCB.CallBack","IContextMenuCB::CallBack","_shell_IContextMenuCB_CallBack","shell.IContextMenuCB_CallBack","shobjidl_core/IContextMenuCB::CallBack"]
old-location: shell\IContextMenuCB_CallBack.htm
tech.root: shell
ms.assetid: 9d091b1a-26b5-4cab-a3ec-6d59dc7d103e
ms.date: 12/05/2018
ms.keywords: CallBack, CallBack method [Windows Shell], CallBack method [Windows Shell],IContextMenuCB interface, IContextMenuCB interface [Windows Shell],CallBack method, IContextMenuCB.CallBack, IContextMenuCB::CallBack, _shell_IContextMenuCB_CallBack, shell.IContextMenuCB_CallBack, shobjidl_core/IContextMenuCB::CallBack
req.header: shobjidl_core.h
req.include-header: Shobjidl.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IContextMenuCB::CallBack
 - shobjidl_core/IContextMenuCB::CallBack
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - shobjidl_core.h
api_name:
 - IContextMenuCB.CallBack
---

# IContextMenuCB::CallBack


## -description

Enables the callback function for a context menu.

## -parameters

### -param psf [in]

Type: <b><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellfolder">IShellFolder</a>*</b>

A pointer to the <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellfolder">IShellFolder</a> interface of the object that supports the <b>IContextMenuCB::CallBack</b> interface. The context menu interface is returned on a call to <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-getuiobjectof">GetUIObjectOf</a>.

### -param hwndOwner [in, optional]

Type: <b>HWND</b>

A handle to the owner of the context menu. This value can be <b>NULL</b>.

### -param pdtobj [in]

Type: <b><a href="/windows/desktop/api/objidl/nn-objidl-idataobject">IDataObject</a>*</b>

A pointer to an <a href="/windows/desktop/api/objidl/nn-objidl-idataobject">IDataObject</a> that contains information about a menu selection. Implement interface <b>IDataObject</b>, or call <a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shcreatedataobject">SHCreateDataObject</a> for the default implementation.

### -param uMsg [in]

Type: <b>UINT</b>

A notification from the Shell's default menu implementation. For example, the default menu implementation calls <a href="/windows/desktop/shell/registering-control-panel-items">DFM_MERGECONTEXTMENU</a> to allow the implementer of <b>IContextMenuCB::CallBack</b> to remove, add, or disable context menu items in this callback. Use one of the following notifications.

                    


<table class="clsStd">
<tr>
<td>
<a href="/windows/win32/shell/dfm-mergecontextmenu">DFM_MERGECONTEXTMENU</a>
</td>
</tr>
<tr>
<td>
<a href="/windows/win32/shell/dfm-invokecommand">DFM_INVOKECOMMAND</a>
</td>
</tr>
<tr>
<td>
<a href="/windows/win32/shell/dfm-gethelptext">DFM_GETHELPTEXT</a>
</td>
</tr>
<tr>
<td>
<a href="/windows/win32/shell/dfm-gethelptextw">DFM_GETHELPTEXTW</a>
</td>
</tr>
<tr>
<td>
<a href="/windows/win32/shell/dfm-wm-measureitem">DFM_WM_MEASUREITEM</a>
</td>
</tr>
<tr>
<td>
<a href="/windows/win32/shell/dfm-wm-drawitem">DFM_WM_DRAWITEM</a>
</td>
</tr>
<tr>
<td>
<a href="/windows/win32/shell/dfm-wm-initmenupopup">DFM_WM_INITMENUPOPUP</a>
</td>
</tr>
<tr>
<td>
<a href="/windows/win32/shell/dfm-validatecmd">DFM_VALIDATECMD</a>
</td>
</tr>
<tr>
<td>
<a href="/windows/win32/shell/dfm-invokecommandex">DFM_INVOKECOMMANDEX</a>
</td>
</tr>
<tr>
<td>
<a href="/windows/win32/shell/dfm-mapcommandname">DFM_MAPCOMMANDNAME</a>
</td>
</tr>
<tr>
<td>
<a href="/windows/win32/shell/dfm-getdefstaticid">DFM_GETDEFSTATICID</a>
</td>
</tr>
<tr>
<td>
<a href="/windows/win32/shell/dfm-getverb">DFM_GETVERB</a>
</td>
</tr>
<tr>
<td>
<a href="/windows/win32/shell/dfm-mergecontextmenu-bottom">DFM_MERGECONTEXTMENU_BOTTOM</a>
</td>
</tr>
</table>

### -param wParam [in]

Type: <b>WPARAM</b>

Data specific to the notification specified in <i>uMsg</i>. See the individual notification page for specific requirements.

### -param lParam [in]

Type: <b>LPARAM</b>

Data specific to the notification specified in <i>uMsg</i>. See the individual notification page for specific requirements.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/shell/context-menu-handlers">Creating Context Menu Handlers</a>



<a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-icontextmenucb">IContextMenuCB</a>
