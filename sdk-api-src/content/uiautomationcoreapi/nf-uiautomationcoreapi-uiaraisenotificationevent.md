---
UID: NF:uiautomationcoreapi.UiaRaiseNotificationEvent
title: UiaRaiseNotificationEvent function
author: windows-sdk-content
description: Called by providers to initiate a notification event.
old-location: winauto\uiauto_UiaRaiseNotificationEvent.htm
old-project: WinAuto
ms.assetid: E9555BC0-A53B-416F-95C3-53696716F61F
ms.author: windowssdkdev
ms.date: 04/16/2018
ms.keywords: UiaRaiseNotificationEvent, UiaRaiseNotificationEvent function [Windows Accessibility], uiautomationcoreapi/UiaRaiseNotificationEvent, winauto.uiauto_UiaRaiseNotificationEvent
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: uiautomationcoreapi.h
req.include-header: UIAutomation.h
req.target-type: Windows
req.target-min-winverclnt: Windows 10, version 1709 [desktop apps | UWP apps]
req.target-min-winversvr: Windows Server 2016 [desktop apps | UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: 
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	Uiautomationcore.dll
-	Ext-MS-Win-UiaCore-L1-1-3.dll
api_name:
-	UiaRaiseNotificationEvent
product: Windows
targetos: Windows
req.lib: Uiautomationcore.lib
req.dll: Uiautomationcore.dll
req.irql: 
req.product: Windows XP with SP1 and later
---

# UiaRaiseNotificationEvent function


## -description


Called by providers to initiate a notification event.


## -parameters




### -param provider [in]

The provider node where the notification event occurred.


### -param notificationKind

The type of notification.


### -param notificationProcessing

Indicates how to process notifications.


### -param displayString [in, optional]

A string to display in the notification message.


### -param activityId [in]

A unique non-localized string to identify an action or group of actions. Use this to pass additional information to the event handler.


## -returns



If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



