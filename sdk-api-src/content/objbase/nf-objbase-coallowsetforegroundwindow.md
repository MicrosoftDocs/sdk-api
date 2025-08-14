---
UID: NF:objbase.CoAllowSetForegroundWindow
title: CoAllowSetForegroundWindow function (objbase.h)
description: This function passes the foreground privilege (the privilege to set the foreground window) from one process to another. The process that has the foreground privilege can call this function to pass that privilege on to a local COM server process.
helpviewer_keywords: ["CoAllowSetForegroundWindow","CoAllowSetForegroundWindow function [COM]","_com_CoAllowSetForegroundWindow","com.coallowsetforegroundwindow","objbase/CoAllowSetForegroundWindow"]
old-location: com\coallowsetforegroundwindow.htm
tech.root: com
ms.assetid: a728aaad-3d7a-425c-b886-ba35c4fa54d0
ms.date: 12/05/2018
ms.keywords: CoAllowSetForegroundWindow, CoAllowSetForegroundWindow function [COM], _com_CoAllowSetForegroundWindow, com.coallowsetforegroundwindow, objbase/CoAllowSetForegroundWindow
req.header: objbase.h
req.include-header: 
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
req.lib: Ole32.lib
req.dll: Ole32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - CoAllowSetForegroundWindow
 - objbase/CoAllowSetForegroundWindow
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - ext-ms-win-com-ole32-l1-4-0.dll
 - ext-ms-win-com-ole32-l1-3-0.dll
 - ext-ms-win-com-ole32-l1-2-0.dll
 - ext-ms-win-com-ole32-l1-1-5.dll
 - Ole32.dll
 - ComBase.dll
 - Ext-MS-Win-COM-OLE32-l1-1-1.dll
 - Ext-MS-Win-COM-OLE32-l1-1-2.dll
 - ext-ms-win-com-ole32-l1-1-3.dll
 - Ext-MS-Win-Com-Ole32-L1-1-4.dll
api_name:
 - CoAllowSetForegroundWindow
req.apiset: ext-ms-win-com-ole32-l1-1-1 (introduced in Windows 8.1)
---

# CoAllowSetForegroundWindow function


## -description

This function passes the foreground privilege (the privilege to set the foreground window) from one process to another. The process that has the foreground privilege can call this function to pass that privilege on to a local COM server process. Note that calling <b>CoAllowSetForegroundWindow</b> only confers the privilege; it does not set the foreground window itself. Foreground and focus are only taken away from the client application when the target COM server calls either <a href="/windows/desktop/api/winuser/nf-winuser-setforegroundwindow">SetForegroundWindow</a> or another API that does so indirectly.

## -parameters

### -param pUnk [in]

A pointer to the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface on the proxy of the 
      target COM server.

### -param lpvReserved [in]

This parameter is reserved and must be <b>NULL</b>.

## -returns

This function can return the following values.

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
The method was successful.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
The <i>lpvReserved</i> parameter is not <b>NULL</b>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_NOINTERFACE</b></dt>
</dl>
</td>
<td width="60%">
The <i>pUnk</i> parameter does not support foreground window control.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_ACCESSDENIED</b></dt>
</dl>
</td>
<td width="60%">
The calling process does not currently possess the foreground privilege.

</td>
</tr>
</table>

## -remarks

The system restricts which processes can call the 
    <a href="/windows/desktop/api/winuser/nf-winuser-setforegroundwindow">SetForegroundWindow</a> and 
    <a href="/windows/desktop/api/winuser/nf-winuser-allowsetforegroundwindow">AllowSetForegroundWindow</a> functions to 
    set the foreground window. As a result, an application is blocked from stealing the focus from another application 
    even when the user is interacting with it. Use <b>CoAllowSetForegroundWindow</b> to pass on the foreground privilege from a process that has it to a process that does not yet have it. This can be done transitively: passing the privilege from one process to another, and then to another, and so on.

<b>CoAllowSetForegroundWindow</b> enables a user 
    that has a custom interface to get the same behavior that happens for OLE interfaces where a change of window is 
    expected (primarily associated with linking and embedding).

Behind the scenes, the <a href="/windows/desktop/api/objidl/nn-objidl-iforegroundtransfer">IForegroundTransfer</a> interface is used to yield the foreground window between processes. A standard COM-provided proxy already implements <b>IForegroundTransfer</b>, so you don't have to do any extra work if you're using a standard proxy. Just call <b>CoAllowSetForegroundWindow</b> to transfer the foreground privilege to any out-of-process COM object.


#### Examples

The following example demonstrates how a client process can create a local COM server, call <b>CoAllowSetForegroundWindow</b> to transfer the foreground privilege, and then call a function on  the COM server that in turn directly or indirectly calls <a href="/windows/desktop/api/winuser/nf-winuser-setforegroundwindow">SetForegroundWindow</a>.


```cpp
Microsoft::WRL::ComPtr<IExampleInterface> exampleLocalServer;

ThrowIfFailed(::CoCreateInstance(CLSID_ExampleLocalServer,
	nullptr, CLSCTX_LOCAL_SERVER, IID_PPV_ARGS(&exampleLocalServer)));

// You can adapt to success or failure, but don't automatically throw. Don’t make the
// opening of a window dependent on successfully passing privilege (and taking foreground),
// because the window will signal to the user that it is ready to take focus.
HRESULT hr = ::CoAllowSetForegroundWindow(exampleLocalServer.Get(), nullptr);

// Call an example method that itself calls ::SetForegroundWindow(HWND).
hr = exampleLocalServer->FunctionThatSetsForegroundWindow();
```

## -see-also

<a href="/windows/desktop/api/objidl/nn-objidl-iforegroundtransfer">IForegroundTransfer</a>
