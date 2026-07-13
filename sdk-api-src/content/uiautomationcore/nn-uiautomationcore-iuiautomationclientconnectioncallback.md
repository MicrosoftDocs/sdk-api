---
UID: NN:uiautomationcore.IUIAutomationClientConnectionCallback
tech.root: WinAuto
title: IUIAutomationClientConnectionCallback
ms.date: 01/07/2026
targetos: Windows
description: Supports the ability to receive synchronous notifications when UI Automation clients connect or disconnect.
prerelease: false
req.assembly: 
req.construct-type: iface
req.ddi-compliance: 
req.header: uiautomationcore.h
req.idl: 
req.include-header: 
req.max-support: 
req.namespace: 
req.redist: 
req.target-min-winverclnt: Windows build 26100
req.target-min-winversvr: 
req.target-type: 
req.unicode-ansi: 
topic_type:
 - apiref
api_type:
 - COM
api_location:
 - uiautomationcore.h
api_name:
 - IUIAutomationClientConnectionCallback
f1_keywords:
 - IUIAutomationClientConnectionCallback
 - uiautomationcore/IUIAutomationClientConnectionCallback
dev_langs:
 - c++
helpviewer_keywords:
 - IUIAutomationClientConnectionCallback
---

# IUIAutomationClientConnectionCallback interface

## -description

Supports the ability to receive synchronous notifications when UI Automation clients connect or disconnect.

## -remarks

Providers implement this interface and register it with [IUIAutomationClientInfoSource](nn-uiautomationcore-iuiautomationclientinfosource.md) to receive notifications when UI Automation clients connect or disconnect.

Methods are invoked synchronously on the UI Automation system thread.

## -see-also
