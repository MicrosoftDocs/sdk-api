---
UID: NF:oobenotification.OOBEComplete
title: OOBEComplete function
author: windows-sdk-content
description: Determines whether OOBE (Windows Welcome) has been completed.
old-location: windowssetupandmigration\oobecomplete.htm
tech.root: WNF
ms.assetid: D543CD82-9985-49E2-A902-34CB5880B875
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: OOBEComplete, isOOBEComplete, isOOBEComplete function, oobenotification/isOOBEComplete, windowssetupandmigration.oobecomplete
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
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
req.lib: Kernel32.lib
req.dll: Kernel32.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Kernel32.dll
 - API-MS-Win-OOBE-Notification-L1-1-0.dll
 - Kernel32Legacy.dll
api_name:
 - isOOBEComplete
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- 
: 
- OOBEComplete
: 
---

# OOBEComplete function


## -description


Determines whether OOBE (Windows Welcome) has been completed.


## -parameters




### -param isOOBEComplete [out]

Pointer to a variable that will receive the completion of OOBE upon success.


## -returns



<b>TRUE</b> if the OOBE completion state was successfully set. Otherwise, 
      <b>FALSE</b> if OOBE completion state was not set. If <b>FALSE</b>, 
      <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a> will retrieve extended error 
      information.



