---
UID: NF:uiautomationcore.IComponentElementFinder.FindElement
tech.root: WinAuto
title: IComponentElementFinder::FindElement
ms.date: 11/12/2026
targetos: Windows
description: Resolves an element identifier to a provider fragment within an endpoint.
prerelease: false
req.construct-type: function
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
 - IComponentElementFinder::FindElement
f1_keywords:
 - IComponentElementFinder::FindElement
 - uiautomationcore/IComponentElementFinder::FindElement
dev_langs:
 - c++
helpviewer_keywords:
 - FindElement
---

# IComponentElementFinder::FindElement method

## -description

Resolves an element identifier to a provider fragment within an endpoint.

## -parameters

### -param elementId [in]

Type: **BSTR**

The identifier returned by [IRawElementProviderComponent::get_ElementId](nf-uiautomationcore-irawelementprovidercomponent-get_elementid.md). The caller owns this string; the implementation must not free it.

### -param elementOut [out, retval]

Type: **[IRawElementProviderFragment](nn-uiautomationcore-irawelementproviderfragment.md)\*\***

Receives the provider fragment corresponding to *elementId*. A returned interface pointer must have an added reference; the caller releases it when finished.

## -returns

Return **S_OK** on success, or an **HRESULT** error code on failure.

## -remarks

Implement this method on the endpoint's fragment root. The implementation maps the identifier to an element in its provider tree.

UI Automation uses this lookup for nonempty component element IDs. If all component elements return an empty ID, UI Automation uses the endpoint's fragment root directly and does not require **IComponentElementFinder**.

## -see-also

[IComponentElementFinder](nn-uiautomationcore-icomponentelementfinder.md)

[IRawElementProviderComponent](nn-uiautomationcore-irawelementprovidercomponent.md)
