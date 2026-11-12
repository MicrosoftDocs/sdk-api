---
UID: NF:uiautomationcore.IUiaEndpointNotifier.RegisterEndpointHostAsEndpointId
tech.root: WinAuto
title: IUiaEndpointNotifier::RegisterEndpointHostAsEndpointId
ms.date: 11/12/2026
targetos: Windows
description: Associates a UI Automation endpoint with another endpoint that hosts its UI.
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
 - IUiaEndpointNotifier::RegisterEndpointHostAsEndpointId
f1_keywords:
 - IUiaEndpointNotifier::RegisterEndpointHostAsEndpointId
 - uiautomationcore/IUiaEndpointNotifier::RegisterEndpointHostAsEndpointId
dev_langs:
 - c++
helpviewer_keywords:
 - RegisterEndpointHostAsEndpointId
---

# IUiaEndpointNotifier::RegisterEndpointHostAsEndpointId method

## -description

Associates a UI Automation endpoint with another endpoint that hosts its UI.

## -parameters

### -param endpointId [in]

Type: **GUID**

The nonzero GUID identifying the endpoint being hosted.

### -param hostEndpointId [in]

Type: **GUID**

The nonzero GUID identifying the endpoint that hosts the UI of *endpointId*.

## -returns

Returns **S_OK** on success, or an **HRESULT** error code on failure.

Returns **E_INVALIDARG** if either endpoint ID is **GUID_NULL**.

## -remarks

This method supports nested endpoints: one endpoint supplies content within another endpoint rather than directly within a window.

Call [RegisterEndpoint](nf-uiautomationcore-iuiaendpointnotifier-registerendpoint.md) for the hosted endpoint first. The host-side placeholder uses *endpointId* to identify the hosted content.

## -see-also

[IUiaEndpointNotifier](nn-uiautomationcore-iuiaendpointnotifier.md)

[IUiaEndpointNotifier::RegisterEndpointHostAsHwnd](nf-uiautomationcore-iuiaendpointnotifier-registerendpointhostashwnd.md)

[IRawElementProviderComponent](nn-uiautomationcore-irawelementprovidercomponent.md)
