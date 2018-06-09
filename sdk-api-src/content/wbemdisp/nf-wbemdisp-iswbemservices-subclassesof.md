---
UID: NF:wbemdisp.ISWbemServices.SubclassesOf
title: ISWbemServices::SubclassesOf
author: windows-sdk-content
description: Returns an SWbemObjectSet object.
old-location: wmi\swbemservices_subclassesof.htm
old-project: WmiSdk
ms.assetid: cfe08956-7215-4e2e-a279-6e86f14e5c27
ms.author: windowssdkdev
ms.date: 06/07/2018
ms.keywords: ISWbemServices interface [Windows Management Instrumentation],SubclassesOf method, ISWbemServices.SubclassesOf, ISWbemServices::SubclassesOf, SWbemServices object [Windows Management Instrumentation],SubclassesOf method, SWbemServices.SubclassesOf, SubclassesOf, SubclassesOf method [Windows Management Instrumentation], SubclassesOf method [Windows Management Instrumentation],ISWbemServices interface, SubclassesOf method [Windows Management Instrumentation],SWbemServices object, _hmm_swbemservices.subclassesof, semisynchronous mode, wbemFlagReturnImmediately, wbemFlagReturnWhenComplete, wbemFlagUseAmendedQualifiers, wbemQueryFlagDeep, wbemQueryFlagShallow, wmi.swbemservices_subclassesof
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: wbemdisp.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: Wbemdisp.tlb
tech.root: 
req.typenames: WbemTimeout
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Wbemdisp.dll
api_name:
 - SWbemServices.SubclassesOf
 - ISWbemServices.SubclassesOf
 - ISWbemServices.SubclassesOf
product: Windows
targetos: Windows
req.lib: 
req.dll: Wbemdisp.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# ISWbemServices::SubclassesOf


## -description


The 
<b>SubclassesOf</b> method of the 
<a href="https://msdn.microsoft.com/7fcfa404-2fe6-42e5-85ac-64536f6d2a44">SWbemServices</a> object returns an 
<a href="https://msdn.microsoft.com/00f5317e-eb8e-42f9-bada-963e11aadda4">SWbemObjectSet</a> object. This object is a collection of subclasses of a specified class. Items in the returned collection can be obtained using standard collection methods. For more information, see 
<a href="https://msdn.microsoft.com/c1ebe529-33cb-4158-923d-124d6328fc60">Accessing a Collection</a>.

This method only works for class objects.

The method is called in the semisynchronous mode. For more information, see <a href="https://msdn.microsoft.com/7a1eda93-014e-4067-b6d0-361a3d2fd1df">Calling a Method</a>.

For an explanation of this syntax, see 
<a href="https://msdn.microsoft.com/889e6322-96f6-4a24-a084-e3b7bfa94a40">Document Conventions for the Scripting API</a>.


## -parameters




### -param strSuperclass [optional]

Specifies a parent class name. Only subclasses of this class return in the enumerator. If you leave this parameter blank, and if <i>iFlags</i> is <b>wbemQueryFlagShallow</b>, only the top-level classes are returned (that is, classes that have no parent class). If this parameter is blank and <i>iFlags</i> is <b>wbemQueryFlagDeep</b> all classes within the namespace are returned.


### -param iFlags [optional]

Determines how detailed the call enumerates. The default values for this parameter are <b>wbemFlagReturnImmediately</b> and <b>wbemQueryFlagDeep</b>. This parameter can accept the following values.



#### wbemQueryFlagShallow (1 (0x1))

Forces the enumeration to include only immediate subclasses of the specified parent class.



#### wbemQueryFlagDeep (0 (0x0))

Default for this parameter. This value forces recursive enumeration into all subclasses that are derived from the specified parent class. The parent class is not returned in the enumeration.



#### wbemFlagReturnImmediately (16 (0x10))

Causes the call to return immediately.



#### wbemFlagReturnWhenComplete (0 (0x0))

Causes this call to block until the call has completed. This flag calls the method in the synchronous mode.



#### wbemFlagUseAmendedQualifiers (131072 (0x20000))

Causes WMI to return class amendment data with the base class definition. 
For more information, see <a href="https://msdn.microsoft.com/01e1cee5-d882-45b6-ac93-68533c2c6c9d">Localizing WMI Class Information</a>.


### -param objWbemNamedValueSet [optional]

Typically, this is undefined. Otherwise, this is an 
<a href="https://msdn.microsoft.com/7d1c3a28-d0d3-4108-9628-74ad483e328e">SWbemNamedValueSet</a> object whose elements represent the context information that can be used by the provider servicing the request. A provider that supports or requires such information must document the recognized value names, data type of the value, allowed values, and semantics.


### -param objWbemObjectSet






## -returns



If the method is successful, an 
<a href="https://msdn.microsoft.com/00f5317e-eb8e-42f9-bada-963e11aadda4">SWbemObjectSet</a> object is returned.




## -see-also




<a href="https://msdn.microsoft.com/00f5317e-eb8e-42f9-bada-963e11aadda4">SWbemObjectSet</a>



<a href="https://msdn.microsoft.com/7fcfa404-2fe6-42e5-85ac-64536f6d2a44">SWbemServices</a>
 

 

