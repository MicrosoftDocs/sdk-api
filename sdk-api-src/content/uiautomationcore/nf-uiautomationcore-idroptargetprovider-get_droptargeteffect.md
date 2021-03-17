---
UID: NF:uiautomationcore.IDropTargetProvider.get_DropTargetEffect
title: IDropTargetProvider::get_DropTargetEffect (uiautomationcore.h)
description: Retrieves a localized string that describes the effect that happens when the user drops the grabbed element on this drop target.
helpviewer_keywords: ["DropTargetEffect property [Windows Accessibility]","DropTargetEffect property [Windows Accessibility]","IDropTargetProvider interface","IDropTargetProvider interface [Windows Accessibility]","DropTargetEffect property","IDropTargetProvider.DropTargetEffect","IDropTargetProvider.get_DropTargetEffect","IDropTargetProvider::DropTargetEffect","IDropTargetProvider::get_DropTargetEffect","get_DropTargetEffect","uiautomationcore/IDropTargetProvider::DropTargetEffect","uiautomationcore/IDropTargetProvider::get_DropTargetEffect","winauto.uiauto_idroptargetprovider_droptargeteffect"]
old-location: winauto\uiauto_idroptargetprovider_droptargeteffect.htm
tech.root: WinAuto
ms.assetid: F94D0513-543D-4B9D-A665-2197349C3B55
ms.date: 12/05/2018
ms.keywords: DropTargetEffect property [Windows Accessibility], DropTargetEffect property [Windows Accessibility],IDropTargetProvider interface, IDropTargetProvider interface [Windows Accessibility],DropTargetEffect property, IDropTargetProvider.DropTargetEffect, IDropTargetProvider.get_DropTargetEffect, IDropTargetProvider::DropTargetEffect, IDropTargetProvider::get_DropTargetEffect, get_DropTargetEffect, uiautomationcore/IDropTargetProvider::DropTargetEffect, uiautomationcore/IDropTargetProvider::get_DropTargetEffect, winauto.uiauto_idroptargetprovider_droptargeteffect
req.header: uiautomationcore.h
req.include-header: UIAutomation.h
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2012 [desktop apps \| UWP apps]
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
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IDropTargetProvider::get_DropTargetEffect
 - uiautomationcore/IDropTargetProvider::get_DropTargetEffect
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - UIAutomationCore.h
api_name:
 - IDropTargetProvider.DropTargetEffect
 - IDropTargetProvider.get_DropTargetEffect
---

# IDropTargetProvider::get_DropTargetEffect


## -description

Retrieves a localized string that describes the effect that happens when the user drops the grabbed element on this drop target.

This property is read-only.

## -parameters

## -remarks

This property describes the default effect that happens when the user drops a grabbed element on a target, such as moving or copying the element.  This property can be a short string such as "move", or a longer one such as "insert into Main group".  The string is always localized.

If this property changes, the provider must notify clients by firing a <a href="/windows/desktop/WinAuto/uiauto-event-ids">UIA_AutomationPropertyChangedEventId</a> event. 



#### Examples


```cpp
IFACEMETHODIMP CRegionProvider::get_DropTargetEffect(BSTR * pDefaultDropAction)
{
    WCHAR wszDropAction[100];
    LoadString(g_hInstance, IDS_REGION_DEFAULTDROPACTION1, wszDropAction, 
        ARRAYSIZE(wszDropAction));
    *pDefaultDropAction = ::SysAllocString(wszDropAction);
    return (*pDefaultDropAction == nullptr) ? E_OUTOFMEMORY : S_OK;
}

```

## -see-also

<a href="/windows/desktop/api/uiautomationcore/nn-uiautomationcore-idroptargetprovider">IDropTargetProvider</a>