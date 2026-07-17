---
UID: NF:uiautomationcore.IUIAutomationClientInfoSource.RegisterClientConnectionCallback
tech.root: WinAuto
title: IUIAutomationClientInfoSource::RegisterClientConnectionCallback
ms.date: 01/07/2026
targetos: Windows
description: Registers a connection callback.
prerelease: false
req.assembly: 
req.construct-type: function
req.ddi-compliance: 
req.dll: 
req.header: uiautomationcore.h
req.idl: 
req.include-header: 
req.irql: 
req.kmdf-ver: 
req.lib: 
req.max-support: 
req.namespace: 
req.redist: 
req.target-min-winverclnt: Windows build 26100
req.target-min-winversvr: 
req.target-type: 
req.type-library: 
req.umdf-ver: 
req.unicode-ansi: 
topic_type:
 - apiref
api_type:
 - COM
api_location:
 - uiautomationcore.h
api_name:
 - IUIAutomationClientInfoSource::RegisterClientConnectionCallback
f1_keywords:
 - IUIAutomationClientInfoSource::RegisterClientConnectionCallback
 - uiautomationcore/IUIAutomationClientInfoSource::RegisterClientConnectionCallback
dev_langs:
 - c++
helpviewer_keywords:
 - RegisterClientConnectionCallback
---

# RegisterClientConnectionCallback function

## -description

Registers a connection callback.

## -parameters

### -param callback [in]

The callback that is being registered.

### -param handle [out]

A handle to the callback (for later unregistration).

## -returns

S_OK - If the callback was registered successfully.

E_INVALIDARG - If the callback or handle parameter is null.

E_OUTOFMEMORY - If memory allocation for registration failed.

## -remarks

Multiple callbacks can be registered and will be called in order.

The callback interface must remain valid until explicitly unregistered.

Store the returned handle to unregister the callback later.

Callbacks are invoked synchronously on the UIA system thread.

## -see-also

[UnregisterClientConnectionCallback function](nf-uiautomationcore-iuiautomationclientinfosource-unregisterclientconnectioncallback.md)
