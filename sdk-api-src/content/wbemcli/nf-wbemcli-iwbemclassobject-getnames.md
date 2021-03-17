---
UID: NF:wbemcli.IWbemClassObject.GetNames
title: IWbemClassObject::GetNames (wbemcli.h)
description: Retrieves the names of the properties in the object.
helpviewer_keywords: ["GetNames","GetNames method [Windows Management Instrumentation]","GetNames method [Windows Management Instrumentation]","IWbemClassObject interface","IWbemClassObject interface [Windows Management Instrumentation]","GetNames method","IWbemClassObject.GetNames","IWbemClassObject::GetNames","_hmm_iwbemclassobject_getnames","wbemcli/IWbemClassObject::GetNames","wmi.iwbemclassobject_getnames"]
old-location: wmi\iwbemclassobject_getnames.htm
tech.root: wmi
ms.assetid: fc75fb17-52a2-40dd-b333-fcd01cae1430
ms.date: 12/05/2018
ms.keywords: GetNames, GetNames method [Windows Management Instrumentation], GetNames method [Windows Management Instrumentation],IWbemClassObject interface, IWbemClassObject interface [Windows Management Instrumentation],GetNames method, IWbemClassObject.GetNames, IWbemClassObject::GetNames, _hmm_iwbemclassobject_getnames, wbemcli/IWbemClassObject::GetNames, wmi.iwbemclassobject_getnames
req.header: wbemcli.h
req.include-header: Wbemidl.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: WbemCli.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: WbemUuid.lib
req.dll: CIMWin32.dll; Esscli.dll; Fastprox.dll; FrameDyn.dll; FrameDynOS.dll; Krnlprov.dll; Ncprov.dll; Wbemcore.dll; Wbemess.dll; Wmipiprt.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IWbemClassObject::GetNames
 - wbemcli/IWbemClassObject::GetNames
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - CIMWin32.dll
 - Esscli.dll
 - Fastprox.dll
 - FrameDyn.dll
 - FrameDynOS.dll
 - Krnlprov.dll
 - Ncprov.dll
 - Wbemcore.dll
 - Wbemess.dll
 - Wmipiprt.dll
api_name:
 - IWbemClassObject.GetNames
---

# IWbemClassObject::GetNames


## -description

The <b>IWbemClassObject::GetNames</b> method 
   retrieves the names of the properties in the object. Furthermore, depending on user-supplied 
   selection criteria, it can retrieve all or a subset of the properties. These properties can then be accessed by 
   using <a href="/windows/desktop/api/wbemcli/nf-wbemcli-iwbemclassobject-get">IWbemClassObject::Get</a> for each name. This 
   method can also return <a href="/windows/desktop/WmiSdk/wmi-system-properties">system properties</a>.

## -parameters

### -param wszQualifierName [in]

A parameter that can be <b>NULL</b>. If not <b>NULL</b>, it must point to a valid <b>LPCWSTR</b> specifying a qualifier name which operates as part of a filter. This is handled as read-only. For more information, see Remarks.

### -param lFlags [in]

For more information, see Remarks.

### -param pQualifierVal [in]

A parameter that can be <b>NULL</b>. If not <b>NULL</b>, it must point to a valid <b>VARIANT</b> structure initialized to a filter value. This <b>VARIANT</b> is handled as read-only by the method. Thus, the caller must call <b>VariantClear</b> on it, if required. For more information, see Remarks.

### -param pNames [out]

A parameter that cannot be <b>NULL</b>, but on entry this parameter must point to <b>NULL</b>. A new <b>SAFEARRAY</b> structure is always allocated, and the pointer is set to point to it. The returned array can have 0 elements, but is always allocated when <b>WBEM_S_NO_ERROR</b> returns. On error, a new <b>SAFEARRAY</b> structure is not returned.

## -returns

This method returns an <b>HRESULT</b> indicating the status of the method call. The following list lists the value contained within an <b>HRESULT</b>. For general <b>HRESULT</b> values, see <a href="/windows/desktop/Debug/system-error-codes">System Error Codes</a>.

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
<a href="/windows/desktop/WmiSdk/wmi-system-properties">system properties</a>.</td>
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
    <a href="/windows/desktop/WmiSdk/retrieving-part-of-an-instance">Retrieving Part of a WMI Instance</a>.

## -see-also

<a href="/windows/desktop/api/wbemcli/nn-wbemcli-iwbemclassobject">IWbemClassObject</a>



<a href="/windows/desktop/api/wbemcli/nf-wbemcli-iwbemclassobject-beginenumeration">IWbemClassObject::BeginEnumeration</a>



<a href="/windows/desktop/api/wbemcli/nf-wbemcli-iwbemclassobject-get">IWbemClassObject::Get</a>



<a href="/windows/win32/api/wbemcli/ne-wbemcli-wbem_condition_flag_type">WBEM_CONDITION_FLAG_TYPE</a>



<a href="/windows/desktop/WmiSdk/wmi-system-properties">WMI System Properties</a>