---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
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
 

 

