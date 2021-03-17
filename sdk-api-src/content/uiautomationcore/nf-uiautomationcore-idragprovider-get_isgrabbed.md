---
UID: NF:uiautomationcore.IDragProvider.get_IsGrabbed
title: IDragProvider::get_IsGrabbed (uiautomationcore.h)
description: Indicates whether the element has been grabbed as part of a drag-and-drop operation.
helpviewer_keywords: ["IDragProvider interface [Windows Accessibility]","IsGrabbed property","IDragProvider.IsGrabbed","IDragProvider.get_IsGrabbed","IDragProvider::IsGrabbed","IDragProvider::get_IsGrabbed","IsGrabbed property [Windows Accessibility]","IsGrabbed property [Windows Accessibility]","IDragProvider interface","get_IsGrabbed","uiautomationcore/IDragProvider::IsGrabbed","uiautomationcore/IDragProvider::get_IsGrabbed","winauto.uiauto_idragprovider_isgrabbed"]
old-location: winauto\uiauto_idragprovider_isgrabbed.htm
tech.root: WinAuto
ms.assetid: E2A472A0-F9CE-4778-96DD-60B00D53EEA6
ms.date: 12/05/2018
ms.keywords: IDragProvider interface [Windows Accessibility],IsGrabbed property, IDragProvider.IsGrabbed, IDragProvider.get_IsGrabbed, IDragProvider::IsGrabbed, IDragProvider::get_IsGrabbed, IsGrabbed property [Windows Accessibility], IsGrabbed property [Windows Accessibility],IDragProvider interface, get_IsGrabbed, uiautomationcore/IDragProvider::IsGrabbed, uiautomationcore/IDragProvider::get_IsGrabbed, winauto.uiauto_idragprovider_isgrabbed
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
 - IDragProvider::get_IsGrabbed
 - uiautomationcore/IDragProvider::get_IsGrabbed
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
 - IDragProvider.IsGrabbed
 - IDragProvider.get_IsGrabbed
---

# IDragProvider::get_IsGrabbed


## -description

Indicates whether the element has been grabbed as part of a drag-and-drop operation.

This property is read-only.

## -parameters

## -remarks

If this property changes, the provider must notify clients by calling <a href="/windows/desktop/api/uiautomationcoreapi/nf-uiautomationcoreapi-uiaraiseautomationpropertychangedevent">UiaRaiseAutomationPropertyChangedEvent</a> and specifying a property identifier of <a href="/windows/desktop/WinAuto/uiauto-control-pattern-propids">UIA_DragIsGrabbedPropertyId</a> or <a href="/windows/desktop/WinAuto/uiauto-control-pattern-propids">UIA_DragDropEffectPropertyId</a>.

## -see-also

<a href="/windows/desktop/api/uiautomationcore/nn-uiautomationcore-idragprovider">IDragProvider</a>