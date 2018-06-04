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

# IWbemClassObject::EndMethodEnumeration


## -description


The 
<b>IWbemClassObject::EndMethodEnumeration</b> method is used to terminate a method enumeration sequence started with 
<a href="https://msdn.microsoft.com/3d8656d7-37e5-4921-906e-c82f8878cd90">IWbemClassObject::BeginMethodEnumeration</a>.

This call is only supported if the current object is a CIM class definition. Method manipulation is not available from 
<a href="https://msdn.microsoft.com/a3ce37d7-5580-4b84-9119-78412c8e0d27">IWbemClassObject</a> pointers which point to CIM instances.


## -parameters






## -returns



This method returns an <b>HRESULT</b> indicating the status of the method call. The following list lists the value contained within an <b>HRESULT</b>. For general <b>HRESULT</b> values, see <a href="https://msdn.microsoft.com/4a3a8feb-a05f-4614-8f04-1f507da7e5b7">System Error Codes</a>.




## -remarks



The caller begins the enumeration sequence using 
<a href="https://msdn.microsoft.com/3d8656d7-37e5-4921-906e-c82f8878cd90">IWbemClassObject::BeginMethodEnumeration</a>, and then calls 
<a href="https://msdn.microsoft.com/4c11e043-518b-46f6-bb39-e80354ef2c8a">IWbemClassObject::NextMethod</a> until <b>WBEM_S_NO_MORE_DATA</b> is returned. The caller optionally finishes the sequence with 
<b>IWbemClassObject::EndMethodEnumeration</b>. The caller may terminate the enumeration early by calling 
<b>IWbemClassObject::EndMethodEnumeration</b> at any time.



