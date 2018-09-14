---
UID: NF:directmanipulation.IDirectManipulationManager.Activate
title: IDirectManipulationManager::Activate
author: windows-sdk-content
description: Activates Direct Manipulation for processing input and handling callbacks on the specified window.
old-location: directmanipulation\idirectmanipulationmanager_activate.htm
tech.root: directmanipulation
ms.assetid: 49a5eccd-16a9-4dca-af78-224fd5acb611
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: Activate, Activate method [Direct Manipulation], Activate method [Direct Manipulation],IDirectManipulationManager interface, IDirectManipulationManager interface [Direct Manipulation],Activate method, IDirectManipulationManager.Activate, IDirectManipulationManager::Activate, directmanipulation.idirectmanipulationmanager_activate, directmanipulation/IDirectManipulationManager::Activate
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
 - IDirectManipulationManager.Activate
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
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


```
LRESULT WndProc(HWND hwnd, UINT msg, WPARAM wParam, LPARAM lParam )
{
    BOOL handled = FALSE;
    switch ( msg )
    {
    case WM_SIZE:
        switch ( wParam)
        {
        case SIZE_MINIMIZED:
        case SIZE_MAXHIDE:
            pManipulationManager->Deactivate(hwnd);
            break;

        default:
            pManipulationManager->Activate(hwnd);
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
}
```





## -see-also




<a href="https://msdn.microsoft.com/d730a446-984e-4be0-aa7f-6d3dc93b2e34">IDirectManipulationManager</a>
 

 

