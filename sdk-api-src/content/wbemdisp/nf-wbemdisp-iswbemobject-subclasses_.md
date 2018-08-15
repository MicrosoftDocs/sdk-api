---
UID: NF:wbemdisp.ISWbemObject.Subclasses_
title: ISWbemObject::Subclasses_
author: windows-sdk-content
description: The Subclasses_ method of the SWbemObject object returns an SWbemObjectSet object.
old-location: wmi\swbemobject_subclasses_.htm
old-project: WmiSdk
ms.assetid: c17e5d4a-016f-42ae-bc11-e21a44772ce5
ms.author: windowssdkdev
ms.date: 08/03/2018
ms.keywords: ISWbemObject interface [Windows Management Instrumentation],Subclasses_ method, ISWbemObject.Subclasses_, ISWbemObject::Subclasses_, SWbemObject object [Windows Management Instrumentation],Subclasses_ method, SWbemObject.Subclasses_, Subclasses_, Subclasses_ method [Windows Management Instrumentation], Subclasses_ method [Windows Management Instrumentation],ISWbemObject interface, Subclasses_ method [Windows Management Instrumentation],SWbemObject object, WbemFlagReturnImmediately, _hmm_swbemobject.subclasses_, wbemFlagReturnWhenComplete, wbemFlagUseAmendedQualifiers, wbemQueryFlagDeep, wbemQueryFlagShallow, wmi.swbemobject_subclasses_
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: wbemdisp.h
req.include-header: 
req.redist: 
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
 - SWbemObject.Subclasses_
 - ISWbemObject.Subclasses_
 - ISWbemObject.Subclasses_
product: Windows
targetos: Windows
req.lib: 
req.dll: Wbemdisp.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# ISWbemObject::Subclasses_


## -description


The 
<b>Subclasses_</b> method of the 
<a href="https://msdn.microsoft.com/d303ec1a-5e0c-4a5e-8ed3-ed353a138755">SWbemObject</a> object returns an 
<a href="https://msdn.microsoft.com/00f5317e-eb8e-42f9-bada-963e11aadda4">SWbemObjectSet</a> object. This object is a collection of subclasses of the current object, which must be a class. Items in the returned collection can be obtained using standard collection methods. For more information, see 
<a href="https://msdn.microsoft.com/c1ebe529-33cb-4158-923d-124d6328fc60">Accessing a Collection</a>.

For an explanation of this syntax, see 
<a href="https://msdn.microsoft.com/889e6322-96f6-4a24-a084-e3b7bfa94a40">Document Conventions for the Scripting API</a>.


## -parameters




### -param iFlags [in, optional]

Integer that determines how detailed the call enumerates. This parameter can accept the following values.



#### wbemQueryFlagDeep (0 (0x0))

Forces recursive enumeration into all subclasses derived from the specified parent class. The parent class itself is not returned in the enumeration.



#### wbemQueryFlagShallow (1 (0x1))

Default value for this parameter. It forces the enumeration to include only immediate subclasses of the specified parent class.



#### WbemFlagReturnImmediately (16 (0x10))

Causes the call to return immediately



#### wbemFlagReturnWhenComplete (0 (0x0))

Causes this call to block until the call has completed.



#### wbemFlagUseAmendedQualifiers (131072 (0x20000))

Causes WMI to return class amendment data along with the base class definition.


### -param objWbemNamedValueSet




### -param objWbemObjectSet






#### - objwbemNamedValueSet [in, optional]

Typically, this is undefined. Otherwise, this is an 
<a href="https://msdn.microsoft.com/7d1c3a28-d0d3-4108-9628-74ad483e328e">SWbemNamedValueSet</a> object whose elements represent the context information that can be used by the provider that is servicing the request. A provider that supports or requires such information must document the recognized value names, data type of the value, allowed values, and semantics.


## -returns



If the call is successful, an 
<a href="https://msdn.microsoft.com/00f5317e-eb8e-42f9-bada-963e11aadda4">SWbemObjectSet</a> object is returned.




## -remarks



It is not an error for the returned collection to have zero elements if there are no subclasses of the current object. The 
<b>Subclasses_</b> method only works for class objects.




## -see-also




<a href="https://msdn.microsoft.com/d303ec1a-5e0c-4a5e-8ed3-ed353a138755">SWbemObject</a>



<a href="https://msdn.microsoft.com/00f5317e-eb8e-42f9-bada-963e11aadda4">SWbemObjectSet</a>
 

 

