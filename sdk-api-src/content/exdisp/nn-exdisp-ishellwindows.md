---
UID: NN:exdisp.IShellWindows
title: IShellWindows
author: windows-sdk-content
description: Provides access to the collection of open Shell windows.
old-location: shell\IShellWindows.htm
old-project: shell
ms.assetid: e609c8b6-2b2e-4188-894c-5c85960206ea
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: IShellWindows, IShellWindows interface [Windows Shell], IShellWindows interface [Windows Shell],described, _win32_IShellWindows, exdisp/IShellWindows, shell.IShellWindows
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
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
tech.root: 
req.typenames: ShellWindowTypeConstants
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Shdocvw.dll
api_name:
 - IShellWindows
product: Windows
targetos: Windows
req.lib: Shdocvw.dll
req.dll: Shdocvw.dll (version 5.00.2014.0216 or later)
req.irql: 
req.product: Internet Explorer 5
---

# IShellWindows interface


## -description


Provides access to the collection of open Shell windows.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IShellWindows</b> interface inherits from the <a href="ebbff4bc-36b2-4861-9efa-ffa45e013eb5">IDispatch</a> interface. <b>IShellWindows</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/library/windows/hardware/hh439300">_NewEnum</a>
</td>
<td align="left" width="63%">
Retrieves an enumerator for the collection of Shell windows.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/10eed153-cb0b-4ce0-8cc5-2e7ebf683fda">FindWindowSW</a>
</td>
<td align="left" width="63%">
Finds a window in the Shell windows collection and returns the window's handle and <a href="ebbff4bc-36b2-4861-9efa-ffa45e013eb5">IDispatch</a> interface.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/50781569-4c80-4304-96f3-8a135cea3b20">get_Count</a>
</td>
<td align="left" width="63%">
Gets the number of windows in the Shell windows collection.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/hh451057">Item</a>
</td>
<td align="left" width="63%">
Returns the registered Shell window for a specified index.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ccd93f0f-3cd2-4b18-b6d2-834665d8b658">OnActivated</a>
</td>
<td align="left" width="63%">
Occurs when a Shell window's activation state changes.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ef2f75fe-dc93-403d-af1a-c08c45e2d818">OnCreated</a>
</td>
<td align="left" width="63%">
Occurs when a new Shell window is created for a frame.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/b65bc979-db32-48b3-b71f-fd389957b265">OnNavigate</a>
</td>
<td align="left" width="63%">
Occurs when a Shell window is navigated to a new location.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/79bc04f0-7b03-40aa-8324-7b4eccc8c527">ProcessAttachDetach</a>
</td>
<td align="left" width="63%">
Deprecated. Always returns S_OK.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/4545cc34-2209-41a5-ab65-283f2985cce0">Register</a>
</td>
<td align="left" width="63%">
Registers an open window as a Shell window; the window is specified by handle.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/75e8b82c-a94e-4aad-a224-f12b22b8a4b2">RegisterPending</a>
</td>
<td align="left" width="63%">
Registers a pending window as a Shell window; the window is specified by an absolute PIDL.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/66ca2569-b763-445b-b5b5-98ef32c64578">Revoke</a>
</td>
<td align="left" width="63%">
Revokes a Shell window's registration and removes the window from the Shell windows collection.

</td>
</tr>
</table> 


## -remarks



A <i>Shell window</i> is a window that has been registered by calling <a href="https://msdn.microsoft.com/4545cc34-2209-41a5-ab65-283f2985cce0">IShellWindows::Register</a> or <a href="https://msdn.microsoft.com/75e8b82c-a94e-4aad-a224-f12b22b8a4b2">IShellWindows::RegisterPending</a>. Upon registration, the specified window is added to the collection of Shell windows, and granted a cookie that uniquely identifies the window within the collection. A window can be un-registered by calling <a href="https://msdn.microsoft.com/66ca2569-b763-445b-b5b5-98ef32c64578">IShellWindows::Revoke</a>.

The Shell windows collection includes file explorer windows and web browser windows Internet Explorer and 3rd-party web browsers). Normally each Shell window implements <a href="ebbff4bc-36b2-4861-9efa-ffa45e013eb5">IDispatch</a>; <a href="https://msdn.microsoft.com/04157d1a-8a4d-4ffd-882d-41748408ba2b">IShellWindows::Item</a> and <a href="https://msdn.microsoft.com/10eed153-cb0b-4ce0-8cc5-2e7ebf683fda">IShellWindows::FindWindowSW</a> provide ways to access a Shell window's <b>IDispatch</b> interface. For more information, see <a href="75bff268-bd85-49c4-b761-b557f4b1c588">Dispatch Interface and Automation Functions</a>.


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

<div class="code"><span codelanguage=""><table>
<tr>
<th></th>
</tr>
<tr>
<td>
<pre>#include "exdisp.h"
                
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
        (void**)&amp;psw
    );
    
    if (SUCCEEDED(hr))
    {
        // Use the IShellWindows instance...
        
        psw-&gt;Release();
    }
}</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/7295a55b-12c7-4ed0-a7a4-9ecee16afdec">CoCreateInstance</a>



<a href="https://msdn.microsoft.com/0f171cf4-87b9-43a6-97f2-80ed344fe376">CoInitialize</a>



<a href="https://msdn.microsoft.com/c340296d-f8eb-43a1-809d-912ea7412fe2">DShellWindowsEvents</a>



<a href="ebbff4bc-36b2-4861-9efa-ffa45e013eb5">IDispatch</a>



<a href="https://msdn.microsoft.com/cad1f961-7fb4-4ba1-be48-b664d3de2c60">ShellWindows</a>
 

 

