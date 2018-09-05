---
UID: NF:wbemdisp.ISWbemObject.References_
title: ISWbemObject::References_
author: windows-sdk-content
description: The References_ method of the SWbemObject object returns a collection of all association classes or instances that refer to the current object.
old-location: wmi\swbemobject_references_.htm
old-project: WmiSdk
ms.assetid: ba02da47-0bb2-40e1-af50-1c42b4be2abd
ms.author: windowssdkdev
ms.date: 08/28/2018
ms.keywords: ISWbemObject interface [Windows Management Instrumentation],References_ method, ISWbemObject.References_, ISWbemObject::References_, References_, References_ method [Windows Management Instrumentation], References_ method [Windows Management Instrumentation],ISWbemObject interface, References_ method [Windows Management Instrumentation],SWbemObject object, SWbemObject object [Windows Management Instrumentation],References_ method, SWbemObject.References_, _hmm_swbemobject.references_, wbemFlagBidirectional, wbemFlagForwardOnly, wbemFlagReturnImmediately, wbemFlagReturnWhenComplete, wbemFlagUseAmendedQualifiers, wmi.swbemobject_references_
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
 - SWbemObject.References_
 - ISWbemObject.References_
 - ISWbemObject.References_
product: Windows
targetos: Windows
req.lib: 
req.dll: Wbemdisp.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# ISWbemObject::References_


## -description


The 
<b>References_</b> method of the 
<a href="https://msdn.microsoft.com/d303ec1a-5e0c-4a5e-8ed3-ed353a138755">SWbemObject</a> object returns a collection of all association classes or instances that refer to the current object.

This method performs the same function as the <a href="https://msdn.microsoft.com/674be546-e7fd-4150-9d7c-2888d24bf1b3">REFERENCES OF</a> WQL query.

For an explanation of this syntax, see 
<a href="https://msdn.microsoft.com/889e6322-96f6-4a24-a084-e3b7bfa94a40">Document Conventions for the Scripting API</a>.


## -parameters




### -param strResultClass [in, optional]

String that contains a class name. If specified, this parameter indicates that the returned association objects must belong to or be derived from the class specified in this parameter.


### -param strRole [in, optional]

String that contains a property name. If specified, this parameter indicates that the returned association objects must be limited to those in which the source object plays a specific role. The role is defined by the name of a specified property (which must be a reference property) of an association.


### -param bClassesOnly [in, optional]

Boolean value that indicates whether or not a list of class names should be returned rather than actual instances of the classes. These are the classes to which the association objects belong. The default value for this parameter is <b>FALSE</b>.


### -param bSchemaOnly [in, optional]

Boolean value that indicates whether or not the query applies to the schema rather than the data. The default value for this parameter is <b>FALSE</b>. It can only be set to <b>TRUE</b> if the object on which this method is invoked is a class. When set to <b>TRUE</b>, the set of returned endpoints represents classes that are suitably associated with the source class in the schema.


### -param strRequiredQualifier [in, optional]

String that contains a qualifier name. If specified, this parameter indicates that the returned association objects must include the specified qualifier.


### -param iFlags [in, optional]

Integer specifying additional flags to the operation. The default for this parameter is <b>wbemFlagReturnImmediately</b>, which directs the call to return immediately rather than wait until the query has completed. This parameter can accept the following values.



#### wbemFlagForwardOnly (32 (0x20))

Causes a forward-only enumerator to be returned. Forward-only enumerators are generally much faster and use less memory than conventional enumerators, but they do not allow calls to 
<a href="https://msdn.microsoft.com/d0773c94-30b5-4217-8a9a-0bceb9e75f02">SWbemObject.Clone_</a>.



#### wbemFlagBidirectional (0 (0x0))

Causes Windows Management Instrumentation (WMI) to retain pointers to objects of the enumeration until the client releases the enumerator.



#### wbemFlagReturnImmediately (16 (0x10))

Causes the call to return immediately.



#### wbemFlagReturnWhenComplete (0 (0x0))

Causes this call to block until the query has completed.



#### wbemFlagUseAmendedQualifiers (131072 (0x20000))

Causes WMI to return class amendment data with the base class definition. 
For more information about amended qualifiers, see <a href="https://msdn.microsoft.com/01e1cee5-d882-45b6-ac93-68533c2c6c9d">Localizing WMI Class Information</a>.


### -param objWbemNamedValueSet




### -param objWbemObjectSet






#### - objwbemNamedValueSet [in, optional]

Typically, this is undefined. Otherwise, this is an 
<a href="https://msdn.microsoft.com/7d1c3a28-d0d3-4108-9628-74ad483e328e">SWbemNamedValueSet</a> object whose elements represent the context information that can be used by the provider that is servicing the request. A provider that supports or requires such information must document the recognized value names, data type of the value, allowed values, and semantics.


## -returns



If the call is successful, an 
<a href="https://msdn.microsoft.com/00f5317e-eb8e-42f9-bada-963e11aadda4">SWbemObjectSet</a> object is returned.




## -remarks



For more information about the REFERENCES OF associated WQL query, source instances, and association objects, see 
<a href="https://msdn.microsoft.com/d6bd9643-523d-4d81-8bf1-da52ccc7524d">ASSOCIATORS OF Statement</a>.




## -see-also




<a href="https://msdn.microsoft.com/d303ec1a-5e0c-4a5e-8ed3-ed353a138755">SWbemObject</a>



<a href="https://msdn.microsoft.com/79f01853-c649-4cbe-b2fa-cff38fb4b733">SWbemObject.Associators_</a>



<a href="https://msdn.microsoft.com/a78e6701-6779-4a02-b811-23b2da4f4167">SWbemServices.AssociatorsOf</a>



<a href="https://msdn.microsoft.com/33425b1c-13f5-4c3d-8f8a-2922f3e95264">SWbemServices.ReferencesTo</a>
 

 

