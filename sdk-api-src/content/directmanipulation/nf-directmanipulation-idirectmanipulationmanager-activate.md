---
UID: NF:directmanipulation.IDirectManipulationManager.Activate
title: IDirectManipulationManager::Activate (directmanipulation.h)
description: Activates Direct Manipulation for processing input and handling callbacks on the specified window.
helpviewer_keywords: ["Activate","Activate method [Direct Manipulation]","Activate method [Direct Manipulation]","IDirectManipulationManager interface","IDirectManipulationManager interface [Direct Manipulation]","Activate method","IDirectManipulationManager.Activate","IDirectManipulationManager::Activate","directmanipulation.idirectmanipulationmanager_activate","directmanipulation/IDirectManipulationManager::Activate"]
old-location: directmanipulation\idirectmanipulationmanager_activate.htm
tech.root: directmanipulation
ms.assetid: 49a5eccd-16a9-4dca-af78-224fd5acb611
ms.date: 12/05/2018
ms.keywords: Activate, Activate method [Direct Manipulation], Activate method [Direct Manipulation],IDirectManipulationManager interface, IDirectManipulationManager interface [Direct Manipulation],Activate method, IDirectManipulationManager.Activate, IDirectManipulationManager::Activate, directmanipulation.idirectmanipulationmanager_activate, directmanipulation/IDirectManipulationManager::Activate
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IDirectManipulationManager::Activate
 - directmanipulation/IDirectManipulationManager::Activate
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - DirectManipulation.h
api_name:
 - IDirectManipulationManager.Activate
---

# IDirectManipulationManager::Activate


## -description

Activates <a href="/previous-versions/windows/desktop/directmanipulation/direct-manipulation-portal">Direct Manipulation</a> for processing input and  handling callbacks on the specified window.

## -parameters

### -param window [in]

The window in which to activate <a href="/previous-versions/windows/desktop/directmanipulation/direct-manipulation-portal">Direct Manipulation</a>.

## -returns

If the method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

The manipulation manager is deactivated, by default. The manager does not receive or respond to input and callbacks until <b>Activate</b> is called for the window.  

Calls to <b>Activate</b> and <a href="/previous-versions/windows/desktop/api/directmanipulation/nf-directmanipulation-idirectmanipulationmanager-deactivate">Deactivate</a> are reference counted.



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

<a href="/previous-versions/windows/desktop/api/directmanipulation/nn-directmanipulation-idirectmanipulationmanager">IDirectManipulationManager</a>