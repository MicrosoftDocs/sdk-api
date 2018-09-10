---
UID: NF:wcmapi.WcmQueryProperty
title: WcmQueryProperty function
author: windows-sdk-content
description: Retrieves the value of a specified WCM property.
old-location: wcm\wcmqueryproperty.htm
tech.root: wcm
ms.assetid: 07c0993e-2892-4908-be3f-d24210ccc300
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: WcmQueryProperty, WcmQueryProperty function [Windows Connection Manager], wcm.wcmqueryproperty, wcmapi/WcmQueryProperty
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Wcmapi.dll
 - Ext-MS-Win-networking-wcmapi-l1-1-0.dll
api_name:
 - WcmQueryProperty
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# WcmQueryProperty function


## -description


The <b>WcmQueryProperty</b> function retrieves the value of a specified WCM property.


## -parameters




### -param pInterface [in, optional]

Type: <b>const GUID*</b>

The interface to query. For global properties, this parameter is NULL.


### -param strProfileName [in, optional]

Type: <b>LPCWSTR</b>

The name of the profile. If querying a non-global property (<b>connection_cost</b>, <b>dataplan_status</b>, or <b>hotspot_profile</b>), the profile must be specified or the call will fail.


### -param Property [in]

Type: <b><a href="https://msdn.microsoft.com/4cb5f7aa-2f06-4a8a-814d-f8e01b496fb9">WCM_PROPERTY</a></b>

The WCM property to query.


### -param pReserved

Type: <b>PVOID</b>

Reserved.


### -param pdwDataSize [out]

Type: <b>PDWORD</b>

The size of the returned property value.


### -param ppData [out]

Type: <b>PBYTE*</b>

The returned property value.


## -returns



Type: <b>DWORD</b>

Returns ERROR_SUCCESS if successful, or an error value otherwise.




## -remarks



The type of data stored in the <i>ppData</i> parameter will vary, depending on which property is being queried. This table shows the data type of each property.

<table>
<tr>
<th>Property name</th>
<th>Data type</th>
</tr>
<tr>
<td>wcm_global_property_domain_policy</td>
<td>
<a href="https://msdn.microsoft.com/0f259661-723b-4c76-8652-c86e0b8c9ebf">WCM_POLICY_VALUE</a>
</td>
</tr>
<tr>
<td>wcm_global_property_minimize_policy</td>
<td>
<a href="https://msdn.microsoft.com/0f259661-723b-4c76-8652-c86e0b8c9ebf">WCM_POLICY_VALUE</a>
</td>
</tr>
<tr>
<td>wcm_global_property_roaming_policy</td>
<td>
<a href="https://msdn.microsoft.com/0f259661-723b-4c76-8652-c86e0b8c9ebf">WCM_POLICY_VALUE</a>
</td>
</tr>
<tr>
<td>wcm_global_property_powermanagement_policy</td>
<td>
<a href="https://msdn.microsoft.com/0f259661-723b-4c76-8652-c86e0b8c9ebf">WCM_POLICY_VALUE</a>
</td>
</tr>
<tr>
<td>wcm_intf_property_connection_cost</td>
<td>
<a href="https://msdn.microsoft.com/18fcc708-74b1-408f-a7ee-64455742324d">WCM_CONNECTION_COST_DATA</a>
</td>
</tr>
<tr>
<td>wcm_intf_property_dataplan_status</td>
<td>
<a href="https://msdn.microsoft.com/6ed0f05c-a9f8-49bb-9fb0-b91af8594d76">WCM_DATAPLAN_STATUS</a>
</td>
</tr>
<tr>
<td>wcm_intf_property_hotspot_profile</td>
<td>Contains zero-length output. </td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/4cb5f7aa-2f06-4a8a-814d-f8e01b496fb9">WCM_PROPERTY</a>
 

 

