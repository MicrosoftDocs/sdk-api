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

# IWbemClassObject::GetNames


## -description


The <b>IWbemClassObject::GetNames</b> method 
   retrieves the names of the properties in the object. Furthermore, depending on user-supplied 
   selection criteria, it can retrieve all or a subset of the properties. These properties can then be accessed by 
   using <a href="https://msdn.microsoft.com/e4f6c28b-42d7-4109-803e-d3aac4d8509e">IWbemClassObject::Get</a> for each name. This 
   method can also return <a href="https://msdn.microsoft.com/e812c0cb-3e08-4cac-8d05-2cd7abc922d1">system properties</a>.


## -parameters




### -param wszQualifierName [in]

A parameter that can be <b>NULL</b>. If not <b>NULL</b>, it must point to a valid <b>LPCWSTR</b> specifying a qualifier name which operates as part of a filter. This is handled as read-only. For more information, see Remarks.


### -param lFlags [in]

For more information, see Remarks.


### -param pQualifierVal




### -param pNames






#### - pQualifierValue [in]

A parameter that can be <b>NULL</b>. If not <b>NULL</b>, it must point to a valid <b>VARIANT</b> structure initialized to a filter value. This <b>VARIANT</b> is handled as read-only by the method. Thus, the caller must call <b>VariantClear</b> on it, if required. For more information, see Remarks.


#### - pstrNames [out]

A parameter that cannot be <b>NULL</b>, but on entry this parameter must point to <b>NULL</b>. A new <b>SAFEARRAY</b> structure is always allocated, and the pointer is set to point to it. The returned array can have 0 elements, but is always allocated when <b>WBEM_S_NO_ERROR</b> returns. On error, a new <b>SAFEARRAY</b> structure is not returned.


## -returns



This method returns an <b>HRESULT</b> indicating the status of the method call. The following list lists the value contained within an <b>HRESULT</b>. For general <b>HRESULT</b> values, see <a href="https://msdn.microsoft.com/4a3a8feb-a05f-4614-8f04-1f507da7e5b7">System Error Codes</a>.




## -remarks



The names returned are controlled by a combination of flags and parameters. For example, all names of all 
     properties can be specified, or only the key properties can be specified, and so on. The primary filter is 
     specified in the <i>lFlags</i> parameter; the other parameters vary depending upon it.

The flag values are bit fields, and can be combined. One flag from each of the following groups can be combined 
     with a flag from each of the other groups. Flag values within a group are mutually exclusive.

<table>
<tr>
<th>Group 1 flags</th>
<th>Description</th>
</tr>
<tr>
<td><b>WBEM_FLAG_ALWAYS</b></td>
<td>Return all property names. The <i>strQualifierName</i> and <i>pQualifierVal</i> parameters are not used.</td>
</tr>
<tr>
<td><b>WBEM_FLAG_ONLY_IF_TRUE</b></td>
<td>Return only properties that have a qualifier of the name specified by the parameter <i>strQualifierName</i>. If this flag is used, you must specify <i>strQualifierName</i>.</td>
</tr>
<tr>
<td><b>WBEM_FLAG_ONLY_IF_FALSE</b></td>
<td>Return only properties that do not have a qualifier of the name specified by the parameter <i>strQualifierName</i>. If this flag is used, you must specify <i>strQualifierName</i>.</td>
</tr>
<tr>
<td><b>WBEM_FLAG_ONLY_IF_IDENTICAL</b></td>
<td>Return only properties that have a qualifier of the name specified by the parameter <i>QualifierName</i>, and also have a value identical to the value specified by the <b>VARIANT</b> structure pointed to by <i>pQualifierVal</i>. If this flag is used, you must specify both <i>QualifierName</i> and <i>pQualifierVal</i>.</td>
</tr>
</table>
 

<table>
<tr>
<th>Group 2 flags</th>
<th>Description</th>
</tr>
<tr>
<td><b>WBEM_FLAG_KEYS_ONLY</b></td>
<td>Return only the names of the property or properties that define the keys.</td>
</tr>
<tr>
<td><b>WBEM_FLAG_REFS_ONLY</b></td>
<td>Return only property names that are object references.</td>
</tr>
</table>
 

<table>
<tr>
<th>Group 3 flags</th>
<th>Description</th>
</tr>
<tr>
<td><b>WBEM_FLAG_LOCAL_ONLY</b></td>
<td>Return only property names that belong to the derived-most class. Exclude properties from the parent class or parent classes.</td>
</tr>
<tr>
<td><b>WBEM_FLAG_PROPAGATED_ONLY</b></td>
<td>Return only property names that belong to the parent class or parent classes.</td>
</tr>
<tr>
<td><b>WBEM_FLAG_SYSTEM_ONLY</b></td>
<td>Return only 
<a href="https://msdn.microsoft.com/e812c0cb-3e08-4cac-8d05-2cd7abc922d1">system properties</a>.</td>
</tr>
<tr>
<td><b>WBEM_FLAG_NONSYSTEM_ONLY</b></td>
<td>Return only property names that are not system properties.</td>
</tr>
</table>
 

It is not an error for an empty list to be returned in cases where no properties match the specified 
    filters.

For more information about using <b>SAFEARRAY</b> structures of 
    <b>BSTR</b> values, see 
    <a href="https://msdn.microsoft.com/6cc26b26-adc9-4a8a-b51e-9db94eb4295f">Retrieving Part of a WMI Instance</a>.




## -see-also




<a href="https://msdn.microsoft.com/a3ce37d7-5580-4b84-9119-78412c8e0d27">IWbemClassObject</a>



<a href="https://msdn.microsoft.com/c7ece530-5309-4f0d-9096-73d01b4a7fde">IWbemClassObject::BeginEnumeration</a>



<a href="https://msdn.microsoft.com/e4f6c28b-42d7-4109-803e-d3aac4d8509e">IWbemClassObject::Get</a>



<a href="https://msdn.microsoft.com/8A3858C1-D2A1-41FB-ADD4-EA36075A1ACC">WBEM_CONDITION_FLAG_TYPE</a>



<a href="https://msdn.microsoft.com/e812c0cb-3e08-4cac-8d05-2cd7abc922d1">WMI System Properties</a>
 

 

