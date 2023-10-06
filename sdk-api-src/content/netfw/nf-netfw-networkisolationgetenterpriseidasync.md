---
UID: NF:netfw.NetworkIsolationGetEnterpriseIdAsync
title: NetworkIsolationGetEnterpriseIdAsync function (netfw.h)
description: Gets the Enterprise ID based on Network Isolation endpoints in the context of the Windows Information Protection (WIP) or the Microsoft Defender Application Guard (MDAG) scenarios.
helpviewer_keywords: ["NETISO_GEID_DEFAULT","NETISO_GEID_FORCE_TO_CHECK","NETISO_GEID_FOR_NEUTRAL_AWARE","NETISO_GEID_FOR_WDAG","NetworkIsolationGetEnterpriseIdAsync","NetworkIsolationGetEnterpriseIdAsync function [ICS/ICF]","ics.networkisolationgetenterpriseidasync","netfw/NetworkIsolationGetEnterpriseIdAsync"]
old-location: ics\networkisolationgetenterpriseidasync.htm
tech.root: ics
ms.assetid: 709211F9-FE7A-4C43-AD35-101C4B64ED26
ms.date: 12/05/2018
ms.keywords: NETISO_GEID_DEFAULT, NETISO_GEID_FORCE_TO_CHECK, NETISO_GEID_FOR_NEUTRAL_AWARE, NETISO_GEID_FOR_WDAG, NetworkIsolationGetEnterpriseIdAsync, NetworkIsolationGetEnterpriseIdAsync function [ICS/ICF], ics.networkisolationgetenterpriseidasync, netfw/NetworkIsolationGetEnterpriseIdAsync
req.header: netfw.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10 [desktop apps only]
req.target-min-winversvr: Windows Server 2016 [desktop apps only]
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
req.dll: Firewallapi.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - NetworkIsolationGetEnterpriseIdAsync
 - netfw/NetworkIsolationGetEnterpriseIdAsync
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - firewallapi.dll
api_name:
 - NetworkIsolationGetEnterpriseIdAsync
---

# NetworkIsolationGetEnterpriseIdAsync function

## -description

Gets the Enterprise ID based on Network Isolation endpoints in the context of the Windows Information Protection (WIP) or the Microsoft Defender Application Guard (MDAG) scenarios. If neither WIP nor MDAG are on, the API returns NULL, unless the flag <b>NETISO_GEID_FORCE_TO_CHECK</b> is passed.  The Enterprise ID can be any string different from NULL or “*”.

Example of NetworkIsolationGetEnterpriseIdAsync usage: https://github.com/microsoft/EnterpriseStateClassify

## -parameters

### -param wszServerName [in]

The name of the Enterprise Data Protection Server.

### -param dwFlags [in]

A bitmask value of control flags which specify the context of the API call.  May contain one or more of the following flags.

| Value | Meaning |
| ------ | ------ |
| **NETISO_GEID_DEFAULT**<br/>0x00 | Default API behavior.<br/>Returns the Enterprise ID for Enterprise resources.<br/>Returns NULL for Personal resources.<br/>For Neutral resources, returns Enterprise ID if it is called from an Enterprise context, or returns NULL if it is called from a Personal context. |
| **NETISO_GEID_FOR_WDAG**<br/>0x01 | Used in the context of the Microsoft Defender Application Guard (MDAG) scenario. |
| **NETISO_GEID_FOR_NEUTRAL_AWARE**<br/>0x02 | Used by applications that are aware of neutral resources.<br/>For Neutral resources the API will return L”*”.<br/>For Enterprise resources the API will return the Enterprise ID.<br/>For Personal resources the API will return NULL. |
| **NETISO_GEID_FORCE_TO_CHECK**<br/>0x04 | Forces API to check the resource even in cases when neither Windows Information Protection nor MDAG are enabled. |

### -param context [in, optional]

Optional context pointer.

### -param callback [in]

Function pointer that will be invoked when a notification is ready for delivery.

### -param hOperation [out]

The handle for the Enterprise Data Protection Server endpoints.

## -returns

Returns ERROR_SUCCESS if successful, or an error value otherwise.

## -remarks

> [!NOTE]
> Windows Defender Application Guard (WDAG) is now Microsoft Defender Application Guard (MDAG). The WDAG name is deprecated, but it is still used in some APIs.
