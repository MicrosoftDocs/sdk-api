---
UID: NF:wbemdisp.ISWbemObject.Instances_
title: ISWbemObject::Instances_
author: windows-sdk-content
description: The Instances_ method of the SWbemObject object creates an enumerator that returns the instances of the current class object. This method implements a simple query. More complex queries may require the use of SWbemServices.ExecQuery.
old-location: wmi\swbemobject_instances_.htm
old-project: WmiSdk
ms.assetid: 30402d7d-f7cb-43b5-96b5-a8a76144e32d
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: ISWbemObject interface [Windows Management Instrumentation],Instances_ method, ISWbemObject.Instances_, ISWbemObject::Instances_, Instances_, Instances_ method [Windows Management Instrumentation], Instances_ method [Windows Management Instrumentation],ISWbemObject interface, Instances_ method [Windows Management Instrumentation],SWbemObject object, SWbemObject object [Windows Management Instrumentation],Instances_ method, SWbemObject.Instances_, _hmm_swbemobject.instances_, wbemFlagBidirectional, wbemFlagForwardOnly, wbemFlagReturnImmediately, wbemFlagReturnWhenComplete, wbemFlagUseAmendedQualifiers, wbemQueryFlagDeep, wbemQueryFlagShallow, wmi.swbemobject_instances_
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
 - SWbemObject.Instances_
 - ISWbemObject.Instances_
 - ISWbemObject.Instances_
product: Windows
targetos: Windows
req.lib: 
req.dll: Wbemdisp.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# ISWbemObject::Instances_


## -description


The 
<b>Instances_</b> method of the 
<a href="https://msdn.microsoft.com/d303ec1a-5e0c-4a5e-8ed3-ed353a138755">SWbemObject</a> object creates an enumerator that returns the instances of the current class object. This method implements a simple query. More complex queries may require the use of 
<a href="https://msdn.microsoft.com/06b9d4c9-cd72-49b2-92b0-d18d94dfbd9f">SWbemServices.ExecQuery</a>.

For an explanation of this syntax, see 
<a href="https://msdn.microsoft.com/889e6322-96f6-4a24-a084-e3b7bfa94a40">Document Conventions for the Scripting API</a>.


## -parameters




### -param iFlags [in, optional]

Integer that determines the behavior of the call. This parameter can accept the following values.



#### wbemFlagForwardOnly (32 (0x20))

Causes a forward-only enumerator to be returned. Forward-only enumerators are generally much faster and use less memory than conventional enumerators, but they do not allow calls to 
<a href="https://msdn.microsoft.com/d0773c94-30b5-4217-8a9a-0bceb9e75f02">SWbemObject.Clone_</a>.



#### wbemFlagBidirectional (0 (0x0))

Causes WMI to retain pointers to objects of the enumeration until the client releases the enumerator.



#### wbemFlagReturnImmediately (16 (0x10))

Default value for this parameter. This flag causes the call to return immediately.



#### wbemFlagReturnWhenComplete (0 (0x0))

Causes this call to block until the query has completed.



#### wbemQueryFlagShallow (1 (0x1))

Forces the enumeration to include only immediate subclasses of the specified parent class.



#### wbemQueryFlagDeep (0 (0x0))

Default for this parameter. This value forces the enumeration to include all classes in the hierarchy.



#### wbemFlagUseAmendedQualifiers (131072 (0x20000))

Causes WMI to return class amendment data with the base class definition.


### -param objWbemNamedValueSet




### -param objWbemObjectSet






#### - objwbemNamedValueSet [in, optional]

Typically, this is undefined. Otherwise, this is an 
<a href="https://msdn.microsoft.com/7d1c3a28-d0d3-4108-9628-74ad483e328e">SWbemNamedValueSet</a> object whose elements represent the context information that can be used by the provider that is servicing the request. A provider that supports or requires such information must document the recognized value names, data type of the value, allowed values, and semantics.


## -returns



If the method is successful, an 
<a href="https://msdn.microsoft.com/00f5317e-eb8e-42f9-bada-963e11aadda4">SWbemObjectSet</a> object returns.




## -remarks



The 
<b>Instances_</b> method only works for class objects. It is not an error for the returned collection to have zero elements. The default behavior for this method is <a href="gloss_s.htm">semisynchronous</a> because of the default <i>IFlags</i> value <b>wbemFlagReturnImmediately</b>.




## -see-also




<a href="https://msdn.microsoft.com/d303ec1a-5e0c-4a5e-8ed3-ed353a138755">SWbemObject</a>



<a href="https://msdn.microsoft.com/00f5317e-eb8e-42f9-bada-963e11aadda4">SWbemObjectSet</a>
 

 

