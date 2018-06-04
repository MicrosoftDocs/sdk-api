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

# IWbemClassObject::Next


## -description


The <b>IWbemClassObject::Next</b> method retrieves the 
    next property in an enumeration that started with 
    <a href="https://msdn.microsoft.com/c7ece530-5309-4f0d-9096-73d01b4a7fde">IWbemClassObject::BeginEnumeration</a>. 
    This should be called repeatedly to enumerate all the properties until 
    <b>WBEM_S_NO_MORE_DATA</b> returns. If the enumeration is to be terminated early, then 
    <a href="https://msdn.microsoft.com/a9fa8567-7504-4d59-a874-1dc7b2620a0b">IWbemClassObject::EndEnumeration</a> should 
    be called.

The order of the properties returned during the enumeration is not defined.


## -parameters




### -param lFlags [in]

Reserved. This parameter must be 0.


### -param strName




### -param pVal [out]

This <b>VARIANT</b> is filled with the value of the property. The method calls 
       <a href="96aeb671-5528-4d3c-8e70-313716550b42">VariantInit</a> on this 
       <b>VARIANT</b>, so the caller should ensure that the <b>VARIANT</b> 
       is not active prior to the call. The caller must use 
       <a href="28741d81-8404-4f85-95d3-5c209ec13835">VariantClear</a> when the value is no 
       longer required.

You can set this parameter to <b>NULL</b> if the value is not required. If an error code 
       is returned, the <b>VARIANT</b> pointed to by <i>pVal</i> is left 
       unmodified.


### -param pType




### -param plFlavor [out, optional]

Can be <b>NULL</b>. If not <b>NULL</b>, the 
       <b>LONG</b> value pointed to receives information on the origin of the property as 
       follows. For more information, see <a href="https://msdn.microsoft.com/6a0769ac-e16c-45e1-92b6-26e4969bf23d">Qualifier Flavors</a> and <a href="https://msdn.microsoft.com/A21ED0FD-1207-42B6-92AE-6080D0E98771">WBEM_FLAVOR_TYPE</a>.



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


#### - pstrName [out]

Receives a new <b>BSTR</b> that contains the property name. To prevent memory leaks 
      in the client process, the caller must call 
      <a href="8f230ee3-5f6e-4cb9-a910-9c90b754dcd3">SysFreeString</a> when the name is no 
      longer required. You can set this parameter to <b>NULL</b> if the name is not required.


#### - pvtType [out, optional]

This parameter can be <b>NULL</b>. If it is not <b>NULL</b>, it must 
      point to a <b>CIMTYPE</b> variable (a <b>LONG</b>) into which the 
      type of the property is placed. It is possible that the value of this property can be a 
      <b>VT_NULL</b> <b>VARIANT</b>, in which case it 
      is necessary to determine the actual type of the property.


## -returns



This method returns an <b>HRESULT</b> that indicates the status of the method call. The 
       following list lists the value contained within an <b>HRESULT</b>. For general 
       <b>HRESULT</b> values, see 
       <a href="https://msdn.microsoft.com/4a3a8feb-a05f-4614-8f04-1f507da7e5b7">System Error Codes</a>.




## -remarks



If the underlying type of the property is an object path, date or time, or another special type, then the 
    returned type does not contain enough information. The caller must examine the 
    <a href="https://msdn.microsoft.com/ae65d4c7-2150-489b-a368-fb38c0d1b3be">CIMTYPE</a> for the specified property, and determine 
    if the property is an object reference, date or time, or another special type.

This method also returns 
    <a href="https://msdn.microsoft.com/e812c0cb-3e08-4cac-8d05-2cd7abc922d1">system properties</a>.




## -see-also




<a href="https://msdn.microsoft.com/a3ce37d7-5580-4b84-9119-78412c8e0d27">IWbemClassObject</a>



<a href="https://msdn.microsoft.com/c7ece530-5309-4f0d-9096-73d01b4a7fde">IWbemClassObject::BeginEnumeration</a>



<a href="https://msdn.microsoft.com/a9fa8567-7504-4d59-a874-1dc7b2620a0b">IWbemClassObject::EndEnumeration</a>



<a href="https://msdn.microsoft.com/e4f6c28b-42d7-4109-803e-d3aac4d8509e">IWbemClassObject::Get</a>



<a href="https://msdn.microsoft.com/e812c0cb-3e08-4cac-8d05-2cd7abc922d1">WMI System Properties</a>
 

 

