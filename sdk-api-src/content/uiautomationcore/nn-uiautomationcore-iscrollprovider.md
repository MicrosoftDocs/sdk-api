---
UID: NN:uiautomationcore.IScrollProvider
title: IScrollProvider (uiautomationcore.h)
description: Provides access to controls that act as scrollable containers for a collection of child objects.
helpviewer_keywords: ["IScrollProvider","IScrollProvider interface [Windows Accessibility]","IScrollProvider interface [Windows Accessibility]","described","uiauto.uiauto_IScrollProvider","uiauto_IScrollProvider","uiautomationcore/IScrollProvider","winauto.uiauto_IScrollProvider"]
old-location: winauto\uiauto_IScrollProvider.htm
tech.root: WinAuto
ms.assetid: 55e1b899-aa9f-45eb-9cfa-d645ea659988
ms.date: 12/05/2018
ms.keywords: IScrollProvider, IScrollProvider interface [Windows Accessibility], IScrollProvider interface [Windows Accessibility],described, uiauto.uiauto_IScrollProvider, uiauto_IScrollProvider, uiautomationcore/IScrollProvider, winauto.uiauto_IScrollProvider
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
 - IScrollProvider
 - uiautomationcore/IScrollProvider
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
 - IScrollProvider
---

# IScrollProvider interface


## -description

Provides access 
        to controls that act as scrollable containers for a collection of child objects. 
        The children of this control must implement <a href="/windows/desktop/api/uiautomationcore/nn-uiautomationcore-iscrollitemprovider">IScrollItemProvider</a>.

## -inheritance

The <b>IScrollProvider</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IScrollProvider</b> also has these types of members:

## -remarks

Implemented on a Microsoft UI Automation provider that must 
            support the <a href="/windows/desktop/WinAuto/uiauto-implementingscroll">Scroll</a> control pattern.

## -see-also

<a href="/windows/desktop/WinAuto/uiauto-providersoverview">UI Automation Providers Overview</a>
