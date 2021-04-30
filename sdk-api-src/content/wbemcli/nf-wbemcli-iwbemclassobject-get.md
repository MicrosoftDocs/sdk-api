---
UID: NF:wbemcli.IWbemClassObject.Get
title: IWbemClassObject::Get (wbemcli.h)
description: The IWbemClassObject::Get method retrieves the specified property value, if it exists. This method can also return system properties.
helpviewer_keywords: ["Get","Get method [Windows Management Instrumentation]","Get method [Windows Management Instrumentation]","IWbemClassObject interface","IWbemClassObject interface [Windows Management Instrumentation]","Get method","IWbemClassObject.Get","IWbemClassObject::Get","WBEM_FLAVOR_ORIGIN_LOCAL","WBEM_FLAVOR_ORIGIN_PROPAGATED","WBEM_FLAVOR_ORIGIN_SYSTEM","_hmm_iwbemclassobject_get","wbemcli/IWbemClassObject::Get","wmi.iwbemclassobject_get"]
old-location: wmi\iwbemclassobject_get.htm
tech.root: wmi
ms.assetid: e4f6c28b-42d7-4109-803e-d3aac4d8509e
ms.date: 12/05/2018
ms.keywords: Get, Get method [Windows Management Instrumentation], Get method [Windows Management Instrumentation],IWbemClassObject interface, IWbemClassObject interface [Windows Management Instrumentation],Get method, IWbemClassObject.Get, IWbemClassObject::Get, WBEM_FLAVOR_ORIGIN_LOCAL, WBEM_FLAVOR_ORIGIN_PROPAGATED, WBEM_FLAVOR_ORIGIN_SYSTEM, _hmm_iwbemclassobject_get, wbemcli/IWbemClassObject::Get, wmi.iwbemclassobject_get
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
 - IWbemClassObject::Get
 - wbemcli/IWbemClassObject::Get
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
 - IWbemClassObject.Get
---

# IWbemClassObject::Get


## -description

The 
<b>IWbemClassObject::Get</b> method retrieves the specified property value, if it exists. This method can also return 
<a href="/windows/desktop/WmiSdk/wmi-system-properties">system properties</a>.

## -parameters

### -param wszName [in]

Name of the desired property. It is treated as read-only.

### -param lFlags [in]

Reserved. This parameter must be 0 (zero).

### -param pVal [out]

When successful, this parameter is assigned the correct type and value for the qualifier, and the <a href="/previous-versions/windows/desktop/api/oleauto/nf-oleauto-variantinit">VariantInit</a> function is called on <i>pVal</i>. It is the responsibility of the caller to call <a href="/previous-versions/windows/desktop/api/oleauto/nf-oleauto-variantclear">VariantClear</a> on <i>pVal</i> when the value is not needed. If there is an error, the value that <i>pVal</i> points to is not modified. If an uninitialized <i>pVal</i> value is passed to the method, then the caller must check the return value of the method, and call <b>VariantClear</b> only when the method succeeds.

### -param pType [out, optional]

Can be <b>NULL</b>. If it is not <b>NULL</b>, it receives the CIM type of the property, that is, one of the CIM-type constants, such as <b>CIM_SINT32</b>, <b>CIM_STRING</b>, and so on. For more information about these values, see <a href="/windows/win32/api/wbemcli/ne-wbemcli-cimtype_enumeration">CIMTYPE_ENUMERATION</a>. This indicates the CIM semantics of the property value packed into <b>VARIANT</b>.

### -param plFlavor [out, optional]

Can be <b>NULL</b>. If not <b>NULL</b>, the LONG value pointed to receives information about the origin of the property. For more information, see <a href="/windows/desktop/WmiSdk/qualifier-flavors">Qualifier Flavors</a> and <a href="/windows/win32/api/wbemcli/ne-wbemcli-wbem_flavor_type">WBEM_FLAVOR_TYPE</a>.



#### WBEM_FLAVOR_ORIGIN_SYSTEM

The property is a standard system property.



#### WBEM_FLAVOR_ORIGIN_PROPAGATED

For classes only. The property was inherited from the parent class.

For instances only. The property is inherited from the parent class, but has not been modified at the instance level.



#### WBEM_FLAVOR_ORIGIN_LOCAL

For classes only. The property belongs to the derived child class.

For instances only. The property is modified at the instance level—that is, a value was supplied, or a qualifier was added or modified.

## -returns

This method returns an <b>HRESULT</b> that indicates the status of the method call. The following list lists the value contained in an <b>HRESULT</b>. For general <b>HRESULT</b> values, see <a href="/windows/desktop/Debug/system-error-codes">System Error Codes</a>.

## -remarks

If the  type of the property is an object path, date/time string, or other special type, then the returned values in the <b>VARIANT</b> do not contain enough information to identify the true type. The <i>pvtType</i> out parameter indicates this.

To obtain the string form of the Common Information Model (CIM) type for the property, the 
<a href="/windows/desktop/api/wbemcli/nn-wbemcli-iwbemqualifierset">IWbemQualifierSet</a> pointer for the property must be obtained, and the <b>Cimtype</b> qualifier retrieved. That qualifier is the string form of the CIM type, such as <b>sint32</b> versus <b>CIM_SINT32</b>, which is a numeric constant.

<div class="alert"><b>Note</b>  When you create a new object using 
<a href="/windows/desktop/api/wbemcli/nf-wbemcli-iwbemclassobject-spawninstance">IWbemClassObject::SpawnInstance</a>, it is important to note that some system properties are not set until the object is written to Windows Management Instrumentation (WMI). In all cases, 
<b>IWbemClassObject::Get</b>   succeeds in accessing the requested system property, but the returned <b>VARIANT</b> may contain <b>VT_NULL</b>.</div>
<div> </div>

#### Examples

For an extended discussion and example of making queries in C++ and WMI, see Making <a href="https://www.codeproject.com/Articles/10539/Making-WMI-Queries-In-C">WMI Queries In C++</a> on CodeProject.

<div class="code"></div>
The following C++ example shows how to retrieve the CIM class name from an object by using the system property <b>__CLASS.</b> The code requires the following #include statements and references to compile.


```cpp
#include <iostream>
using namespace std;
#include <wbemidl.h>
#pragma comment(lib, "wbemuuid.lib")
```

```cpp
//Assumes that pObj is defined as a pointer
// to an IWbemClassObject object.

VARIANT v;
BSTR strClassProp = SysAllocString(L"__CLASS");
HRESULT hr;
hr = pObj->Get(strClassProp, 0, &v, 0, 0);
SysFreeString(strClassProp);

// check the HRESULT to see if the action succeeded.

if (SUCCEEDED(hr) && (V_VT(&v) == VT_BSTR))
{
    wprintf(L"The class name is %s\n.", V_BSTR(&v));
}
else
{
    wprintf(L"Error in getting specified object\n");
}
VariantClear(&v);



```

## -see-also

<a href="/windows/desktop/api/wbemcli/nn-wbemcli-iwbemclassobject">IWbemClassObject</a>



<a href="/windows/desktop/api/wbemcli/nf-wbemcli-iwbemclassobject-getpropertyqualifierset">IWbemClassObject::GetPropertyQualifierSet</a>



<a href="/windows/desktop/WmiSdk/wmi-qualifiers">WMI Qualifiers</a>



<a href="/windows/desktop/WmiSdk/wmi-system-classes">WMI System Classes</a>



<a href="/windows/desktop/WmiSdk/wmi-system-properties">WMI System Properties</a>