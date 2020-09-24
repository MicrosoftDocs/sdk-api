---
UID: NF:uiautomationcore.IDockProvider.get_DockPosition
title: IDockProvider::get_DockPosition (uiautomationcore.h)
description: Indicates the current docking position of this element.
helpviewer_keywords: ["DockPosition property [Windows Accessibility]","DockPosition property [Windows Accessibility]","IDockProvider interface","IDockProvider interface [Windows Accessibility]","DockPosition property","IDockProvider.DockPosition","IDockProvider.get_DockPosition","IDockProvider::DockPosition","IDockProvider::get_DockPosition","get_DockPosition","uiauto.uiauto_IDockProvider_DockPosition","uiauto_IDockProvider_DockPosition","uiautomationcore/IDockProvider::DockPosition","uiautomationcore/IDockProvider::get_DockPosition","winauto.uiauto_IDockProvider_DockPosition"]
old-location: winauto\uiauto_IDockProvider_DockPosition.htm
tech.root: WinAuto
ms.assetid: aa170dec-a4e1-48ac-8434-a24b79006653
ms.date: 12/05/2018
ms.keywords: DockPosition property [Windows Accessibility], DockPosition property [Windows Accessibility],IDockProvider interface, IDockProvider interface [Windows Accessibility],DockPosition property, IDockProvider.DockPosition, IDockProvider.get_DockPosition, IDockProvider::DockPosition, IDockProvider::get_DockPosition, get_DockPosition, uiauto.uiauto_IDockProvider_DockPosition, uiauto_IDockProvider_DockPosition, uiautomationcore/IDockProvider::DockPosition, uiautomationcore/IDockProvider::get_DockPosition, winauto.uiauto_IDockProvider_DockPosition
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IDockProvider::get_DockPosition
 - uiautomationcore/IDockProvider::get_DockPosition
dev_langs:
 - c++
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

<a href="/windows/desktop/api/uiautomationcore/nn-uiautomationcore-idockprovider">IDockProvider</a>



<a href="/windows/desktop/WinAuto/uiauto-providersoverview">UI Automation Providers Overview</a>