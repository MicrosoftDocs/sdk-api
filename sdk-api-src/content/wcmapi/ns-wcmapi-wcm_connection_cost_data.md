---
UID: NS:wcmapi._WCM_CONNECTION_COST_DATA
title: WCM_CONNECTION_COST_DATA (wcmapi.h)
description: Specifies information about a connection cost.
helpviewer_keywords: ["*PWCM_CONNECTION_COST_DATA","PWCM_CONNECTION_COST_DATA","PWCM_CONNECTION_COST_DATA structure pointer [Windows Connection Manager]","WCM_CONNECTION_COST_CONGESTED","WCM_CONNECTION_COST_DATA","WCM_CONNECTION_COST_DATA structure [Windows Connection Manager]","WCM_CONNECTION_COST_FIXED","WCM_CONNECTION_COST_OVERDATALIMIT","WCM_CONNECTION_COST_ROAMING","WCM_CONNECTION_COST_UNKNOWN","WCM_CONNECTION_COST_UNRESTRICTED","WCM_CONNECTION_COST_VARIABLE","wcm.wcm_connection_cost_data","wcmapi/PWCM_CONNECTION_COST_DATA","wcmapi/WCM_CONNECTION_COST_DATA"]
old-location: wcm\wcm_connection_cost_data.htm
tech.root: wcm
ms.assetid: 18fcc708-74b1-408f-a7ee-64455742324d
ms.date: 12/05/2018
ms.keywords: '*PWCM_CONNECTION_COST_DATA, PWCM_CONNECTION_COST_DATA, PWCM_CONNECTION_COST_DATA structure pointer [Windows Connection Manager], WCM_CONNECTION_COST_CONGESTED, WCM_CONNECTION_COST_DATA, WCM_CONNECTION_COST_DATA structure [Windows Connection Manager], WCM_CONNECTION_COST_FIXED, WCM_CONNECTION_COST_OVERDATALIMIT, WCM_CONNECTION_COST_ROAMING, WCM_CONNECTION_COST_UNKNOWN, WCM_CONNECTION_COST_UNRESTRICTED, WCM_CONNECTION_COST_VARIABLE, wcm.wcm_connection_cost_data, wcmapi/PWCM_CONNECTION_COST_DATA, wcmapi/WCM_CONNECTION_COST_DATA'
req.header: wcmapi.h
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: WCM_CONNECTION_COST_DATA, *PWCM_CONNECTION_COST_DATA
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _WCM_CONNECTION_COST_DATA
 - wcmapi/_WCM_CONNECTION_COST_DATA
 - PWCM_CONNECTION_COST_DATA
 - wcmapi/PWCM_CONNECTION_COST_DATA
 - WCM_CONNECTION_COST_DATA
 - wcmapi/WCM_CONNECTION_COST_DATA
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Wcmapi.h
api_name:
 - WCM_CONNECTION_COST_DATA
---

# WCM_CONNECTION_COST_DATA structure


## -description

The <b>WCM_CONNECTION_COST_DATA</b> structure specifies information about a connection cost.

## -struct-fields

### -field ConnectionCost

Type: <b>DWORD</b>

Specifies the connection cost type.


This must include one (and only one) of the following flags:



<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="WCM_CONNECTION_COST_UNKNOWN"></a><a id="wcm_connection_cost_unknown"></a><dl>
<dt><b>WCM_CONNECTION_COST_UNKNOWN</b></dt>
<dt>0x0</dt>
</dl>
</td>
<td width="60%">
Connection cost information is not available.

</td>
</tr>
<tr>
<td width="40%"><a id="WCM_CONNECTION_COST_UNRESTRICTED"></a><a id="wcm_connection_cost_unrestricted"></a><dl>
<dt><b>WCM_CONNECTION_COST_UNRESTRICTED</b></dt>
<dt>0x1</dt>
</dl>
</td>
<td width="60%">
The connection is unlimited and has unrestricted usage constraints.

</td>
</tr>
<tr>
<td width="40%"><a id="WCM_CONNECTION_COST_FIXED"></a><a id="wcm_connection_cost_fixed"></a><dl>
<dt><b>WCM_CONNECTION_COST_FIXED</b></dt>
<dt>0x2</dt>
</dl>
</td>
<td width="60%">
Usage counts toward a fixed allotment of data which the user has already paid for (or agreed to pay for).

</td>
</tr>
<tr>
<td width="40%"><a id="WCM_CONNECTION_COST_VARIABLE"></a><a id="wcm_connection_cost_variable"></a><dl>
<dt><b>WCM_CONNECTION_COST_VARIABLE</b></dt>
<dt>0x4</dt>
</dl>
</td>
<td width="60%">
The connection cost is on a per-byte basis.

</td>
</tr>
</table>
 

And may include any combination of the following flags:

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="WCM_CONNECTION_COST_OVERDATALIMIT"></a><a id="wcm_connection_cost_overdatalimit"></a><dl>
<dt><b>WCM_CONNECTION_COST_OVERDATALIMIT</b></dt>
<dt>0x10000</dt>
</dl>
</td>
<td width="60%">
The connection has exceeded its data limit.

</td>
</tr>
<tr>
<td width="40%"><a id="WCM_CONNECTION_COST_CONGESTED"></a><a id="wcm_connection_cost_congested"></a><dl>
<dt><b>WCM_CONNECTION_COST_CONGESTED</b></dt>
<dt>0x20000</dt>
</dl>
</td>
<td width="60%">
The connection is throttled due to high traffic.

</td>
</tr>
<tr>
<td width="40%"><a id="WCM_CONNECTION_COST_ROAMING"></a><a id="wcm_connection_cost_roaming"></a><dl>
<dt><b>WCM_CONNECTION_COST_ROAMING</b></dt>
<dt>0x40000</dt>
</dl>
</td>
<td width="60%">
The connection is outside of the home network.

</td>
</tr>
</table>

### -field CostSource

Type: <b><a href="/windows/desktop/api/wcmapi/ne-wcmapi-wcm_connection_cost_source">WCM_CONNECTION_COST_SOURCE</a></b>

Specifies the cost source.

## -see-also

<a href="/windows/desktop/api/wcmapi/ne-wcmapi-wcm_connection_cost_source">WCM_CONNECTION_COST_SOURCE</a>