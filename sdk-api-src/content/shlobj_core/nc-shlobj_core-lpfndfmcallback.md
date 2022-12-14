---
UID: NC:shlobj_core.LPFNDFMCALLBACK
title: LPFNDFMCALLBACK (shlobj_core.h)
description: LPFNDFMCALLBACK may be altered or unavailable.
helpviewer_keywords: ["LPFNDFMCALLBACK","LPFNDFMCALLBACK callback","LPFNDFMCALLBACK callback function [Windows Shell]","_win32_LPFNDFMCALLBACK","shell.LPFNDFMCALLBACK","shlobj_core/LPFNDFMCALLBACK"]
old-location: shell\LPFNDFMCALLBACK.htm
tech.root: shell
ms.assetid: a5635196-80de-4db9-9c3a-65f2b241b4a0
ms.date: 12/05/2018
ms.keywords: LPFNDFMCALLBACK, LPFNDFMCALLBACK callback, LPFNDFMCALLBACK callback function [Windows Shell], _win32_LPFNDFMCALLBACK, shell.LPFNDFMCALLBACK, shlobj_core/LPFNDFMCALLBACK
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - LPFNDFMCALLBACK
 - shlobj_core/LPFNDFMCALLBACK
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - shlobj_core.h
api_name:
 - LPFNDFMCALLBACK
---

# LPFNDFMCALLBACK callback function


## -description

<p class="CCE_Message">[<b>LPFNDFMCALLBACK</b> is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions.]

Defines the prototype for the callback function that receives messages from the Shell's default context menu implementation.

## -parameters

### -param psf [in, optional]

Type: <b><a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellfolder">IShellFolder</a>*</b>

A pointer to the <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellfolder">IShellFolder</a> object the message applies to. This value can be <b>NULL</b>.

### -param hwnd [in, optional]

Type: <b>HWND</b>

The handle of the window that contains the view. This value can be <b>NULL</b>.

### -param pdtobj [in, optional]

Type: <b><a href="/windows/desktop/api/objidl/nn-objidl-idataobject">IDataObject</a>*</b>


<a href="/windows/desktop/api/objidl/nn-objidl-idataobject">IDataObject</a> that represents the selection the context menu is based on. This value can be <b>NULL</b>.

### -param uMsg

Type: <b>UINT</b>

One of the following notifications.
    					
                        

<table class="clsStd">
<tr>
<th>Notification</th>
<th>Usage</th>
</tr>
<tr>
<td>
<a href="/windows/desktop/shell/registering-control-panel-items">DFM_MERGECONTEXTMENU</a>
</td>
<td>Sent by the default context menu implementation to allow <b>LPFNDFMCALLBACK</b> to add items to the menu.</td>
</tr>
<tr>
<td>
<a href="/windows/desktop/shell/preview-handler-guidelines">DFM_INVOKECOMMAND</a>
</td>
<td>Sent by the default context menu implementation to request <b>LPFNDFMCALLBACK</b> to invoke a menu command.</td>
</tr>
<tr>
<td>
<a href="/windows/desktop/shell/library-ovw">DFM_GETDEFSTATICID</a>
</td>
<td>Sent by the default context menu implementation when the default menu command is being created, allowing an alternate choice to be made.</td>
</tr>
</table>

### -param wParam

Type: <b>WPARAM</b>

Additional information. See the individual notification pages for specific requirements.

### -param lParam

Type: <b>LPARAM</b>

Additional information. See the individual notification pages for specific requirements.

## -returns

Type: <b>HRESULT</b>

Returns S_OK if the message was handled, or an error value otherwise, including the following:

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_NOTIMPL</b></dt>
</dl>
</td>
<td width="60%">
The message was not handled.

</td>
</tr>
</table>
