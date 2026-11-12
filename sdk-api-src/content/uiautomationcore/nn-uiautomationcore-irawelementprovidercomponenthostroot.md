---
UID: NN:uiautomationcore.IRawElementProviderComponentHostRoot
tech.root: WinAuto
title: IRawElementProviderComponentHostRoot
ms.date: 11/12/2026
targetos: Windows
description: Resolves an endpoint ID to the host-side fragment that parents the endpoint's provider tree.
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
 - IRawElementProviderComponentHostRoot
f1_keywords:
 - IRawElementProviderComponentHostRoot
 - uiautomationcore/IRawElementProviderComponentHostRoot
dev_langs:
 - c++
helpviewer_keywords:
 - IRawElementProviderComponentHostRoot
---

# IRawElementProviderComponentHostRoot interface

## -description

Resolves an endpoint ID to the host-side fragment that parents the endpoint's provider tree.

## -inheritance

The **IRawElementProviderComponentHostRoot** interface inherits from [IUnknown](/windows/win32/api/unknwn/nn-unknwn-iunknown).

## -remarks

Implement this interface on the host's root provider. When UI Automation navigates upward from an endpoint's tree, it calls [GetComponentHostElement](nf-uiautomationcore-irawelementprovidercomponenthostroot-getcomponenthostelement.md) to locate the corresponding host-side parent.

This complements [IRawElementProviderComponent](nn-uiautomationcore-irawelementprovidercomponent.md), which identifies the endpoint when navigation proceeds from the host into its hosted content.

## -see-also

[IRawElementProviderComponent](nn-uiautomationcore-irawelementprovidercomponent.md)

[IUIAutomationProviderApi::UiaHostProviderFromEndpoint](nf-uiautomationcore-iuiautomationproviderapi-uiahostproviderfromendpoint.md)
