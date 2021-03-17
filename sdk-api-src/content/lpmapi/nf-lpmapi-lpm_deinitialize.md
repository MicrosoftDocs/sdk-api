---
UID: NF:lpmapi.LPM_Deinitialize
title: LPM_Deinitialize function (lpmapi.h)
description: The LPM_Deinitialize function allows the PCM to instruct LPMs to deinitialize, whether due to system shutdown or a change in Designated Subnet Bandwidth Manager (DSBM) status.
helpviewer_keywords: ["LPM_Deinitialize","LPM_Deinitialize callback","LPM_Deinitialize callback function [QOS]","_gqos_lpm_deinitialize","lpmapi/LPM_Deinitialize","qos.lpm_deinitialize"]
old-location: qos\lpm_deinitialize.htm
tech.root: QOS
ms.assetid: d3a1edc5-a3fd-4c49-9cd9-f06ba56fec81
ms.date: 12/05/2018
ms.keywords: LPM_Deinitialize, LPM_Deinitialize callback, LPM_Deinitialize callback function [QOS], _gqos_lpm_deinitialize, lpmapi/LPM_Deinitialize, qos.lpm_deinitialize
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
 - LPM_Deinitialize
 - lpmapi/LPM_Deinitialize
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
 - LPM_Deinitialize
---

# LPM_Deinitialize function


## -description

The 
<i>LPM_Deinitialize</i> function allows the PCM to instruct LPMs to deinitialize, whether due to system shutdown or a change in Designated Subnet Bandwidth Manager (DSBM) status. This occurs when the Admission Control Service no longer needs to do policy based–admission control, such as when a demotion from DSBM status occurs. LPMs should free resources, close connections to external entities such as policy server or directory services, and perform any other cleanup necessary to properly relinquish LPM activities. The PCM will unload the DLL after 
<i>LPM_Deinitialize</i> returns.

## -parameters

### -param LpmHandle

Unique handle to the LPM, as supplied through 
<a href="/previous-versions/windows/desktop/api/lpmapi/nf-lpmapi-lpm_initialize">LPM_Initialize</a> during initialization.

## -returns

If another value is returned from 
<i>LPM_Deinitialize</i>, the PCM will record the name of this DLL (implementations of LPMs are always in the form of a DLL), as well as this return value, in the Event Log.

## -remarks

LPMs do not need to return errors for outstanding requests when 
<i>LPM_Deinitialize</i> is called; PCM assumes LPV_REJECT for outstanding requests. LPMs should deinitialize synchronously before returning. If an LPM has been loaded and initialized multiple times to facilitate the handling of multiple PE types, the PCM will call 
<i>LPM_Deinitialize</i> multiple times as well.

## -see-also

<a href="/previous-versions/windows/desktop/api/lpmapi/nf-lpmapi-lpm_initialize">LPM_Initialize</a>