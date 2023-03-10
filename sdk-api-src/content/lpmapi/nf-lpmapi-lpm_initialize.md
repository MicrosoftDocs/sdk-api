---
UID: NF:lpmapi.LPM_Initialize
title: LPM_Initialize function (lpmapi.h)
description: The LPM_Initialize function initializes a local policy module (LPM).
helpviewer_keywords: ["LPM_Initialize","LPM_Initialize callback","LPM_Initialize callback function [QOS]","_gqos_lpm_initialize","lpmapi/LPM_Initialize","qos.lpm_initialize"]
old-location: qos\lpm_initialize.htm
tech.root: QOS
ms.assetid: 00f4ab59-8808-4bcb-8258-5aad113ad2b5
ms.date: 12/05/2018
ms.keywords: LPM_Initialize, LPM_Initialize callback, LPM_Initialize callback function [QOS], _gqos_lpm_initialize, lpmapi/LPM_Initialize, qos.lpm_initialize
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - LPM_Initialize
 - lpmapi/LPM_Initialize
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - Lpmapi.h
api_name:
 - LPM_Initialize
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
<a href="/previous-versions/windows/desktop/qos/policy-elements">Policy Elements</a>.

It is possible for a single DLL to support multiple PE types by having the DLL name entered multiple times in the PCM configuration data. Under such circumstances, the PCM will load and call the same LPM_Initialize routine multiple times; it is the LPM's responsibility to return different PE types for these additional calls.

LPMs can return a special PE type, LPM_ALL_PE_TYPES, to indicate that it will make policy based–admission control decisions based on all policy data objects. In this scenario, the PCM will assume that this LPM understands how to generate policy data objects for outgoing messages that the PCM is not able to understand.

### -param Reserved [out]

Reserved for future use.

## -returns

If the LPM is initialized successfully, and a valid PE type is returned in <i>pSupportedPeType</i>, the return value will be LPM_OK. The PCM treats any value other than LPM_OK as an error, and unloads the DLL (LPMs are always implemented as DLLs). If a value other than LPM_OK is returned or <i>pSupportedPeType</i> is invalid, the PCM writes a record to the Event Log and includes the name of the DLL and the returned error value.

## -see-also

<a href="/previous-versions/windows/desktop/api/lpmapi/nf-lpmapi-lpm_admitrsvpmsg">LPM_AdmitRsvpMsg</a>



<a href="/previous-versions/windows/desktop/api/lpmapi/nf-lpmapi-lpm_getrsvpobjects">LPM_GetRsvpObjects</a>



<a href="/previous-versions/windows/desktop/api/lpmapi/nc-lpmapi-pallocmem">PALLOCMEM</a>



<a href="/previous-versions/windows/desktop/api/lpmapi/nc-lpmapi-pfreemem">PFREEMEM</a>