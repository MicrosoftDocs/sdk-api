---
UID: NF:oobenotification.OOBEComplete
title: OOBEComplete function (oobenotification.h)
description: Determines whether OOBE (Windows Welcome) has been completed.
helpviewer_keywords: ["OOBEComplete","isOOBEComplete","isOOBEComplete function","oobenotification/isOOBEComplete","windowssetupandmigration.oobecomplete"]
old-location: windowssetupandmigration\oobecomplete.htm
tech.root: windowssetupandmigration
ms.assetid: D543CD82-9985-49E2-A902-34CB5880B875
ms.date: 12/05/2018
ms.keywords: OOBEComplete, isOOBEComplete, isOOBEComplete function, oobenotification/isOOBEComplete, windowssetupandmigration.oobecomplete
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - OOBEComplete
 - oobenotification/OOBEComplete
dev_langs:
 - c++
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
      <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a> will retrieve extended error 
      information.