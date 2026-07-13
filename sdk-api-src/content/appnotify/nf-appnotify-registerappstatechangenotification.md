---
UID: NF:appnotify.RegisterAppStateChangeNotification
title: RegisterAppStateChangeNotification function (appnotify.h)
description: Enables an app to register a callback function through which it can be notified that its library is going into or coming out of a suspended state.
helpviewer_keywords: ["RegisterAppStateChangeNotification","RegisterAppStateChangeNotification function [Windows Shell]","appnotify/RegisterAppStateChangeNotification","shell.RegisterAppStateChangeNotification"]
old-location: shell\RegisterAppStateChangeNotification.htm
tech.root: shell
ms.assetid: EE55F783-BF18-49F0-934E-67A252138565
ms.date: 12/05/2018
ms.keywords: RegisterAppStateChangeNotification, RegisterAppStateChangeNotification function [Windows Shell], appnotify/RegisterAppStateChangeNotification, shell.RegisterAppStateChangeNotification
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
 - RegisterAppStateChangeNotification
 - appnotify/RegisterAppStateChangeNotification
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
 - RegisterAppStateChangeNotification
---

# RegisterAppStateChangeNotification function


## -description

Enables an app to register a callback function through which it can be notified that its library is going into or coming out of a suspended state. The app can use this information to perform any necessary operations, such as preserving state, that should be performed at that point.

## -parameters

### -param Routine [in]

A pointer to a callback function that is called when the app enters or leaves the suspended state. See <a href="/windows/desktop/api/appnotify/nc-appnotify-pappstate_change_routine">PAPPSTATE_CHANGE_ROUTINE</a> for more detail on this function.

### -param Context [in, optional]

App-specific context information that the app uses when going into or out of a suspended state. This is commonly a "this" pointer.

### -param Registration [out]

When this function returns successfully, this parameter receives the address of a pointer to a value that can be used to identify the registration. Store this value to use with <a href="/windows/desktop/api/appnotify/nf-appnotify-unregisterappstatechangenotification">UnregisterAppStateChangeNotification</a>.

## -returns

A standard Win32 status code.

## -see-also

<a href="/windows/desktop/api/appnotify/nf-appnotify-unregisterappstatechangenotification">UnregisterAppStateChangeNotification</a>