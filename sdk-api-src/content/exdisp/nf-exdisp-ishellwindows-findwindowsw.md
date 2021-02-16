---
UID: NF:exdisp.IShellWindows.FindWindowSW
title: IShellWindows::FindWindowSW (exdisp.h)
description: Finds a window in the Shell windows collection and returns the window's handle and IDispatch interface.
helpviewer_keywords: ["FindWindowSW","FindWindowSW method [Windows Shell]","FindWindowSW method [Windows Shell]","IShellWindows interface","IShellWindows interface [Windows Shell]","FindWindowSW method","IShellWindows.FindWindowSW","IShellWindows::FindWindowSW","_win32_IShellWindows_FindWindowSW","exdisp/IShellWindows::FindWindowSW","shell.IShellWindows_FindWindowSW"]
old-location: shell\IShellWindows_FindWindowSW.htm
tech.root: shell
ms.assetid: 10eed153-cb0b-4ce0-8cc5-2e7ebf683fda
ms.date: 12/05/2018
ms.keywords: FindWindowSW, FindWindowSW method [Windows Shell], FindWindowSW method [Windows Shell],IShellWindows interface, IShellWindows interface [Windows Shell],FindWindowSW method, IShellWindows.FindWindowSW, IShellWindows::FindWindowSW, _win32_IShellWindows_FindWindowSW, exdisp/IShellWindows::FindWindowSW, shell.IShellWindows_FindWindowSW
req.header: exdisp.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: ExDisp.idl
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
 - IShellWindows::FindWindowSW
 - exdisp/IShellWindows::FindWindowSW
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
 - IShellWindows.FindWindowSW
---

# IShellWindows::FindWindowSW


## -description

Finds a window in the Shell windows collection and returns the window's handle and <a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface.

## -parameters

### -param pvarLoc [in]

Type: <b>VARIANT*</b>

A <a href="/windows/desktop/api/oaidl/ns-oaidl-variant">VARIANT</a> of type VT_VARIANT | VT_BYREF. Set the value of <i>pvarLoc</i> to an absolute <a href="/windows/desktop/api/shtypes/ns-shtypes-itemidlist">PIDL</a> (PIDLIST_ABSOLUTE) that specifies the window to find. (See remarks.)

### -param pvarLocRoot [in]

Type: <b>VARIANT*</b>

Must be <b>NULL</b> or of type VT_EMPTY.

### -param swClass [in]

Type: <b>int</b>

One or more <a href="/windows/desktop/api/exdisp/ne-exdisp-shellwindowtypeconstants">ShellWindowTypeConstants</a> flags that specify window types to include in the search.

### -param phwnd [out]

Type: <b>long*</b>

A handle for the window matching the specified search criteria, or <b>NULL</b> if no such window was found.

### -param swfwOptions

Type: <b>int</b>

One or more <a href="/windows/desktop/api/exdisp/ne-exdisp-shellwindowfindwindowoptions">ShellWindowFindWindowOptions</a> flags that specify search options.

### -param ppdispOut [out, retval]

Type: <b><a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a>**</b>

A reference to the window's <a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface, or <b>NULL</b> if no such window was found.

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
A window matching the specified search criteria was found.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_FALSE</b></dt>
</dl>
</td>
<td width="60%">
A window matching the specified search criteria was not found.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_NOINTERFACE</b></dt>
</dl>
</td>
<td width="60%">
A window was found, but a reference to the window's <a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface could not be obtained. Only occurs if the <a href="/windows/desktop/api/exdisp/ne-exdisp-shellwindowfindwindowoptions">SWFO_NEEDDISPATCH</a> flag is set.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_PENDING</b></dt>
</dl>
</td>
<td width="60%">
A window was found, but the window is pending open. Only occurs if the <a href="/windows/desktop/api/exdisp/ne-exdisp-shellwindowfindwindowoptions">SWFO_INCLUDEPENDING</a> flag is set.

</td>
</tr>
</table>

## -remarks

If the <a href="/windows/desktop/api/exdisp/ne-exdisp-shellwindowfindwindowoptions">SWFO_COOKIEPASSED</a> flag is set, <i>pvarLoc</i> is interpreted as a cookie instead of a PIDL.