---
UID: NN:uiautomationcore.IComponentElementFinder
tech.root: WinAuto
title: IComponentElementFinder
ms.date: 11/12/2026
targetos: Windows
description: Resolves an element identifier to an element within a UI Automation endpoint's provider tree.
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
 - IComponentElementFinder
f1_keywords:
 - IComponentElementFinder
 - uiautomationcore/IComponentElementFinder
dev_langs:
 - c++
helpviewer_keywords:
 - IComponentElementFinder
---

# IComponentElementFinder interface

## -description

Resolves an element identifier to an element within a UI Automation endpoint's provider tree.

## -inheritance

The **IComponentElementFinder** interface inherits from [IUnknown](/windows/win32/api/unknwn/nn-unknwn-iunknown).

## -remarks

Implement this interface on the endpoint's fragment root when component elements expose nonempty [IRawElementProviderComponent::ElementId](nf-uiautomationcore-irawelementprovidercomponent-get_elementid.md) values. UI Automation calls [FindElement](nf-uiautomationcore-icomponentelementfinder-findelement.md) to resolve an ID to the corresponding [IRawElementProviderFragment](nn-uiautomationcore-irawelementproviderfragment.md).

The host and endpoint provider must agree on the element identifiers used for this lookup. These identifiers are separate from the GUID that identifies the endpoint.

If all component elements return an empty **ElementId**, this interface is not required. UI Automation uses the endpoint's fragment root directly.

## -see-also

[IRawElementProviderComponent](nn-uiautomationcore-irawelementprovidercomponent.md)

[IRawElementProviderFragmentRoot](nn-uiautomationcore-irawelementproviderfragmentroot.md)
