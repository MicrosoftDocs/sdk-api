---
UID: NC:timeprov.AlertSamplesAvailFunc
title: AlertSamplesAvailFunc (timeprov.h)
description: Notifies the system that there are new time samples available.helpviewer_keywords: ["AlertSamplesAvailFunc","AlertSamplesAvailFunc callback","AlertSamplesAvailFunc callback function","_win32_alertsamplesavail","base.alertsamplesavail","timeprov/AlertSamplesAvailFunc"]
old-location: base\alertsamplesavail.htm
tech.root: SysInfo
ms.assetid: f90da019-072e-46c9-8e05-0321a9960968
ms.date: 12/05/2018
ms.keywords: AlertSamplesAvailFunc, AlertSamplesAvailFunc callback, AlertSamplesAvailFunc callback function, _win32_alertsamplesavail, base.alertsamplesavail, timeprov/AlertSamplesAvailFunc
f1_keywords:
- timeprov/AlertSamplesAvailFunc
dev_langs:
- c++
req.header: timeprov.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
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
- Timeprov.h
api_name:
- AlertSamplesAvailFunc
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# AlertSamplesAvailFunc callback function


## -description


Notifies the system that there are new time samples available.


## -parameters




### -param Arg1








## -returns



If the function succeeds, the return value is S_OK. Otherwise, the return value is one of the error codes defined in WinError.h.




## -remarks



The time provider manager uses this notification to determine when to send a TPC_GetSamples command. A hardware provider does not need to call this function, as the time provider manager requests samples without this notification. Time providers that provide samples sporadically, such as a provider that works in the background when a user establishes a transient dial-up connection, must call this function.

The 
<a href="https://docs.microsoft.com/windows/desktop/api/timeprov/nf-timeprov-timeprovopen">TimeProvOpen</a> function returns a pointer to this function.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/timeprov/nf-timeprov-timeprovopen">TimeProvOpen</a>
 

 

