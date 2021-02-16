---
UID: NF:wbemcli.IWbemClassObject.Next
title: IWbemClassObject::Next (wbemcli.h)
description: The IWbemClassObject::Next method retrieves the next property in an enumeration that started with IWbemClassObject::BeginEnumeration.
helpviewer_keywords: ["IWbemClassObject interface [Windows Management Instrumentation]","Next method","IWbemClassObject.Next","IWbemClassObject::Next","Next","Next method [Windows Management Instrumentation]","Next method [Windows Management Instrumentation]","IWbemClassObject interface","WBEM_FLAVOR_ORIGIN_LOCAL","WBEM_FLAVOR_ORIGIN_PROPAGATED","WBEM_FLAVOR_ORIGIN_SYSTEM","_hmm_iwbemclassobject_next","wbemcli/IWbemClassObject::Next","wmi.iwbemclassobject_next"]
old-location: wmi\iwbemclassobject_next.htm
tech.root: wmi
ms.assetid: 6d0e8aa3-ae64-4934-9000-2c526ceb7fb6
ms.date: 12/05/2018
ms.keywords: IWbemClassObject interface [Windows Management Instrumentation],Next method, IWbemClassObject.Next, IWbemClassObject::Next, Next, Next method [Windows Management Instrumentation], Next method [Windows Management Instrumentation],IWbemClassObject interface, WBEM_FLAVOR_ORIGIN_LOCAL, WBEM_FLAVOR_ORIGIN_PROPAGATED, WBEM_FLAVOR_ORIGIN_SYSTEM, _hmm_iwbemclassobject_next, wbemcli/IWbemClassObject::Next, wmi.iwbemclassobject_next
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
 - IWbemClassObject::Next
 - wbemcli/IWbemClassObject::Next
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
 - IWbemClassObject.Next
---

# IWbemClassObject::Next


## -description

The <b>IWbemClassObject::Next</b> method retrieves the 
    next property in an enumeration that started with 
    <a href="/windows/desktop/api/wbemcli/nf-wbemcli-iwbemclassobject-beginenumeration">IWbemClassObject::BeginEnumeration</a>. 
    This should be called repeatedly to enumerate all the properties until 
    <b>WBEM_S_NO_MORE_DATA</b> returns. If the enumeration is to be terminated early, then 
    <a href="/windows/desktop/api/wbemcli/nf-wbemcli-iwbemclassobject-endenumeration">IWbemClassObject::EndEnumeration</a> should 
    be called.

The order of the properties returned during the enumeration is not defined.

## -parameters

### -param lFlags [in]

Reserved. This parameter must be 0.

### -param strName [out]

Receives a new <b>BSTR</b> that contains the property name. To prevent memory leaks 
      in the client process, the caller must call 
      <a href="/previous-versions/windows/desktop/api/oleauto/nf-oleauto-sysfreestring">SysFreeString</a> when the name is no 
      longer required. You can set this parameter to <b>NULL</b> if the name is not required.

### -param pVal [out]

This <b>VARIANT</b> is filled with the value of the property. The method calls 
       <a href="/previous-versions/windows/desktop/api/oleauto/nf-oleauto-variantinit">VariantInit</a> on this 
       <b>VARIANT</b>, so the caller should ensure that the <b>VARIANT</b> 
       is not active prior to the call. The caller must use 
       <a href="/previous-versions/windows/desktop/api/oleauto/nf-oleauto-variantclear">VariantClear</a> when the value is no 
       longer required.

You can set this parameter to <b>NULL</b> if the value is not required. If an error code 
       is returned, the <b>VARIANT</b> pointed to by <i>pVal</i> is left 
       unmodified.

### -param pType [out, optional]

This parameter can be <b>NULL</b>. If it is not <b>NULL</b>, it must 
      point to a <b>CIMTYPE</b> variable (a <b>LONG</b>) into which the 
      type of the property is placed. It is possible that the value of this property can be a 
      <b>VT_NULL</b> <b>VARIANT</b>, in which case it 
      is necessary to determine the actual type of the property.

### -param plFlavor [out, optional]

Can be <b>NULL</b>. If not <b>NULL</b>, the 
       <b>LONG</b> value pointed to receives information on the origin of the property as 
       follows. For more information, see <a href="/windows/desktop/WmiSdk/qualifier-flavors">Qualifier Flavors</a> and <a href="/windows/win32/api/wbemcli/ne-wbemcli-wbem_flavor_type">WBEM_FLAVOR_TYPE</a>.



#### WBEM_FLAVOR_ORIGIN_SYSTEM

The property is a standard system property.



#### 

For classes:



#### WBEM_FLAVOR_ORIGIN_PROPAGATED

The property was inherited from the parent class.

The property, while inherited from the parent class, has not been modified at the instance level.



#### WBEM_FLAVOR_ORIGIN_LOCAL

The property belongs to the derived-most class.

The property is modified at the instance level (that is, either a value was supplied or a qualifier was 
        added/modified).

For instances:

## -returns

This method returns an <b>HRESULT</b> that indicates the status of the method call. The 
       following list lists the value contained within an <b>HRESULT</b>. For general 
       <b>HRESULT</b> values, see 
       <a href="/windows/desktop/Debug/system-error-codes">System Error Codes</a>.

## -remarks

If the underlying type of the property is an object path, date or time, or another special type, then the 
    returned type does not contain enough information. The caller must examine the 
    <a href="/windows/desktop/WmiSdk/cimtype-qualifier">CIMTYPE</a> for the specified property, and determine 
    if the property is an object reference, date or time, or another special type.

This method also returns 
    <a href="/windows/desktop/WmiSdk/wmi-system-properties">system properties</a>.

## -see-also

<a href="/windows/desktop/api/wbemcli/nn-wbemcli-iwbemclassobject">IWbemClassObject</a>



<a href="/windows/desktop/api/wbemcli/nf-wbemcli-iwbemclassobject-beginenumeration">IWbemClassObject::BeginEnumeration</a>



<a href="/windows/desktop/api/wbemcli/nf-wbemcli-iwbemclassobject-endenumeration">IWbemClassObject::EndEnumeration</a>



<a href="/windows/desktop/api/wbemcli/nf-wbemcli-iwbemclassobject-get">IWbemClassObject::Get</a>



<a href="/windows/desktop/WmiSdk/wmi-system-properties">WMI System Properties</a>