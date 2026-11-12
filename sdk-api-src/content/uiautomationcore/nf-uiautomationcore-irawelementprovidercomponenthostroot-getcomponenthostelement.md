---
UID: NF:uiautomationcore.IRawElementProviderComponentHostRoot.GetComponentHostElement
tech.root: WinAuto
title: IRawElementProviderComponentHostRoot::GetComponentHostElement
ms.date: 11/12/2026
targetos: Windows
description: Retrieves the host-side parent fragment corresponding to an endpoint.
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
 - IRawElementProviderComponentHostRoot::GetComponentHostElement
f1_keywords:
 - IRawElementProviderComponentHostRoot::GetComponentHostElement
 - uiautomationcore/IRawElementProviderComponentHostRoot::GetComponentHostElement
dev_langs:
 - c++
helpviewer_keywords:
 - GetComponentHostElement
---

# IRawElementProviderComponentHostRoot::GetComponentHostElement method

## -description

Retrieves the host-side parent fragment corresponding to an endpoint.

## -parameters

### -param componentSiteId [in]

Type: **GUID**

The endpoint ID identifying the hosted component. This is the same value exposed as the component's **ComponentSiteId**.

### -param hostElementOut [out, retval]

Type: **[IRawElementProviderFragment](nn-uiautomationcore-irawelementproviderfragment.md)\*\***

Receives the host-side parent fragment for the specified endpoint. A returned interface pointer must have an added reference; the caller releases it when finished.

## -returns

Return **S_OK** on success, or an **HRESULT** error code on failure.

## -remarks

Implement this method on the host's root provider. UI Automation uses it when navigating upward from an endpoint into the host's provider tree.

Return the host fragment that is the parent of the endpoint's content, not a provider from inside the endpoint.

## -see-also

[IRawElementProviderComponentHostRoot](nn-uiautomationcore-irawelementprovidercomponenthostroot.md)

[IRawElementProviderComponent::get_ComponentSiteId](nf-uiautomationcore-irawelementprovidercomponent-get_componentsiteid.md)
