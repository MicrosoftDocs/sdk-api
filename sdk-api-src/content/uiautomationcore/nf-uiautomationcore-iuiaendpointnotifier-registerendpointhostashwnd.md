---
UID: NF:uiautomationcore.IUiaEndpointNotifier.RegisterEndpointHostAsHwnd
tech.root: WinAuto
title: IUiaEndpointNotifier::RegisterEndpointHostAsHwnd
ms.date: 11/12/2026
targetos: Windows
description: Associates a UI Automation endpoint with its host window.
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
 - IUiaEndpointNotifier::RegisterEndpointHostAsHwnd
f1_keywords:
 - IUiaEndpointNotifier::RegisterEndpointHostAsHwnd
 - uiautomationcore/IUiaEndpointNotifier::RegisterEndpointHostAsHwnd
dev_langs:
 - c++
helpviewer_keywords:
 - RegisterEndpointHostAsHwnd
---

# IUiaEndpointNotifier::RegisterEndpointHostAsHwnd method

## -description

Associates a UI Automation endpoint with its host window.

## -parameters

### -param endpointId [in]

Type: **GUID**

The nonzero GUID identifying the endpoint.

### -param hostHwnd [in]

Type: **HWND**

The handle of the window that visually contains the endpoint's UI. This window can belong to another process.

## -returns

Returns **S_OK** on success, or an **HRESULT** error code on failure.

Returns **E_INVALIDARG** if *endpointId* is **GUID_NULL** or *hostHwnd* is **NULL**.

## -remarks

Call [RegisterEndpoint](nf-uiautomationcore-iuiaendpointnotifier-registerendpoint.md) first. Use the same endpoint ID in this association and in the host-side [IRawElementProviderComponent](nn-uiautomationcore-irawelementprovidercomponent.md) placeholder.

UI Automation uses the association to integrate the endpoint's tree into the host window's tree and to resolve navigation back to the host.

## -see-also

[IUiaEndpointNotifier](nn-uiautomationcore-iuiaendpointnotifier.md)

[IUiaEndpointNotifier::RegisterEndpointHostAsCoreWindow](nf-uiautomationcore-iuiaendpointnotifier-registerendpointhostascorewindow.md)

[IUiaEndpointNotifier::RegisterEndpointHostAsEndpointId](nf-uiautomationcore-iuiaendpointnotifier-registerendpointhostasendpointid.md)
