---
UID: NC:appnotify.PAPPSTATE_CHANGE_ROUTINE
title: PAPPSTATE_CHANGE_ROUTINE (appnotify.h)
description: Specifies an app-defined callback function that notifies the app when the app is entering or leaving a suspended state.
helpviewer_keywords: ["PAPPSTATE_CHANGE_ROUTINE","PAPPSTATE_CHANGE_ROUTINE function","PAPPSTATE_CHANGE_ROUTINE function pointer [Windows Shell]","appnotify/PAPPSTATE_CHANGE_ROUTINE","shell.PAPPSTATE_CHANGE_ROUTINE"]
old-location: shell\PAPPSTATE_CHANGE_ROUTINE.htm
tech.root: shell
ms.assetid: AA5B09FA-2016-4C9D-8DE3-CD3C6141B45A
ms.date: 12/05/2018
ms.keywords: PAPPSTATE_CHANGE_ROUTINE, PAPPSTATE_CHANGE_ROUTINE function, PAPPSTATE_CHANGE_ROUTINE function pointer [Windows Shell], appnotify/PAPPSTATE_CHANGE_ROUTINE, shell.PAPPSTATE_CHANGE_ROUTINE
f1_keywords:
- appnotify/PAPPSTATE_CHANGE_ROUTINE
dev_langs:
- c++
req.header: appnotify.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8.1 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- UserDefined
api_location:
- appnotify.h
api_name:
- PAPPSTATE_CHANGE_ROUTINE
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# PAPPSTATE_CHANGE_ROUTINE callback function


## -description


Specifies an app-defined callback function that notifies the app when the app is entering or leaving a suspended state.


## -parameters




### -param Quiesced


### -param Context [in]

Type: <b>PVOID</b>

A pointer to data that the app can save when suspending and use upon resuming. This value is supplied by the <a href="https://docs.microsoft.com/windows/desktop/api/appnotify/nf-appnotify-registerappstatechangenotification">RegisterAppStateChangeNotification</a> function. This is commonly a "this" pointer.


#### - Suspended [in]

Type: <b>BOOLEAN</b>

<b>TRUE</b> if the app is entering the suspended state; <b>FALSE</b> if the app is leaving the suspended state.


