---
UID: NN:uiautomationcore.ISelectionProvider
title: ISelectionProvider (uiautomationcore.h)
description: Provides access to controls that act as containers for a collection of individual, selectable child items.
helpviewer_keywords: ["ISelectionProvider","ISelectionProvider interface [Windows Accessibility]","ISelectionProvider interface [Windows Accessibility]","described","uiauto.uiauto_ISelectionProvider","uiauto_ISelectionProvider","uiautomationcore/ISelectionProvider","winauto.uiauto_ISelectionProvider"]
old-location: winauto\uiauto_ISelectionProvider.htm
tech.root: WinAuto
ms.assetid: e02731f8-e58d-4c66-95bf-005cf954471c
ms.date: 12/05/2018
ms.keywords: ISelectionProvider, ISelectionProvider interface [Windows Accessibility], ISelectionProvider interface [Windows Accessibility],described, uiauto.uiauto_ISelectionProvider, uiauto_ISelectionProvider, uiautomationcore/ISelectionProvider, winauto.uiauto_ISelectionProvider
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
req.dll: UIAutomationCore.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ISelectionProvider
 - uiautomationcore/ISelectionProvider
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - UIAutomationCore.dll
api_name:
 - ISelectionProvider
---

# ISelectionProvider interface


## -description

Provides access 
        to controls that act as containers for a collection of individual, selectable child items. 
        The children of this control must implement <a href="/windows/desktop/api/uiautomationcore/nn-uiautomationcore-iselectionitemprovider">ISelectionItemProvider</a>.

## -inheritance

The <b>ISelectionProvider</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>ISelectionProvider</b> also has these types of members:

## -remarks

This interface is implemented by a UI Automation provider.

Providers should raise an event of type <a href="/windows/desktop/WinAuto/uiauto-event-ids">UIA_Selection_InvalidatedEventId</a> when a selection in a container has changed significantly.

## -see-also

<a href="/windows/desktop/WinAuto/uiauto-providersoverview">UI Automation Providers Overview</a>
