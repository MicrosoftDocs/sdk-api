---
UID: NF:uiautomationcore.IUiaEndpointNotifier.SetDefaultVisualReferenceId
tech.root: WinAuto
title: IUiaEndpointNotifier::SetDefaultVisualReferenceId
ms.date: 11/12/2026
targetos: Windows
description: Sets the default visual reference used to interpret an endpoint provider's coordinates.
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
 - IUiaEndpointNotifier::SetDefaultVisualReferenceId
f1_keywords:
 - IUiaEndpointNotifier::SetDefaultVisualReferenceId
 - uiautomationcore/IUiaEndpointNotifier::SetDefaultVisualReferenceId
dev_langs:
 - c++
helpviewer_keywords:
 - SetDefaultVisualReferenceId
---

# IUiaEndpointNotifier::SetDefaultVisualReferenceId method

## -description

Sets the default visual reference used to interpret an endpoint provider's coordinates.

## -parameters

### -param endpointId [in]

Type: **GUID**

The nonzero GUID identifying the endpoint.

### -param visualReferenceId [in]

Type: **UINT64**

A nonzero identifier for the host visual reference relative to which the provider reports coordinates. This is a visual reference identifier, not the endpoint GUID or a window handle.

## -returns

Returns **S_OK** on success, or an **HRESULT** error code on failure.

Returns **E_INVALIDARG** if *endpointId* is **GUID_NULL** or *visualReferenceId* is zero.

## -remarks

This method supplies the reference used in hosting environments that transform visual-relative provider coordinates into global screen coordinates. It does not register an endpoint or associate an endpoint with its host.

The visual reference is cleared when the endpoint is unregistered. Do not generate an arbitrary value or cast an **HWND** to obtain a visual reference identifier.

## -see-also

[IUiaEndpointNotifier](nn-uiautomationcore-iuiaendpointnotifier.md)

[IUiaEndpointNotifier::UnregisterEndpoint](nf-uiautomationcore-iuiaendpointnotifier-unregisterendpoint.md)
