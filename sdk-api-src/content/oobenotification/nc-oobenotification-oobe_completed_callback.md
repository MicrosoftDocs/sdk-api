---
UID: NC:oobenotification.OOBE_COMPLETED_CALLBACK
title: OOBE_COMPLETED_CALLBACK
author: windows-sdk-content
description: Application-defined callback function used with the RegisterWaitUntilOOBECompleted function.
old-location: windowssetupandmigration\oobe_completed_callback.htm
old-project: WNF
ms.assetid: 9786D6C3-82B1-4546-9BE9-7705AD3B7DBD
ms.author: windowssdkdev
ms.date: 02/15/2018
ms.keywords: OOBE_COMPLETED_CALLBACK, OOBE_COMPLETED_CALLBACK callback, OOBE_COMPLETED_CALLBACK callback function, oobenotification/OOBE_COMPLETED_CALLBACK, windowssetupandmigration.oobe_completed_callback
ms.prod: windows
ms.technology: windows-sdk
ms.topic: callback
req.header: oobenotification.h
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
req.typenames: NET_INTERFACE_CONTEXT_TABLE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - Oobenotification.h
api_name:
 - OOBE_COMPLETED_CALLBACK
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: ADAM
---

# OOBE_COMPLETED_CALLBACK callback function


## -description


Application-defined callback function used with the <a href="https://msdn.microsoft.com/D1581B09-06A7-483F-929D-1AF93832942D">RegisterWaitUntilOOBECompleted</a> function.


## -parameters




### -param CallbackContext

Pointer to the callback context. This is the value passed to the <a href="https://msdn.microsoft.com/D1581B09-06A7-483F-929D-1AF93832942D">RegisterWaitUntilOOBECompleted</a> function as the <i>CallbackContext</i> parameter.


## -returns



This callback function does not return a value.




## -remarks



Once the callback function has completed, <a href="https://msdn.microsoft.com/966803DF-744A-430F-86C0-F6ACA754C603">UnregisterWaitUntilOOBECompleted</a> should be called.



