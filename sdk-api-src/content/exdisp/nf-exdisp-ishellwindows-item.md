---
UID: NF:exdisp.IShellWindows.Item
title: IShellWindows::Item (exdisp.h)
description: Returns the registered Shell window for a specified index.
helpviewer_keywords: ["IShellWindows interface [Windows Shell]","Item method","IShellWindows.Item","IShellWindows::Item","Item","Item method [Windows Shell]","Item method [Windows Shell]","IShellWindows interface","_win32_IShellWindows_Item","exdisp/IShellWindows::Item","shell.IShellWindows_Item"]
old-location: shell\IShellWindows_Item.htm
tech.root: shell
ms.assetid: 04157d1a-8a4d-4ffd-882d-41748408ba2b
ms.date: 12/05/2018
ms.keywords: IShellWindows interface [Windows Shell],Item method, IShellWindows.Item, IShellWindows::Item, Item, Item method [Windows Shell], Item method [Windows Shell],IShellWindows interface, _win32_IShellWindows_Item, exdisp/IShellWindows::Item, shell.IShellWindows_Item
req.header: exdisp.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Exdisp.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: Shdocvw.dll (version 5.00.2014.0216 or later)
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
req.product: Internet Explorer 5
ms.custom: 19H1
f1_keywords:
 - IShellWindows::Item
 - exdisp/IShellWindows::Item
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Shdocvw.dll
api_name:
 - IShellWindows.Item
---

# IShellWindows::Item


## -description

Returns the registered Shell window for a specified index.

## -parameters

### -param index [in, optional]

Type: <b>VARIANT</b>

A <a href="/windows/desktop/api/oaidl/ns-oaidl-variant">VARIANT</a> of type VT_UI4, VT_I2, or VT_I4. If the type is VT_UI4, the value of <i>index</i> is interpreted as a member of <a href="/windows/desktop/api/exdisp/ne-exdisp-shellwindowtypeconstants">ShellWindowTypeConstants</a>; in this case, <b>Item</b> returns the window that is closest to the foreground window and has a matching type. If the type is VT_I, or VT_I4, <i>index</i> is treated as an index into the Shell windows collection.

### -param Folder [out, retval]

Type: <b><a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a>**</b>

A reference to the window's <a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface, or <b>NULL</b> if the specified window was not found.

## -returns

Type: <b>HRESULT</b>

One of the following values, or a standard result code.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The specified window was found.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_FALSE</b></dt>
</dl>
</td>
<td width="60%">
The specified window was not found.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/exdisp/nn-exdisp-ishellwindows">IShellWindows</a>



<a href="/windows/win32/api/exdisp/nf-exdisp-ishellwindows-_newenum">IShellWindows::_NewEnum</a>



<a href="/windows/desktop/api/exdisp/nf-exdisp-ishellwindows-get_count">IShellWindows::get_Count</a>