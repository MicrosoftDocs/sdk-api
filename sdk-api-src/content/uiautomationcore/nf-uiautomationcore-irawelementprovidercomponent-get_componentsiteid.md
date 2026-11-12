---
UID: NF:uiautomationcore.IRawElementProviderComponent.get_ComponentSiteId
tech.root: WinAuto
title: IRawElementProviderComponent::get_ComponentSiteId
ms.date: 11/12/2026
targetos: Windows
description: Retrieves the endpoint ID used to locate a component's provider.
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
 - IRawElementProviderComponent::get_ComponentSiteId
f1_keywords:
 - IRawElementProviderComponent::get_ComponentSiteId
 - uiautomationcore/IRawElementProviderComponent::get_ComponentSiteId
dev_langs:
 - c++
helpviewer_keywords:
 - get_ComponentSiteId
---

# IRawElementProviderComponent::get_ComponentSiteId method

## -description

Retrieves the endpoint ID used to locate a component's provider.

## -parameters

### -param componentSiteIdOut [out, retval]

Type: **GUID\***

Receives the endpoint ID. For a host-side placeholder that redirects navigation to an endpoint, return the GUID used to register that endpoint.

## -returns

Return **S_OK** on success, or an **HRESULT** error code on failure.

## -remarks

The API uses the name *component site ID* for the endpoint ID. The host and endpoint provider must agree on this value.

An element that identifies content within its current endpoint without redirecting to another endpoint can return **GUID_NULL** here and expose a nonempty [ElementId](nf-uiautomationcore-irawelementprovidercomponent-get_elementid.md) for lookup within that endpoint.

This property does not register an endpoint. Registration is performed through [IUiaEndpointNotifier::RegisterEndpoint](nf-uiautomationcore-iuiaendpointnotifier-registerendpoint.md).

## -see-also

[IRawElementProviderComponent](nn-uiautomationcore-irawelementprovidercomponent.md)

[IRawElementProviderComponent::get_ElementId](nf-uiautomationcore-irawelementprovidercomponent-get_elementid.md)
