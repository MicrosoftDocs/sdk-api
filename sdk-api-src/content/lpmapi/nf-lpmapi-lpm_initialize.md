---
UID: NF:lpmapi.LPM_Initialize
title: LPM_Initialize function
author: windows-sdk-content
description: The LPM_Initialize function initializes a local policy module (LPM).
old-location: qos\lpm_initialize.htm
old-project: qos
ms.assetid: 00f4ab59-8808-4bcb-8258-5aad113ad2b5
ms.author: windowssdkdev
ms.date: 03/26/2018
ms.keywords: LPM_Initialize, LPM_Initialize callback, LPM_Initialize callback function [QOS], _gqos_lpm_initialize, lpmapi/LPM_Initialize, qos.lpm_initialize
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: lpmapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
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
req.typenames: MC_TIMING_REPORT, *LPMC_TIMING_REPORT
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - Lpmapi.h
api_name:
 - LPM_Initialize
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# LPM_Initialize function


## -description


The 
<i>LPM_Initialize</i> function initializes a local policy module (LPM). This occurs when the Admission Control Service needs to do policy based–admission control, such as when an SBM becomes the Designated Subnet Bandwidth Manager (DSBM). LPMs should initialize themselves, synchronously, before returning.


## -parameters




### -param LpmHandle [in]

Unique handle for the LPM, assigned by the PCM.


### -param pLpmInitInfo [in]

Pointer to an LPM_INIT_INFO structure containing LPM initialization information.


### -param pLpmVersionNumber [out]

Version of LPM being requested.


### -param pSupportedPeType [out]

Valid policy element (PE) type that the LPM uses to make policy based–admission control decisions. Each LPM can only support one PE type, though future versions may allow an LPM to support multiple PE types. Reserved PE types are defined in Lpmapi.h. For more information about policy element types, see 
<a href="https://msdn.microsoft.com/72eeb985-85e2-48c6-b79f-73f48295740a">Policy Elements</a>.

It is possible for a single DLL to support multiple PE types by having the DLL name entered multiple times in the PCM configuration data. Under such circumstances, the PCM will load and call the same LPM_Initialize routine multiple times; it is the LPM's responsibility to return different PE types for these additional calls.

LPMs can return a special PE type, LPM_ALL_PE_TYPES, to indicate that it will make policy based–admission control decisions based on all policy data objects. In this scenario, the PCM will assume that this LPM understands how to generate policy data objects for outgoing messages that the PCM is not able to understand.


### -param Reserved [out]

Reserved for future use.


## -returns



If the LPM is initialized successfully, and a valid PE type is returned in <i>pSupportedPeType</i>, the return value will be LPM_OK. The PCM treats any value other than LPM_OK as an error, and unloads the DLL (LPMs are always implemented as DLLs). If a value other than LPM_OK is returned or <i>pSupportedPeType</i> is invalid, the PCM writes a record to the Event Log and includes the name of the DLL and the returned error value.




## -see-also




<a href="https://msdn.microsoft.com/0bf84c25-312c-4b4a-8bb1-e8f00711dbe3">LPM_AdmitRsvpMsg</a>



<a href="https://msdn.microsoft.com/1ae417e9-3180-4fd4-90f6-6e91c12d523b">LPM_GetRsvpObjects</a>



<a href="https://msdn.microsoft.com/e7b38820-4a7e-4f17-a67d-b94caa9037f5">PALLOCMEM</a>



<a href="https://msdn.microsoft.com/b700b5c1-9fd7-4fc9-a5ed-f8ac75d22037">PFREEMEM</a>
 

 

