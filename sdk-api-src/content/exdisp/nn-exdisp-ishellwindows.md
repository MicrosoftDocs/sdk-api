---
UID: NN:exdisp.IShellWindows
title: IShellWindows (exdisp.h)
description: Provides access to the collection of open Shell windows.
old-location: shell\IShellWindows.htm
tech.root: shell
ms.assetid: e609c8b6-2b2e-4188-894c-5c85960206ea
ms.date: 12/05/2018
ms.keywords: IShellWindows, IShellWindows interface [Windows Shell], IShellWindows interface [Windows Shell],described, _win32_IShellWindows, exdisp/IShellWindows, shell.IShellWindows
f1_keywords:
- exdisp/IShellWindows
dev_langs:
- c++
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
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- Shdocvw.dll
api_name:
- IShellWindows
targetos: Windows
req.typenames: 
req.redist: 
req.product: Internet Explorer 5
ms.custom: 19H1
---

# IShellWindows interface


## -description


Provides access to the collection of open Shell windows.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IShellWindows</b> interface inherits from the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface. <b>IShellWindows</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IShellWindows</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/win32/api/exdisp/nf-exdisp-ishellwindows-_newenum">_NewEnum</a>
</td>
<td align="left" width="63%">
Retrieves an enumerator for the collection of Shell windows.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/exdisp/nf-exdisp-ishellwindows-findwindowsw">FindWindowSW</a>
</td>
<td align="left" width="63%">
Finds a window in the Shell windows collection and returns the window's handle and <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/exdisp/nf-exdisp-ishellwindows-get_count">get_Count</a>
</td>
<td align="left" width="63%">
Gets the number of windows in the Shell windows collection.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/exdisp/nf-exdisp-ishellwindows-item">Item</a>
</td>
<td align="left" width="63%">
Returns the registered Shell window for a specified index.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/exdisp/nf-exdisp-ishellwindows-onactivated">OnActivated</a>
</td>
<td align="left" width="63%">
Occurs when a Shell window's activation state changes.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/exdisp/nf-exdisp-ishellwindows-oncreated">OnCreated</a>
</td>
<td align="left" width="63%">
Occurs when a new Shell window is created for a frame.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/exdisp/nf-exdisp-ishellwindows-onnavigate">OnNavigate</a>
</td>
<td align="left" width="63%">
Occurs when a Shell window is navigated to a new location.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/exdisp/nf-exdisp-ishellwindows-processattachdetach">ProcessAttachDetach</a>
</td>
<td align="left" width="63%">
Deprecated. Always returns S_OK.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/exdisp/nf-exdisp-ishellwindows-register">Register</a>
</td>
<td align="left" width="63%">
Registers an open window as a Shell window; the window is specified by handle.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/exdisp/nf-exdisp-ishellwindows-registerpending">RegisterPending</a>
</td>
<td align="left" width="63%">
Registers a pending window as a Shell window; the window is specified by an absolute PIDL.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/exdisp/nf-exdisp-ishellwindows-revoke">Revoke</a>
</td>
<td align="left" width="63%">
Revokes a Shell window's registration and removes the window from the Shell windows collection.

</td>
</tr>
</table> 


## -remarks



A <i>Shell window</i> is a window that has been registered by calling <a href="https://docs.microsoft.com/windows/desktop/api/exdisp/nf-exdisp-ishellwindows-register">IShellWindows::Register</a> or <a href="https://docs.microsoft.com/windows/desktop/api/exdisp/nf-exdisp-ishellwindows-registerpending">IShellWindows::RegisterPending</a>. Upon registration, the specified window is added to the collection of Shell windows, and granted a cookie that uniquely identifies the window within the collection. A window can be un-registered by calling <a href="https://docs.microsoft.com/windows/desktop/api/exdisp/nf-exdisp-ishellwindows-revoke">IShellWindows::Revoke</a>.

The Shell windows collection includes file explorer windows and web browser windows Internet Explorer and 3rd-party web browsers). Normally each Shell window implements <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a>; <a href="https://docs.microsoft.com/windows/desktop/api/exdisp/nf-exdisp-ishellwindows-item">IShellWindows::Item</a> and <a href="https://docs.microsoft.com/windows/desktop/api/exdisp/nf-exdisp-ishellwindows-findwindowsw">IShellWindows::FindWindowSW</a> provide ways to access a Shell window's <b>IDispatch</b> interface. For more information, see <a href="https://docs.microsoft.com/previous-versions/windows/desktop/automat/dispatch-interfaces">Dispatch Interface and Automation Functions</a>.


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




<a href="https://docs.microsoft.com/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance">CoCreateInstance</a>



<a href="https://docs.microsoft.com/windows/desktop/api/objbase/nf-objbase-coinitialize">CoInitialize</a>



<a href="https://docs.microsoft.com/windows/desktop/shell/dshellwindowsevents">DShellWindowsEvents</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a>



<a href="https://docs.microsoft.com/windows/desktop/shell/shellwindows">ShellWindows</a>
 

 

