---
UID: NF:uiautomationcore.IUiaEndpointNotifier.RegisterEndpointHostAsCoreWindow
tech.root: WinAuto
title: IUiaEndpointNotifier::RegisterEndpointHostAsCoreWindow
ms.date: 11/12/2026
targetos: Windows
description: Associates a UI Automation endpoint with a CoreWindow host.
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
 - IUiaEndpointNotifier::RegisterEndpointHostAsCoreWindow
f1_keywords:
 - IUiaEndpointNotifier::RegisterEndpointHostAsCoreWindow
 - uiautomationcore/IUiaEndpointNotifier::RegisterEndpointHostAsCoreWindow
dev_langs:
 - c++
helpviewer_keywords:
 - RegisterEndpointHostAsCoreWindow
---

# IUiaEndpointNotifier::RegisterEndpointHostAsCoreWindow method

## -description

Associates a UI Automation endpoint with a CoreWindow host.

## -parameters

### -param endpointId [in]

Type: **GUID**

The nonzero GUID identifying the endpoint.

### -param coreWindow [in]

Type: **IUnknown\***

The [Windows.UI.Core.CoreWindow](/uwp/api/windows.ui.core.corewindow) that hosts the endpoint's UI.

## -returns

Returns **S_OK** on success, or an **HRESULT** error code on failure.

Returns **E_INVALIDARG** if *endpointId* is **GUID_NULL**, or **E_POINTER** if *coreWindow* is **NULL**.

## -remarks

Call [RegisterEndpoint](nf-uiautomationcore-iuiaendpointnotifier-registerendpoint.md) before associating the host.

The public parameter type is **IUnknown\*** to avoid a dependency on Windows Runtime declarations in the interface definition. The object passed must be a **CoreWindow**, not an arbitrary **IUnknown** implementation.

Use [RegisterEndpointHostAsHwnd](nf-uiautomationcore-iuiaendpointnotifier-registerendpointhostashwnd.md) for a host identified by an **HWND**.

## -see-also

[IUiaEndpointNotifier](nn-uiautomationcore-iuiaendpointnotifier.md)

[IUiaEndpointNotifier::RegisterEndpointHostAsEndpointId](nf-uiautomationcore-iuiaendpointnotifier-registerendpointhostasendpointid.md)
