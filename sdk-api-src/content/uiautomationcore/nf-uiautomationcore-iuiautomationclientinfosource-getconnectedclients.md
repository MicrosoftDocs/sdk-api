---
UID: NF:uiautomationcore.IUIAutomationClientInfoSource.GetConnectedClients
tech.root: WinAuto
title: IUIAutomationClientInfoSource::GetConnectedClients
ms.date: 01/07/2026
targetos: Windows
description: Retrieves information about currently connected UI Automation clients.
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
 - IUIAutomationClientInfoSource::GetConnectedClients
f1_keywords:
 - IUIAutomationClientInfoSource::GetConnectedClients
 - uiautomationcore/IUIAutomationClientInfoSource::GetConnectedClients
dev_langs:
 - c++
helpviewer_keywords:
 - GetConnectedClients
---

# GetConnectedClients function

## -description

Retrieves information about currently connected UI Automation clients.

## -parameters

### -param clients [out, retval]

A SAFEARRAY of [IUIAutomationClientInfo](nn-uiautomationcore-iuiautomationclientinfo.md) interface pointers.

## -returns

S_OK - If the UI Automation client information was retrieved successfully or the *clients* SAFEARRAY is empty (no clients connected).

E_INVALIDARG - If *clients* is null.

E_OUTOFMEMORY - If memory allocation for the client array failed.

## -remarks

Caller must destroy the SAFEARRAY using the [SafeArrayDestroy function](../oleauto/nf-oleauto-safearraydestroy.md).

The returned interfaces provide a snapshot at the time of the call.

Client connections may change between calls to this method.

## -see-also
