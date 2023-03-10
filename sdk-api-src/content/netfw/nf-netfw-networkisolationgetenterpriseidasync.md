---
UID: NF:netfw.NetworkIsolationGetEnterpriseIdAsync
title: NetworkIsolationGetEnterpriseIdAsync function (netfw.h)
description: Gets the Enterprise ID based on Network Isolation endpoints in the context of the Windows Information Protection (WIP) or the Windows Defender Application Guard (WDAG) scenarios.
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

Gets the Enterprise ID based on Network Isolation endpoints in the context of the Windows Information Protection (WIP) or the Windows Defender Application Guard (WDAG) scenarios. If neither WIP nor WDAG are on, the API returns NULL, unless the flag <b>NETISO_GEID_FORCE_TO_CHECK</b> is passed.  The Enterprise ID can be any string different from NULL or “*”.

Example of NetworkIsolationGetEnterpriseIdAsync usage: https://github.com/microsoft/EnterpriseStateClassify

## -parameters

### -param wszServerName [in]

The name of the Enterprise Data Protection Server.

### -param dwFlags [in]

A bitmask value of control flags which specify the context of the API call.  May contain one or more of the following flags.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="NETISO_GEID_DEFAULT"></a><a id="netiso_geid_default"></a><dl>
<dt><b>NETISO_GEID_DEFAULT</b></dt>
<dt>0x00</dt>
</dl>
</td>
<td width="60%">
Default API behavior.
Returns the Enterprise ID for Enterprise resources.
Returns NULL for Personal resources.
For Neutral resources, returns Enterprise ID if it is called from an Enterprise context, or returns NULL if it is called from a Personal context.


</td>
</tr>
<tr>
<td width="40%"><a id="NETISO_GEID_FOR_WDAG"></a><a id="netiso_geid_for_wdag"></a><dl>
<dt><b>NETISO_GEID_FOR_WDAG</b></dt>
<dt>0x01</dt>
</dl>
</td>
<td width="60%">
Used in the context of the Windows Defender Application Guard (WDAG) scenario.

</td>
</tr>
<tr>
<td width="40%"><a id="NETISO_GEID_FOR_NEUTRAL_AWARE"></a><a id="netiso_geid_for_neutral_aware"></a><dl>
<dt><b>NETISO_GEID_FOR_NEUTRAL_AWARE</b></dt>
<dt>0x02</dt>
</dl>
</td>
<td width="60%">
Used by applications that are aware of neutral resources.
For Neutral resources the API will return L”*”.
For Enterprise resources the API will return the Enterprise ID.
For Personal resources the API will return NULL.

</td>
</tr>
<tr>
<td width="40%"><a id="NETISO_GEID_FORCE_TO_CHECK"></a><a id="netiso_geid_force_to_check"></a><dl>
<dt><b>NETISO_GEID_FORCE_TO_CHECK</b></dt>
<dt>0x04</dt>
</dl>
</td>
<td width="60%">
Forces API to check the resource even in cases when neither Windows Information Protection nor Windows Defender Application Guard are enabled.

</td>
</tr>
</table>

### -param context [in, optional]

Optional context pointer.

### -param callback [in]

Function pointer that will be invoked when a notification is ready for delivery.

### -param hOperation [out]

The handle for the Enterprise Data Protection Server endpoints.

## -returns

Returns ERROR_SUCCESS if successful, or an error value otherwise.

