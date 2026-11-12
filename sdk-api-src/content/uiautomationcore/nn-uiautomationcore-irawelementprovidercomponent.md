---
UID: NN:uiautomationcore.IRawElementProviderComponent
tech.root: WinAuto
title: IRawElementProviderComponent
ms.date: 11/12/2026
targetos: Windows
description: Identifies an endpoint and an optional element within its provider tree for UI Automation tree navigation.
prerelease: false
req.construct-type: iface
req.header: uiautomationcore.h
req.idl: UIAutomationCore.idl
req.target-min-winverclnt:
req.target-min-winversvr:
topic_type:
 - apiref
api_type:
 - COM
api_location:
 - uiautomationcore.h
api_name:
 - IRawElementProviderComponent
f1_keywords:
 - IRawElementProviderComponent
 - uiautomationcore/IRawElementProviderComponent
dev_langs:
 - c++
helpviewer_keywords:
 - IRawElementProviderComponent
---

# IRawElementProviderComponent interface

## -description

Identifies an endpoint and an optional element within its provider tree for UI Automation tree navigation.

## -inheritance

The **IRawElementProviderComponent** interface inherits from [IUnknown](/windows/win32/api/unknwn/nn-unknwn-iunknown).

## -remarks

A host-side placeholder implements this interface to identify the endpoint that supplies its content. UI Automation uses [ComponentSiteId](nf-uiautomationcore-irawelementprovidercomponent-get_componentsiteid.md) to connect to that endpoint. *Component site ID* is the existing API name for the endpoint ID.

[ElementId](nf-uiautomationcore-irawelementprovidercomponent-get_elementid.md) optionally identifies a specific element within the endpoint. When it is nonempty, UI Automation uses [IComponentElementFinder](nn-uiautomationcore-icomponentelementfinder.md) on the endpoint's fragment root to resolve it. When it is empty, UI Automation uses the endpoint's fragment root directly.

Elements within an endpoint can also expose an **ElementId** for lookup without redirecting navigation to another endpoint.

## -see-also

[IUiaEndpointNotifier](nn-uiautomationcore-iuiaendpointnotifier.md)

[IRawElementProviderComponentHostRoot](nn-uiautomationcore-irawelementprovidercomponenthostroot.md)

[IComponentElementFinder](nn-uiautomationcore-icomponentelementfinder.md)
