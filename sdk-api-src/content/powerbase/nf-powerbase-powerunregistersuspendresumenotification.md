---
UID: NF:powerbase.PowerUnregisterSuspendResumeNotification
title: PowerUnregisterSuspendResumeNotification function
author: windows-driver-content
description: Cancels a registration to receive notification when the system is suspended or resumed.
old-location: base\powerunregistersuspendresumenotification.htm
old-project: Power
ms.assetid: 5680e6bd-1694-4d5f-94ea-41b24149c741
ms.author: windowsdriverdev
ms.date: 3/27/2018
ms.keywords: PowerUnregisterSuspendResumeNotification, PowerUnregisterSuspendResumeNotification function, base.powerunregistersuspendresumenotification, powerbase/PowerUnregisterSuspendResumeNotification
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: powerbase.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: PNRPINFO_V2, *PPNRPINFO_V2
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	Powrprof.dll
-	API-MS-Win-power-base-l1-1-0.dll
api_name:
-	PowerUnregisterSuspendResumeNotification
product: Windows
targetos: Windows
req.lib: Powrprof.lib
req.dll: Powrprof.dll
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# PowerUnregisterSuspendResumeNotification function


## -description


Cancels a registration to receive notification when the system is suspended or resumed.


## -parameters




### -param RegistrationHandle [in, out]

A handle to a registration obtained by calling the <a href="https://msdn.microsoft.com/3b39ec3a-417c-4ce4-a581-ed967f1baec9">PowerRegisterSuspendResumeNotification</a> function.


## -returns



Returns ERROR_SUCCESS (zero) if the call was successful, and a nonzero value if the call failed.




## -see-also




<a href="https://msdn.microsoft.com/3b39ec3a-417c-4ce4-a581-ed967f1baec9">PowerRegisterSuspendResumeNotification</a>
 

 

