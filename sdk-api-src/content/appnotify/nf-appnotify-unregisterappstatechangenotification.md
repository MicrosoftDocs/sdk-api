---
UID: NF:appnotify.UnregisterAppStateChangeNotification
title: UnregisterAppStateChangeNotification function (appnotify.h)
description: Cancels a change notification registered through RegisterAppStateChangeNotification.
helpviewer_keywords: ["UnregisterAppStateChangeNotification","UnregisterAppStateChangeNotification function [Windows Shell]","appnotify/UnregisterAppStateChangeNotification","shell.UnregisterAppStateChangeNotification"]
old-location: shell\UnregisterAppStateChangeNotification.htm
tech.root: shell
ms.assetid: 97D92C75-5C73-4DCF-BE65-2558A1101789
ms.date: 12/05/2018
ms.keywords: UnregisterAppStateChangeNotification, UnregisterAppStateChangeNotification function [Windows Shell], appnotify/UnregisterAppStateChangeNotification, shell.UnregisterAppStateChangeNotification
req.header: appnotify.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Appnotify.lib
req.dll: Twinapi.core.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - UnregisterAppStateChangeNotification
 - appnotify/UnregisterAppStateChangeNotification
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - api-ms-win-core-psm-appnotify-l1-1-1.dll
 - twinapi.core.dll
 - API-MS-Win-Core-psm-appnotify-l1-1-0.dll
 - twinapi.AppCore.dll
api_name:
 - UnregisterAppStateChangeNotification
---

# UnregisterAppStateChangeNotification function


## -description

Cancels a change notification registered through <a href="/windows/desktop/api/appnotify/nf-appnotify-registerappstatechangenotification">RegisterAppStateChangeNotification</a>.

## -parameters

### -param Registration [in, out]

A pointer to the registration handle retrieved by <a href="/windows/desktop/api/appnotify/nf-appnotify-registerappstatechangenotification">RegisterAppStateChangeNotification</a> through its <i>Registration</i> parameter.

## -returns

This function does not return a value.

## -see-also

<a href="/windows/desktop/api/appnotify/nf-appnotify-registerappstatechangenotification">RegisterAppStateChangeNotification</a>