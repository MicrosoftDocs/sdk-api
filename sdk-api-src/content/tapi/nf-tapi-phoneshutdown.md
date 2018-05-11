---
UID: NF:tapi.phoneShutdown
title: phoneShutdown function
author: windows-driver-content
description: The phoneShutdown function shuts down the application's usage of TAPI's phone abstraction.
old-location: tapi2\phoneshutdown.htm
old-project: Tapi
ms.assetid: 0cf8bc07-946a-450d-8062-b9e19c22a4c5
ms.author: windowsdriverdev
ms.date: 5/8/2018
ms.keywords: "_tapi2_phoneshutdown, phoneShutdown, phoneShutdown function [TAPI 2.2], tapi/phoneShutdown, tapi2.phoneshutdown"
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: tapi.h
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
req.typenames: FLICK_POINT
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	Tapi32.dll
api_name:
-	phoneShutdown
product: Windows
targetos: Windows
req.lib: Tapi32.lib
req.dll: Tapi32.dll
req.irql: 
req.product: Windows XP with SP1 and later
---

# phoneShutdown function


## -description


The 
<b>phoneShutdown</b> function shuts down the application's usage of TAPI's phone abstraction.


## -parameters




### -param hPhoneApp

Application's usage handle for TAPI.


## -returns



Returns zero if the request succeeds or a negative error number if an error occurs. Possible return values are:

PHONEERR_INVALAPPHANDLE, PHONEERR_NOMEM, PHONEERR_UNINITIALIZED, PHONEERR_RESOURCEUNAVAIL.




## -remarks



If this function is called when the application has open phone devices, these devices are closed.



