---
UID: NF:uiautomationcore.IDragProvider.get_DropEffect
title: IDragProvider::get_DropEffect (uiautomationcore.h)
description: Retrieves a localized string that indicates what happens when this element is dropped as part of a drag-drop operation.
helpviewer_keywords: ["DropEffect property [Windows Accessibility]","DropEffect property [Windows Accessibility]","IDragProvider interface","IDragProvider interface [Windows Accessibility]","DropEffect property","IDragProvider.DropEffect","IDragProvider.get_DropEffect","IDragProvider::DropEffect","IDragProvider::get_DropEffect","get_DropEffect","uiautomationcore/IDragProvider::DropEffect","uiautomationcore/IDragProvider::get_DropEffect","winauto.uiauto_idragprovider_dropeffect"]
old-location: winauto\uiauto_idragprovider_dropeffect.htm
tech.root: WinAuto
ms.assetid: 90850574-83EA-4291-99D0-391D8CACFE9F
ms.date: 12/05/2018
ms.keywords: DropEffect property [Windows Accessibility], DropEffect property [Windows Accessibility],IDragProvider interface, IDragProvider interface [Windows Accessibility],DropEffect property, IDragProvider.DropEffect, IDragProvider.get_DropEffect, IDragProvider::DropEffect, IDragProvider::get_DropEffect, get_DropEffect, uiautomationcore/IDragProvider::DropEffect, uiautomationcore/IDragProvider::get_DropEffect, winauto.uiauto_idragprovider_dropeffect
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
 - IDragProvider::get_DropEffect
 - uiautomationcore/IDragProvider::get_DropEffect
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
 - IDragProvider.DropEffect
 - IDragProvider.get_DropEffect
---

# IDragProvider::get_DropEffect


## -description

Retrieves a localized string that indicates what happens when this element is dropped as part of a drag-drop operation.

This property is read-only.

## -parameters

## -remarks

In the source-only style of UI Automation drag-and-drop, no elements implement the <a href="/windows/desktop/WinAuto/uiauto-implementingdroptarget">DropTarget</a> pattern.  To find out what effect dropping the dragged element will have, a client can query the <b>DropEffect</b> property of the dragged element.  This property can be a short string such as "move", or a longer one, such as "insert into Main group".  The string is always localized.

If this property changes, the provider must notify clients by calling <a href="/windows/desktop/api/uiautomationcoreapi/nf-uiautomationcoreapi-uiaraiseautomationpropertychangedevent">UiaRaiseAutomationPropertyChangedEvent</a> and specifying a property identifier of <a href="/windows/desktop/WinAuto/uiauto-control-pattern-propids">UIA_DragIsGrabbedPropertyId</a> or <a href="/windows/desktop/WinAuto/uiauto-control-pattern-propids">UIA_DragDropEffectPropertyId</a>.

## -see-also

<a href="/windows/desktop/api/uiautomationcore/nn-uiautomationcore-idragprovider">IDragProvider</a>