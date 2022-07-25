---
UID: NF:wbemcli.IWbemClassObject.Put
title: IWbemClassObject::Put (wbemcli.h)
description: Sets a named property to a new value.
helpviewer_keywords: ["IWbemClassObject interface [Windows Management Instrumentation]","Put method","IWbemClassObject.Put","IWbemClassObject::Put","Put","Put method [Windows Management Instrumentation]","Put method [Windows Management Instrumentation]","IWbemClassObject interface","_hmm_iwbemclassobject_put","wbemcli/IWbemClassObject::Put","wmi.iwbemclassobject_put"]
old-location: wmi\iwbemclassobject_put.htm
tech.root: wmi
ms.assetid: 7b67739f-5c67-447a-a1a5-fad9ce3e857a
ms.date: 12/05/2018
ms.keywords: IWbemClassObject interface [Windows Management Instrumentation],Put method, IWbemClassObject.Put, IWbemClassObject::Put, Put, Put method [Windows Management Instrumentation], Put method [Windows Management Instrumentation],IWbemClassObject interface, _hmm_iwbemclassobject_put, wbemcli/IWbemClassObject::Put, wmi.iwbemclassobject_put
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
 - IWbemClassObject::Put
 - wbemcli/IWbemClassObject::Put
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
 - IWbemClassObject.Put
---

# IWbemClassObject::Put


## -description

The 
<b>IWbemClassObject::Put</b> method sets a named property to a new value. This method always overwrites the current value with a new one. When 
<a href="/windows/desktop/api/wbemcli/nn-wbemcli-iwbemclassobject">IWbemClassObject</a> points to a CIM class definition, 
<b>Put</b>  creates or updates the property value. When 
<b>IWbemClassObject</b> points to a CIM instance, 
<b>Put</b> updates a property value only. <b>Put</b> cannot create a property value.

A user cannot create properties with names that begin or end with an underscore (_). This is reserved for system classes and properties.

## -parameters

### -param wszName [in]

A parameter that must point to a valid property name. This parameter cannot be <b>NULL</b>.

### -param lFlags [in]

Reserved. This parameter must be 0 (zero).

### -param pVal [in]

A parameter that must point to a valid <b>VARIANT</b>, which becomes the new property value. If <i>pVal</i> is <b>NULL</b> or points to a <b>VARIANT</b> of type <b>VT_NULL</b>, the property is set to <b>NULL</b>, that is, no value.

### -param Type [in]

A type of <b>VARIANT</b> pointed to by <i>pVal</i>.

The <b>NULL</b> value for a property designated by a <b>VARIANT</b> of type <b>VT_NULL</b> is distinguished from a property of type <b>VT_I4</b> with a 0 (zero) value.

When creating new properties, if <i>pVal</i> is <b>NULL</b> or points to a <b>VT_NULL</b>, the type of the property is determined from the <i>vtType</i> parameter.

If <i>pVal</i> is to contain an embedded 
<a href="/windows/desktop/api/wbemcli/nn-wbemcli-iwbemclassobject">IWbemClassObject</a>, the caller must call <b>IWbemClassObject::QueryInterface</b> for <b>IID_IUnknown</b> and place the resulting pointer in the <b>VARIANT</b> using a type of <b>VT_UNKNOWN</b>. The original embedded object is copied during the 
<b>Put</b> operation, and so cannot be modified by the operation.

The pointer is treated as read-only. The caller must call <a href="/previous-versions/windows/desktop/api/oleauto/nf-oleauto-variantclear">VariantClear</a> after this call is complete.

Use this parameter only when creating new properties in a CIM class definition and <i>pVal</i> is <b>NULL</b> or points to a <b>VARIANT</b> of type <b>VT_NULL</b>. In such a case, the <i>vtType</i> parameter specifies the CIM type of the property. In every other case, <i>vtType</i> must be 0 (zero). Also, <i>vtType</i> must be 0 (zero) when the underlying object is an instance (even if <i>pVal</i> is <b>NULL</b>), because the type of the property is fixed and cannot be changed. In other words, use <i>vtType</i> if, and only if, <i>pVal</i> is <b>NULL</b> or points to a <b>VT_NULL</b><b>VARIANT</b>, and the underlying object is a CIM class.

When using 
<b>IWbemClassObject::Put</b> to assign empty array values to a property, you do not need to specify the exact VT type; you can assign a value to <i>pVal</i> that is a <b>VARIANT</b> with a variant type of <b>VT_ARRAY</b>|<b>VT_VARIANT</b>.

## -returns

This method returns an <b>HRESULT</b> that indicates the status of the method call. The following list lists the values contained within an <b>HRESULT</b>. For general <b>HRESULT</b> values, see <a href="/windows/desktop/Debug/system-error-codes">System Error Codes</a>.

## -remarks

If the property set by the 
<b>IWbemClassObject::Put</b> method exists in the parent class, the default value of the property is changed unless the property type does not match the parent class type. If the property does not exist and it is not a type mismatch, the property is created.

When executing this method on an instance, an overwrite always occurs, because the property always exists.

When creating a new class and the underlying type of the property is an object reference, date/time string, or other special type, you might need to modify the CIM type parameter for the property to indicate the special new class. The 
<a href="/windows/desktop/WmiSdk/swbemproperty-cimtype">CIMType</a> qualifier on instance properties is read-only and inherited from the class object.

If the variant type specified in <i>pVal</i> does not match the CIM type of the property, WMI attempts to change the variant to the appropriate variant type, using the normal variant coercion rules. If the variant cannot be coerced, <b>WBEM_E_TYPE_MISMATCH</b> is returned. The following list lists exceptions to the normal variant coercion rules when the property is type <b>uint32</b>.

<table>
<tr>
<th>Pass in variant type</th>
<th>Result</th>
</tr>
<tr>
<td><b>VT_I4</b></td>
<td><b>S_OK</b></td>
</tr>
<tr>
<td><b>VT_I2</b></td>
<td><b>WBEM_TYPE_MISMATCH</b></td>
</tr>
<tr>
<td><b>VT_R8</b></td>
<td>
<b>S_OK</b>

However, passing in a <b>VT_ARRAY</b>|<b>VT_R8</b> to a property of type <b>uint32</b>[] will fail.

</td>
</tr>
</table>
 

The 
<a href="/windows/desktop/WmiSdk/wmi-system-properties">__CLASS</a> system property is only writable during class creation, when it may not be left blank. All other system properties are read-only.


#### Examples

The following code example shows how to set the class name for a new CIM class.


```cpp
// pObj is an empty object from IWbemServices::GetObject
// Set up the property value.
VARIANT v; 
VariantInit(&v);
V_VT(&v) = VT_BSTR;
V_BSTR(&v) = SysAllocString(L"MyClass");

// Write it.
LPCWSTR strClassProp = L"__CLASS";
pObj->Put(strClassProp, 0, &v, 0);

// Clean up.
VariantClear(&v);
```


The following code example shows  how to set the value of the  SomeUint64 property.  Be aware that the <b>BSTR</b> value must be in decimal format and not hexadecimal.


```cpp
// pObj is an instance containing a uint64 property
// Set up the property value.
VARIANT v; 
VariantInit(&v);
V_VT(&v) = VT_BSTR;
V_BSTR(&v) = SysAllocString(L"1033"); // - decimal format, not hex

// Write it.
LPCWSTR strClassProp = L"SomeUint64";
pObj->Put(strClassProp, 0, &v, CIM_UINT64);

// Clean up.
VariantClear(&v);
```

## -see-also

<a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)">IUnknown::QueryInterface</a>



<a href="/windows/desktop/api/wbemcli/nn-wbemcli-iwbemclassobject">IWbemClassObject</a>



<a href="/windows/desktop/WmiSdk/wmi-qualifiers">WMI Qualifiers</a>



<a href="/windows/desktop/WmiSdk/wmi-system-classes">WMI System Classes</a>



<a href="/windows/desktop/WmiSdk/wmi-system-properties">WMI System Properties</a>