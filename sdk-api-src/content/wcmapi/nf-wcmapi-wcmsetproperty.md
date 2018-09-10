---
UID: NF:wcmapi.WcmSetProperty
title: WcmSetProperty function
author: windows-sdk-content
description: Sets the value of a WCM property.
old-location: wcm\wcmsetproperty.htm
tech.root: wcm
ms.assetid: 79985d5e-a6a1-447c-b12e-11c6022c19a6
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: WcmSetProperty, WcmSetProperty function [Windows Connection Manager], wcm.wcmsetproperty, wcmapi/WcmSetProperty
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
 - WcmSetProperty
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
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

Type: <b><a href="https://msdn.microsoft.com/4cb5f7aa-2f06-4a8a-814d-f8e01b496fb9">WCM_PROPERTY</a></b>

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
<td>Variable-length XML string. See the <a href="https://msdn.microsoft.com/bae26f60-b40d-4ebe-85e0-daef3635f295">HotSpotProfile schema</a> for more information.</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/bae26f60-b40d-4ebe-85e0-daef3635f295">HotSpotProfile schema</a>



<a href="https://msdn.microsoft.com/4cb5f7aa-2f06-4a8a-814d-f8e01b496fb9">WCM_PROPERTY</a>
 

 

