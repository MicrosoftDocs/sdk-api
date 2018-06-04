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

# IWbemClassObject::NextMethod


## -description


The 
<b>IWbemClassObject::NextMethod</b> method is used to retrieve the next method in a method enumeration sequence that starts with 
a call to  <a href="https://msdn.microsoft.com/3d8656d7-37e5-4921-906e-c82f8878cd90">IWbemClassObject::BeginMethodEnumeration</a>.

This call is only supported if the current object is a CIM class definition. Method manipulation is not available from 
<a href="https://msdn.microsoft.com/a3ce37d7-5580-4b84-9119-78412c8e0d27">IWbemClassObject</a> pointers that point to CIM instances.


## -parameters




### -param lFlags [in]

Reserved. This parameter must be 0 (zero).


### -param pstrName




### -param ppInSignature [out]

A pointer that receives a pointer to an 
<a href="https://msdn.microsoft.com/a3ce37d7-5580-4b84-9119-78412c8e0d27">IWbemClassObject</a> containing the in parameters for the method.


### -param ppOutSignature [out]

A pointer that receives a pointer to an 
<a href="https://msdn.microsoft.com/a3ce37d7-5580-4b84-9119-78412c8e0d27">IWbemClassObject</a> containing the out parameters for the method.


#### - pName [out]

A pointer that should point to <b>NULL</b> prior to the call. This parameter receives the address of a <b>BSTR</b> value containing the method name. The caller must release the string using <b>SysFreeString</b> when it is no longer required.


## -returns



This method returns an <b>HRESULT</b> indicating the status of the method call. The following list lists the value contained within an <b>HRESULT</b>. For general <b>HRESULT</b> values, see <a href="https://msdn.microsoft.com/4a3a8feb-a05f-4614-8f04-1f507da7e5b7">System Error Codes</a>.




## -remarks



The caller begins the enumeration sequence using 
<a href="https://msdn.microsoft.com/3d8656d7-37e5-4921-906e-c82f8878cd90">IWbemClassObject::BeginMethodEnumeration</a>, and then calls 
<b>IWbemClassObject::NextMethod</b> until <b>WBEM_S_NO_MORE_DATA</b> is returned. The caller, optionally, finishes the sequence with 
<a href="https://msdn.microsoft.com/7a6de467-65f7-4873-a2dd-9c52c138b1d2">IWbemClassObject::EndMethodEnumeration</a>. The caller may terminate the enumeration early by calling 
<b>IWbemClassObject::EndMethodEnumeration</b> at any time.

<div class="alert"><b>Note</b>  The caller must call <a href="_com_iunknown_release">IWbemClassObject::Release</a> on the <i>ppInSignature</i> and <i>ppOutSignature</i> pointers when these objects are no longer required.</div>
<div> </div>


