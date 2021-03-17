---
UID: NF:powerbase.PowerUnregisterSuspendResumeNotification
title: PowerUnregisterSuspendResumeNotification function (powerbase.h)
description: Cancels a registration to receive notification when the system is suspended or resumed.
helpviewer_keywords: ["PowerUnregisterSuspendResumeNotification","PowerUnregisterSuspendResumeNotification function","base.powerunregistersuspendresumenotification","powerbase/PowerUnregisterSuspendResumeNotification"]
old-location: base\powerunregistersuspendresumenotification.htm
tech.root: base
ms.assetid: 5680e6bd-1694-4d5f-94ea-41b24149c741
ms.date: 12/05/2018
ms.keywords: PowerUnregisterSuspendResumeNotification, PowerUnregisterSuspendResumeNotification function, base.powerunregistersuspendresumenotification, powerbase/PowerUnregisterSuspendResumeNotification
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
req.lib: Powrprof.lib
req.dll: Powrprof.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - PowerUnregisterSuspendResumeNotification
 - powerbase/PowerUnregisterSuspendResumeNotification
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Powrprof.dll
 - API-MS-Win-power-base-l1-1-0.dll
api_name:
 - PowerUnregisterSuspendResumeNotification
---

# PowerUnregisterSuspendResumeNotification function


## -description

Cancels a registration to receive notification when the system is suspended or resumed.

## -parameters

### -param RegistrationHandle [in, out]

A handle to a registration obtained by calling the <a href="/windows/desktop/api/powerbase/nf-powerbase-powerregistersuspendresumenotification">PowerRegisterSuspendResumeNotification</a> function.

## -returns

Returns ERROR_SUCCESS (zero) if the call was successful, and a nonzero value if the call failed.

## -see-also

<a href="/windows/desktop/api/powerbase/nf-powerbase-powerregistersuspendresumenotification">PowerRegisterSuspendResumeNotification</a>