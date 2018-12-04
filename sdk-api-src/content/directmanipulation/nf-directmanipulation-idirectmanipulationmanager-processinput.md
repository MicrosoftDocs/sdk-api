---
UID: NF:directmanipulation.IDirectManipulationManager.ProcessInput
title: IDirectManipulationManager::ProcessInput
author: windows-sdk-content
description: Passes keyboard and mouse messages to the manipulation manager on the app's UI thread.
old-location: directmanipulation\idirectmanipulationmanager_processinput.htm
tech.root: directmanipulation
ms.assetid: ed7fa19b-acfe-4d5d-bd71-a77e5016fe68
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: IDirectManipulationManager interface [Direct Manipulation],ProcessInput method, IDirectManipulationManager.ProcessInput, IDirectManipulationManager::ProcessInput, ProcessInput, ProcessInput method [Direct Manipulation], ProcessInput method [Direct Manipulation],IDirectManipulationManager interface, directmanipulation.idirectmanipulationmanager_processinput, directmanipulation/IDirectManipulationManager::ProcessInput
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: directmanipulation.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: DirectManipulation.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - DirectManipulation.h
api_name:
 - IDirectManipulationManager.ProcessInput
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDirectManipulationManager::ProcessInput


## -description


Passes keyboard and mouse messages to the manipulation manager on the app's UI thread.


## -parameters




### -param message [in]

The input message to process.


### -param handled [out, retval]

<b>TRUE</b> if no further processing should be done with this message; otherwise, <b>FALSE</b>.


## -returns



If the method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.




## -remarks



Call this method for mouse and keyboard input.


#### Examples

The following example shows how to pass messages to the manipulation manager.

<div class="code"><span codelanguage=""><table>
<tr>
<th></th>
</tr>
<tr>
<td>
<pre>LRESULT WndProc(HWND hwnd, UINT message, WPARAM wParam, LPARAM lParam)
{
    BOOL handled = FALSE;

LRESULT WndProc(HWND hwnd, UINT message, WPARAM wParam, LPARAM lParam)
{
    BOOL handled = FALSE;
    switch (msg)
    {
    case WM_KEYDOWN:
    case WM_POINTERWHEEL:
    case WM_POINTERHWHEEL:
    case WM_MOUSEWHEEL:
    case WM_MOUSEHWHEEL:
        MSG msg = {};
        msg.hwnd = hwnd;
        msg.message = message;
        msg.lParam = lParam;
        msg.wParam = wParam;

        if (FAILED(m_pManipulationManager-&gt;ProcessInput(&amp;msg, &amp;handled)))
        {
            handled = false;
        }
        break;
    }

    if ( !handled)
    {
        return DefWindowProc(hwnd,msg,wParam,lParam);
    }
    else
    {
        return 0;
    }
}
</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/d730a446-984e-4be0-aa7f-6d3dc93b2e34">IDirectManipulationManager</a>
 

 

