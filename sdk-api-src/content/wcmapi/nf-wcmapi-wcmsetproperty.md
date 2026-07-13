---
UID: NF:wcmapi.WcmSetProperty
title: WcmSetProperty function (wcmapi.h)
description: Sets the value of a WCM property.
helpviewer_keywords: ["WcmSetProperty","WcmSetProperty function [Windows Connection Manager]","wcm.wcmsetproperty","wcmapi/WcmSetProperty"]
old-location: wcm\wcmsetproperty.htm
tech.root: wcm
ms.assetid: 79985d5e-a6a1-447c-b12e-11c6022c19a6
ms.date: 12/05/2018
ms.keywords: WcmSetProperty, WcmSetProperty function [Windows Connection Manager], wcm.wcmsetproperty, wcmapi/WcmSetProperty
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
req.lib: Wcmapi.lib
req.dll: Wcmapi.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - WcmSetProperty
 - wcmapi/WcmSetProperty
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - ext-ms-win-networking-wcmapi-l1-1-1.dll
 - Wcmapi.dll
 - Ext-MS-Win-networking-wcmapi-l1-1-0.dll
api_name:
 - WcmSetProperty
---

# WcmSetProperty function


## -description

The <b>WcmSetProperty</b> function sets the value of a WCM property.

## -parameters

### -param pInterface [in, optional]

Type: <b>const GUID*</b>

The interface to set. For global properties, this parameter is NULL.

### -param strProfileName [in, optional]

Type: <b>LPCWSTR</b>

The profile name.

### -param Property [in]

Type: <b><a href="/windows/desktop/api/wcmapi/ne-wcmapi-wcm_property">WCM_PROPERTY</a></b>

The WCM property to set.

### -param pReserved

Type: <b>PVOID</b>

Reserved.

### -param dwDataSize [in]

Type: <b>DWORD</b>

The size of the new property value.

### -param pbData [in, optional]

Type: <b>const BYTE*</b>

The new property value.

## -returns

Type: <b>DWORD</b>

Returns ERROR_SUCCESS if successful, or an error value otherwise.

## -remarks

The type of data stored in the <i>pbData</i> parameter will vary, depending on which property is being set. This table shows the data type of each property.

<table>
<tr>
<th>Property name</th>
<th>Data type</th>
</tr>
<tr>
<td>wcm_global_property_domain_policy</td>
<td>
<a href="/windows/desktop/api/wcmapi/ns-wcmapi-wcm_policy_value">WCM_POLICY_VALUE</a>
</td>
</tr>
<tr>
<td>wcm_global_property_minimize_policy</td>
<td>
<a href="/windows/desktop/api/wcmapi/ns-wcmapi-wcm_policy_value">WCM_POLICY_VALUE</a>
</td>
</tr>
<tr>
<td>wcm_global_property_roaming_policy</td>
<td>
<a href="/windows/desktop/api/wcmapi/ns-wcmapi-wcm_policy_value">WCM_POLICY_VALUE</a>
</td>
</tr>
<tr>
<td>wcm_global_property_powermanagement_policy</td>
<td>
<a href="/windows/desktop/api/wcmapi/ns-wcmapi-wcm_policy_value">WCM_POLICY_VALUE</a>
</td>
</tr>
<tr>
<td>wcm_intf_property_connection_cost</td>
<td>
<a href="/windows/desktop/api/wcmapi/ns-wcmapi-wcm_connection_cost_data">WCM_CONNECTION_COST_DATA</a>
</td>
</tr>
<tr>
<td>wcm_intf_property_dataplan_status</td>
<td>
<a href="/windows/desktop/api/wcmapi/ns-wcmapi-wcm_dataplan_status">WCM_DATAPLAN_STATUS</a>
</td>
</tr>
<tr>
<td>wcm_intf_property_hotspot_profile</td>
<td>Variable-length XML string. See the <a href="/uwp/schemas/mobilebroadbandschema/hotspotprofile/schema-root">HotSpotProfile schema</a> for more information.</td>
</tr>
</table>

## -see-also

<a href="/uwp/schemas/mobilebroadbandschema/hotspotprofile/schema-root">HotSpotProfile schema</a>



<a href="/windows/desktop/api/wcmapi/ne-wcmapi-wcm_property">WCM_PROPERTY</a>