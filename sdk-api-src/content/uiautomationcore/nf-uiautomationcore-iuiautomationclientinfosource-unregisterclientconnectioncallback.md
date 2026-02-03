---
UID: NF:uiautomationcore.IUIAutomationClientInfoSource.UnregisterClientConnectionCallback
tech.root: WinAuto
title: IUIAutomationClientInfoSource::UnregisterClientConnectionCallback
ms.date: 01/07/2026
targetos: Windows
description: Unregisters a previously registered connection callback.
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
 - IUIAutomationClientInfoSource::UnregisterClientConnectionCallback
f1_keywords:
 - IUIAutomationClientInfoSource::UnregisterClientConnectionCallback
 - uiautomationcore/IUIAutomationClientInfoSource::UnregisterClientConnectionCallback
dev_langs:
 - c++
helpviewer_keywords:
 - UnregisterClientConnectionCallback
---

# UnregisterClientConnectionCallback function

## -description

Unregisters a previously registered connection callback.

## -parameters

### -param handle [in]

A handle to the previously registered callback.

## -returns

S_OK - If the callback is unregistered successfully.

S_FALSE - If the *handle* is not found (callback may have already been unregistered).

E_INVALIDARG - If the handle value is invalid.

## -remarks

Safe to call multiple times with the same handle.

After successful unregistration, the callback will no longer be invoked.

The callback interface can be released after successful unregistration.

## -see-also

[RegisterClientConnectionCallback](nf-uiautomationcore-iuiautomationclientinfosource-registerclientconnectioncallback.md)
