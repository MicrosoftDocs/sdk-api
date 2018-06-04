---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# IDirectManipulationManager::Activate


## -description


Activates <a href="https://msdn.microsoft.com/26358bc5-71e9-40f0-9243-9bddd961a0e5">Direct Manipulation</a> for processing input and  handling callbacks on the specified window. 


## -parameters




### -param window [in]

The window in which to activate <a href="https://msdn.microsoft.com/26358bc5-71e9-40f0-9243-9bddd961a0e5">Direct Manipulation</a>.


## -returns



If the method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.




## -remarks



The manipulation manager is deactivated, by default. The manager does not receive or respond to input and callbacks until <b>Activate</b> is called for the window.  

Calls to <b>Activate</b> and <a href="https://msdn.microsoft.com/7f80fe8a-e088-41fa-b72e-2b248307ac4a">Deactivate</a> are reference counted.



#### Examples

The following example shows how to activate and deactivate input processing.

<div class="code"><span codelanguage=""><table>
<tr>
<th></th>
</tr>
<tr>
<td>
<pre>LRESULT WndProc(HWND hwnd, UINT msg, WPARAM wParam, LPARAM lParam )
{
    BOOL handled = FALSE;
    switch ( msg )
    {
    case WM_SIZE:
        switch ( wParam)
        {
        case SIZE_MINIMIZED:
        case SIZE_MAXHIDE:
            pManipulationManager-&gt;Deactivate(hwnd);
            break;

        default:
            pManipulationManager-&gt;Activate(hwnd);
            break;
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
}</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/d730a446-984e-4be0-aa7f-6d3dc93b2e34">IDirectManipulationManager</a>
 

 

