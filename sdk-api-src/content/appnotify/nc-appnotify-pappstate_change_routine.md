---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
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
---

# PAPPSTATE_CHANGE_ROUTINE callback function


## -description


Specifies an app-defined callback function that notifies the app when the app is entering or leaving a suspended state.


## -parameters




### -param Quiesced


### -param Context [in]

Type: <b>PVOID</b>

A pointer to data that the app can save when suspending and use upon resuming. This value is supplied by the <a href="https://msdn.microsoft.com/EE55F783-BF18-49F0-934E-67A252138565">RegisterAppStateChangeNotification</a> function. This is commonly a "this" pointer.


#### - Suspended [in]

Type: <b>BOOLEAN</b>

<b>TRUE</b> if the app is entering the suspended state; <b>FALSE</b> if the app is leaving the suspended state.


## -returns



This function pointer does not return a value.



