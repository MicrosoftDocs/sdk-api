---
UID: NF:appnotify.UnregisterAppStateChangeNotification
title: UnregisterAppStateChangeNotification function
author: windows-sdk-content
description: Cancels a change notification registered through RegisterAppStateChangeNotification.
old-location: shell\UnregisterAppStateChangeNotification.htm
old-project: shell
ms.assetid: 97D92C75-5C73-4DCF-BE65-2558A1101789
ms.author: windowssdkdev
ms.date: 06/04/2018
ms.keywords: UnregisterAppStateChangeNotification, UnregisterAppStateChangeNotification function [Windows Shell], appnotify/UnregisterAppStateChangeNotification, shell.UnregisterAppStateChangeNotification
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: PACKAGE_VERSION
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - twinapi.core.dll
 - API-MS-Win-Core-psm-appnotify-l1-1-0.dll
 - twinapi.AppCore.dll
api_name:
 - UnregisterAppStateChangeNotification
product: Windows
targetos: Windows
req.lib: Appnotify.lib
req.dll: Twinapi.core.dll
req.irql: 
---

# UnregisterAppStateChangeNotification function


## -description


Cancels a change notification registered through <a href="https://msdn.microsoft.com/EE55F783-BF18-49F0-934E-67A252138565">RegisterAppStateChangeNotification</a>.


## -parameters




### -param Registration [in, out]

A pointer to the registration handle retrieved by <a href="https://msdn.microsoft.com/EE55F783-BF18-49F0-934E-67A252138565">RegisterAppStateChangeNotification</a> through its <i>Registration</i> parameter.


## -returns



This function does not return a value.




## -see-also




<a href="https://msdn.microsoft.com/EE55F783-BF18-49F0-934E-67A252138565">RegisterAppStateChangeNotification</a>
 

 

