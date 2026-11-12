---
UID: NF:uiautomationcore.IRawElementProviderComponent.get_ElementId
tech.root: WinAuto
title: IRawElementProviderComponent::get_ElementId
ms.date: 11/12/2026
targetos: Windows
description: Retrieves an optional identifier for an element within a UI Automation endpoint.
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
 - IRawElementProviderComponent::get_ElementId
f1_keywords:
 - IRawElementProviderComponent::get_ElementId
 - uiautomationcore/IRawElementProviderComponent::get_ElementId
dev_langs:
 - c++
helpviewer_keywords:
 - get_ElementId
---

# IRawElementProviderComponent::get_ElementId method

## -description

Retrieves an optional identifier for an element within a UI Automation endpoint.

## -parameters

### -param elementIdOut [out, retval]

Type: **BSTR\***

Receives the element identifier. Return an empty string or **NULL** to select the endpoint's fragment root directly.

For a nonempty value, allocate the string with [SysAllocString](/windows/win32/api/oleauto/nf-oleauto-sysallocstring) or an equivalent **BSTR** allocation function. The caller frees the returned string with [SysFreeString](/windows/win32/api/oleauto/nf-oleauto-sysfreestring).

## -returns

Return **S_OK** on success, or an **HRESULT** error code on failure.

## -remarks

When this property returns a nonempty identifier, the endpoint's fragment root must implement [IComponentElementFinder](nn-uiautomationcore-icomponentelementfinder.md). UI Automation passes the identifier to **FindElement** to obtain the corresponding provider.

The identifier is scoped to the endpoint and is separate from the endpoint GUID returned by [ComponentSiteId](nf-uiautomationcore-irawelementprovidercomponent-get_componentsiteid.md). It is not required to be a UI Automation **AutomationId** property value.

## -see-also

[IRawElementProviderComponent](nn-uiautomationcore-irawelementprovidercomponent.md)

[IComponentElementFinder::FindElement](nf-uiautomationcore-icomponentelementfinder-findelement.md)
