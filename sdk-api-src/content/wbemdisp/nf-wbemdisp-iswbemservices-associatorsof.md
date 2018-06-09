---
UID: NF:wbemdisp.ISWbemServices.AssociatorsOf
title: ISWbemServices::AssociatorsOf
author: windows-sdk-content
description: Returns a collection of objects (classes or instances) called endpoints that are associated with a specified object.
old-location: wmi\swbemservices_associatorsof.htm
old-project: WmiSdk
ms.assetid: a78e6701-6779-4a02-b811-23b2da4f4167
ms.author: windowssdkdev
ms.date: 06/07/2018
ms.keywords: AssociatorsOf, AssociatorsOf method [Windows Management Instrumentation], AssociatorsOf method [Windows Management Instrumentation],ISWbemServices interface, AssociatorsOf method [Windows Management Instrumentation],SWbemServices object, ISWbemServices interface [Windows Management Instrumentation],AssociatorsOf method, ISWbemServices.AssociatorsOf, ISWbemServices::AssociatorsOf, SWbemServices object [Windows Management Instrumentation],AssociatorsOf method, SWbemServices.AssociatorsOf, _hmm_swbemservices.associatorsof, wbemFlagBidirectional, wbemFlagForwardOnly, wbemFlagReturnImmediately, wbemFlagReturnWhenComplete, wbemFlagUseAmendedQualifiers, wmi.swbemservices_associatorsof
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
 - SWbemServices.AssociatorsOf
 - ISWbemServices.AssociatorsOf
 - ISWbemServices.AssociatorsOf
product: Windows
targetos: Windows
req.lib: 
req.dll: Wbemdisp.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# ISWbemServices::AssociatorsOf


## -description


The 
<b>AssociatorsOf</b> method of the 
<a href="https://msdn.microsoft.com/7fcfa404-2fe6-42e5-85ac-64536f6d2a44">SWbemServices</a> object returns a collection of objects (classes or instances) called endpoints that are associated with a specified object.  This method performs the same function that the ASSOCIATORS OF WQL query performs.

This method is  called in the semisynchronous mode by default. For more information, see <a href="https://msdn.microsoft.com/7a1eda93-014e-4067-b6d0-361a3d2fd1df">Calling a Method</a>.

For an explanation of this syntax, see 
<a href="https://msdn.microsoft.com/889e6322-96f6-4a24-a084-e3b7bfa94a40">Document Conventions for the Scripting API</a>.


## -parameters




### -param strObjectPath

Required. String that contains the object path of the source class or instance. For more information, see <a href="https://msdn.microsoft.com/7a390541-609d-4b97-b91c-1a41d21ec17d">Describing the Location of a WMI Object</a>.


### -param strAssocClass [optional]

String that contains an association class. If specified, this parameter indicates that the returned endpoints must be associated with the source through the specified association class or a class that is derived from this association class.


### -param strResultClass [optional]

String that contains a class name. If specified, this optional parameter indicates that the returned endpoints must belong to or be derived from the class specified in this parameter.


### -param strResultRole [optional]

String that contains a property name. If specified, this parameter indicates that the returned endpoints must play a particular role in their association with the source object. The role is defined by the name of a specified property (which must be a reference property) of an association.


### -param strRole [optional]

String that contains a property name. If specified, this parameter indicates that the returned endpoints must participate in an association with the source object in which the source object plays a particular role. The role is defined by the name of a specified property (which must be a reference property) of an association.


### -param bClassesOnly [optional]

Boolean value that indicates whether a list of class names should be returned rather than actual instances of the classes. These are the classes to which the endpoint instances belong. The default value for this parameter is <b>FALSE</b>.


### -param bSchemaOnly [optional]

Boolean value that indicates whether the query applies to the schema rather than the data. The default value for this parameter is <b>FALSE</b>. It can only be set to <b>TRUE</b> if the <i>strObjectPath</i> parameter specifies the object path of a class. When set to <b>TRUE</b>, the set of returned endpoints represent classes that are suitably associated with the source class in schema.


### -param strRequiredAssocQualifier [optional]

String that contains a qualifier name. If specified, this parameter indicates that the returned endpoints must be associated with the source object through an association class that includes the specified qualifier.


### -param strRequiredQualifier [optional]

String that contains a qualifier name. If specified, this parameter indicates that the returned endpoints must include the specified qualifier.


### -param iFlags [optional]

Integer that specifies additional flags to the operation. The default value for this parameter is <b>wbemFlagReturnImmediately</b>, which calls the method in the semisynchronous mode. This parameter can accept the following values.



#### wbemFlagForwardOnly (32 (0x20))

Causes a forward-only enumerator to be returned. Forward-only enumerators are generally much faster and use less memory than conventional enumerators, but they do not allow calls to 
<a href="https://msdn.microsoft.com/d0773c94-30b5-4217-8a9a-0bceb9e75f02">SWbemObject.Clone_</a>.



#### wbemFlagBidirectional (0 (0x0))

Causes WMI to retain pointers to objects of the enumeration until the client releases the enumerator.



#### wbemFlagReturnImmediately (16 (0x10))

Causes the call to return immediately.



#### wbemFlagReturnWhenComplete (0 (0x0))

Causes this call to block until the query has completed. This flag calls the method in synchronous mode.



#### wbemFlagUseAmendedQualifiers (131072 (0x20000))

Causes WMI to return class amendment data along with the base class definition. 

       For more information, see <a href="https://msdn.microsoft.com/01e1cee5-d882-45b6-ac93-68533c2c6c9d">Localizing WMI Class Information</a>.


### -param objWbemNamedValueSet




### -param objWbemObjectSet






#### - objwbemNamedValueSet [optional]

Typically, this is undefined. Otherwise, this is an 
<a href="https://msdn.microsoft.com/7d1c3a28-d0d3-4108-9628-74ad483e328e">SWbemNamedValueSet</a> object whose elements represent the context information that can be used by the provider that is servicing the request. A provider that supports or requires such information must document the recognized value names, data type of the value, allowed values, and semantics.


## -returns



If the call is successful, an 
<a href="https://msdn.microsoft.com/00f5317e-eb8e-42f9-bada-963e11aadda4">SWbemObjectSet</a> object is returned.




## -remarks



The method retrieves the instances of managed resources that are associated with a specified resource through one or more association classes. You provide the object path for the originating endpoint, and AssociatorsOf returns the managed resources at the opposite endpoint. The AssociatorsOf method performs the same function that the ASSOCIATORS OF WQL query performs.

For more information about the ASSOCIATORS OF WQL query, source instances, and endpoints, see 
<a href="https://msdn.microsoft.com/d6bd9643-523d-4d81-8bf1-da52ccc7524d">ASSOCIATORS OF Statement</a>.




## -see-also




<a href="https://msdn.microsoft.com/c71e11cd-39a5-40d8-b279-f5ee9ff3ae04">SWbemObject.AssociatorsAsync_</a>



<a href="https://msdn.microsoft.com/79f01853-c649-4cbe-b2fa-cff38fb4b733">SWbemObject.Associators_</a>



<a href="https://msdn.microsoft.com/ba02da47-0bb2-40e1-af50-1c42b4be2abd">SWbemObject.References_</a>



<a href="https://msdn.microsoft.com/7fcfa404-2fe6-42e5-85ac-64536f6d2a44">SWbemServices</a>



<a href="https://msdn.microsoft.com/3969d90f-d39c-40f1-9328-fc1afbaa53b1">SWbemServices.AssociatorsOfAsync</a>



<a href="https://msdn.microsoft.com/33425b1c-13f5-4c3d-8f8a-2922f3e95264">SWbemServices.ReferencesTo</a>
 

 

