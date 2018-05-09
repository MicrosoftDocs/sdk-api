---
UID: NF:appnotify.RegisterAppStateChangeNotification
title: RegisterAppStateChangeNotification function
author: windows-driver-content
description: Enables an app to register a callback function through which it can be notified that its library is going into or coming out of a suspended state.
old-location: shell\RegisterAppStateChangeNotification.htm
old-project: shell
ms.assetid: EE55F783-BF18-49F0-934E-67A252138565
ms.author: windowsdriverdev
ms.date: 5/7/2018
ms.keywords: RegisterAppStateChangeNotification, RegisterAppStateChangeNotification function [Windows Shell], appnotify/RegisterAppStateChangeNotification, shell.RegisterAppStateChangeNotification
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
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
req.typenames: PACKAGE_VERSION
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	twinapi.core.dll
-	API-MS-Win-Core-psm-appnotify-l1-1-0.dll
-	twinapi.AppCore.dll
api_name:
-	RegisterAppStateChangeNotification
product: Windows
targetos: Windows
req.lib: Appnotify.lib
req.dll: Twinapi.core.dll
req.irql: 
---

# RegisterAppStateChangeNotification function


## -description


Enables an app to register a callback function through which it can be notified that its library is going into or coming out of a suspended state. The app can use this information to perform any necessary operations, such as preserving state, that should be performed at that point.


## -parameters




### -param Routine [in]

A pointer to a callback function that is called when the app enters or leaves the suspended state. See <a href="https://msdn.microsoft.com/AA5B09FA-2016-4C9D-8DE3-CD3C6141B45A">PAPPSTATE_CHANGE_ROUTINE</a> for more detail on this function.


### -param Context [in, optional]

App-specific context information that the app uses when going into or out of a suspended state. This is commonly a "this" pointer.


### -param Registration [out]

When this function returns successfully, this parameter receives the address of a pointer to a value that can be used to identify the registration. Store this value to use with <a href="https://msdn.microsoft.com/97D92C75-5C73-4DCF-BE65-2558A1101789">UnregisterAppStateChangeNotification</a>.


## -returns



A standard Win32 status code.




## -see-also




<a href="https://msdn.microsoft.com/97D92C75-5C73-4DCF-BE65-2558A1101789">UnregisterAppStateChangeNotification</a>
 

 

