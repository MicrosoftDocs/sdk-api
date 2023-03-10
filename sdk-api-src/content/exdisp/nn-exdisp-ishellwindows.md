---
UID: NN:exdisp.IShellWindows
title: IShellWindows (exdisp.h)
description: Provides access to the collection of open Shell windows.
helpviewer_keywords: ["IShellWindows","IShellWindows interface [Windows Shell]","IShellWindows interface [Windows Shell]","described","_win32_IShellWindows","exdisp/IShellWindows","shell.IShellWindows"]
old-location: shell\IShellWindows.htm
tech.root: shell
ms.assetid: e609c8b6-2b2e-4188-894c-5c85960206ea
ms.date: 12/05/2018
ms.keywords: IShellWindows, IShellWindows interface [Windows Shell], IShellWindows interface [Windows Shell],described, _win32_IShellWindows, exdisp/IShellWindows, shell.IShellWindows
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
 - IShellWindows
 - exdisp/IShellWindows
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
 - IShellWindows
---

# IShellWindows interface


## -description

Provides access to the collection of open Shell windows.

## -inheritance

The <b>IShellWindows</b> interface inherits from the <a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface. <b>IShellWindows</b> also has these types of members:

## -remarks

A <i>Shell window</i> is a window that has been registered by calling <a href="/windows/desktop/api/exdisp/nf-exdisp-ishellwindows-register">IShellWindows::Register</a> or <a href="/windows/desktop/api/exdisp/nf-exdisp-ishellwindows-registerpending">IShellWindows::RegisterPending</a>. Upon registration, the specified window is added to the collection of Shell windows, and granted a cookie that uniquely identifies the window within the collection. A window can be un-registered by calling <a href="/windows/desktop/api/exdisp/nf-exdisp-ishellwindows-revoke">IShellWindows::Revoke</a>.

The Shell windows collection includes file explorer windows and web browser windows Internet Explorer and 3rd-party web browsers). Normally each Shell window implements <a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a>; <a href="/windows/desktop/api/exdisp/nf-exdisp-ishellwindows-item">IShellWindows::Item</a> and <a href="/windows/desktop/api/exdisp/nf-exdisp-ishellwindows-findwindowsw">IShellWindows::FindWindowSW</a> provide ways to access a Shell window's <b>IDispatch</b> interface. For more information, see <a href="/previous-versions/windows/desktop/automat/dispatch-interfaces">Dispatch Interface and Automation Functions</a>.


<table class="clsStd">
<tr>
<th>IID</th>
<td>IID_IShellWindows (85CB6900-4D95-11CF-960C-0080C7F4EE85)</td>
</tr>
<tr>
<th>CLSID</th>
<td>CLSID_ShellWindows (9BA05972-F6A8-11CF-A442-00A0C90A8F39)</td>
</tr>
</table>
 



The following example shows how to retrieve an <b>IShellWindows</b> instance.


```
#include "exdisp.h"
                
...

IShellWindows *psw;
HRESULT hr;

hr = CoInitialize(NULL);
if (SUCCEEDED(hr))
{
    hr = CoCreateInstance(
        CLSID_ShellWindows,
        NULL,
        CLSCTX_ALL,
        IID_IShellWindows,
        (void**)&psw
    );
    
    if (SUCCEEDED(hr))
    {
        // Use the IShellWindows instance...
        
        psw->Release();
    }
}
```

## -see-also

<a href="/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance">CoCreateInstance</a>



<a href="/windows/desktop/api/objbase/nf-objbase-coinitialize">CoInitialize</a>



<a href="/windows/desktop/shell/dshellwindowsevents">DShellWindowsEvents</a>



<a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a>



<a href="/windows/desktop/shell/shellwindows">ShellWindows</a>
