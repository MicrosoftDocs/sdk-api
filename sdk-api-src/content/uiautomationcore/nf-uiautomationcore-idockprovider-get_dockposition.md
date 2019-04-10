---
UID: NF:uiautomationcore.IDockProvider.get_DockPosition
title: IDockProvider::get_DockPosition (uiautomationcore.h)
author: windows-sdk-content
description: Indicates the current docking position of this element.
old-location: winauto\uiauto_IDockProvider_DockPosition.htm
tech.root: WinAuto
ms.assetid: aa170dec-a4e1-48ac-8434-a24b79006653
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: DockPosition property [Windows Accessibility], DockPosition property [Windows Accessibility],IDockProvider interface, IDockProvider interface [Windows Accessibility],DockPosition property, IDockProvider.DockPosition, IDockProvider.get_DockPosition, IDockProvider::DockPosition, IDockProvider::get_DockPosition, get_DockPosition, uiauto.uiauto_IDockProvider_DockPosition, uiauto_IDockProvider_DockPosition, uiautomationcore/IDockProvider::DockPosition, uiautomationcore/IDockProvider::get_DockPosition, winauto.uiauto_IDockProvider_DockPosition
ms.topic: method
req.header: uiautomationcore.h
req.include-header: UIAutomation.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2003 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: UIAutomationCore.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: Uiautomationcore.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Uiautomationcore.dll
api_name:
 - IDockProvider.DockPosition
 - IDockProvider.get_DockPosition
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDockProvider::get_DockPosition


## -description


Indicates the current docking position of this element.
				

This property is read-only.


## -parameters


## -remarks



A docking container is a control that allows the arrangement of child elements, both horizontally and vertically, relative to the boundaries of the docking container and other elements in the container.


#### Examples

The following example shows how to return the DockPosition property.
			


```cpp

    // dockPosition is a global variable of type DockPosition.

    HRESULT STDMETHODCALLTYPE BucketControl::get_DockPosition(DockPosition *pRetVal)
    {
        if (pRetVal == NULL)
        {
            return E_INVALIDARG;
        }
        *pRetVal = dockPosition;
        return S_OK;
    }
            
```





## -see-also




<a href="https://msdn.microsoft.com/106ca4b4-1304-4942-88a4-79a3895b552f">IDockProvider</a>



<a href="https://msdn.microsoft.com/8928c889-0e0a-439f-87e8-a9d121fcf73f">UI Automation Providers Overview</a>
 

 

