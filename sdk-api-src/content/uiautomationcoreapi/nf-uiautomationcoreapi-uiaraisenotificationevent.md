---
UID: NF:uiautomationcoreapi.UiaRaiseNotificationEvent
title: UiaRaiseNotificationEvent function (uiautomationcoreapi.h)
description: Called by providers to initiate a notification event.
helpviewer_keywords: ["UiaRaiseNotificationEvent","UiaRaiseNotificationEvent function [Windows Accessibility]","uiautomationcoreapi/UiaRaiseNotificationEvent","winauto.uiauto_UiaRaiseNotificationEvent"]
old-location: winauto\uiauto_UiaRaiseNotificationEvent.htm
tech.root: WinAuto
ms.assetid: E9555BC0-A53B-416F-95C3-53696716F61F
ms.date: 12/05/2018
ms.keywords: UiaRaiseNotificationEvent, UiaRaiseNotificationEvent function [Windows Accessibility], uiautomationcoreapi/UiaRaiseNotificationEvent, winauto.uiauto_UiaRaiseNotificationEvent
req.header: uiautomationcoreapi.h
req.include-header: UIAutomation.h
req.target-type: Windows
req.target-min-winverclnt: Windows 10, version 1709 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2016 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Uiautomationcore.lib
req.dll: Uiautomationcore.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - UiaRaiseNotificationEvent
 - uiautomationcoreapi/UiaRaiseNotificationEvent
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Uiautomationcore.dll
 - Ext-MS-Win-UiaCore-L1-1-3.dll
api_name:
 - UiaRaiseNotificationEvent
---

# UiaRaiseNotificationEvent function

## -description

Called by providers to initiate a notification event.

## -parameters

### -param provider [in]

The provider node where the notification event occurred.

### -param notificationKind

The type of notification, as a [NotificationKind enumeration](../uiautomationcore/ne-uiautomationcore-notificationkind.md) value.

### -param notificationProcessing

The preferred way to process a notification, as a [NotificationProcessing enumeration](../uiautomationcore/ne-uiautomationcore-notificationprocessing.md) value.

### -param displayString [in, optional]

A string to display in the notification message.

### -param activityId [in]

A unique non-localized string to identify an action or group of actions. Use this to pass additional information to the event handler.

## -returns

If this function succeeds, it returns S_OK. Otherwise, it returns an HRESULT error code.

## -remarks

If your window uses the [`WS_POPUP`](/windows/win32/winmsg/window-styles) style, it must also implement the [Window Control Pattern](/windows/win32/winauto/uiauto-implementingwindow) and handle the [WM_GETOBJECT](/windows/win32/winauto/wm-getobject) message (see [How to Expose a Server-Side UI Automation Provider](/windows/win32/winauto/uiauto-howto-expose-serverside-uiautomation-provider) for more details).
