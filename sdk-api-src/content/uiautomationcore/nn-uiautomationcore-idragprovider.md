---
UID: NN:uiautomationcore.IDragProvider
title: IDragProvider (uiautomationcore.h)
description: Enables a Microsoft UI Automation element to describe itself as an element that can be dragged as part of a drag-and-drop operation.
helpviewer_keywords: ["IDragProvider","IDragProvider interface [Windows Accessibility]","IDragProvider interface [Windows Accessibility]","described","uiautomationcore/IDragProvider","winauto.uiauto_idragprovider"]
old-location: winauto\uiauto_idragprovider.htm
tech.root: WinAuto
ms.assetid: FAC4A56D-17BC-42E6-A03E-EE45D717DE37
ms.date: 12/05/2018
ms.keywords: IDragProvider, IDragProvider interface [Windows Accessibility], IDragProvider interface [Windows Accessibility],described, uiautomationcore/IDragProvider, winauto.uiauto_idragprovider
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
req.dll: UIAutomationCore.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IDragProvider
 - uiautomationcore/IDragProvider
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
 - IDragProvider
---

# IDragProvider interface


## -description

Enables a Microsoft UI Automation element to describe itself as an element that can be dragged as part of a drag-and-drop operation.

## -inheritance

The <b>IDragProvider</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IDragProvider</b> also has these types of members:

## -remarks

A provider can implement <b>IDragProvider</b> only on the element being dragged, or it can use an intermediary drag object that implements <b>IDragProvider</b>, in addition to the <b>IDragProvider</b> implementation on the individual element.  The intermediary is responsible for firing all events, which enables the provider to support dragging multiple elements at once, and to describe the multi-element drag operation with a single set of drag properties and events.

## -see-also

<a href="/windows/desktop/api/uiautomationcore/nn-uiautomationcore-idroptargetprovider">IDropTargetProvider</a>



<a href="/windows/desktop/WinAuto/ui-automation-support-for-drag-and-drop">UI Automation Support for Drag-and-Drop</a>
