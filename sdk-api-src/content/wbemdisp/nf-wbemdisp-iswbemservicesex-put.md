---
UID: NF:wbemdisp.ISWbemServicesEx.Put
title: ISWbemServicesEx::Put
author: windows-sdk-content
description: Returns an SWbemObjectPath object that contains the path of the object to which the data was written.
old-location: wmi\swbemservicesex_put.htm
old-project: WmiSdk
ms.assetid: 1a9a718d-875d-4102-9d9d-3d10be162f58
ms.author: windowssdkdev
ms.date: 06/07/2018
ms.keywords: ISWbemServicesEx interface [Windows Management Instrumentation],Put method, ISWbemServicesEx.Put, ISWbemServicesEx::Put, Put, Put method [Windows Management Instrumentation], Put method [Windows Management Instrumentation],ISWbemServicesEx interface, Put method [Windows Management Instrumentation],SWbemServicesEx object, SWbemServicesEx object [Windows Management Instrumentation],Put method, SWbemServicesEx.Put, _hmm_swbemservicesex.put, wbemChangeFlagCreateOnly, wbemChangeFlagCreateOrUpdate, wbemChangeFlagUpdateCompatible, wbemChangeFlagUpdateForceMode, wbemChangeFlagUpdateOnly, wbemChangeFlagUpdateSafeMode, wbemFlagReturnImmediately, wbemFlagReturnWhenComplete, wbemFlagUseAmendedQualifiers, wmi.swbemservicesex_put
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
 - SWbemServicesEx.Put
 - ISWbemServicesEx.Put
 - ISWbemServicesEx.Put
product: Windows
targetos: Windows
req.lib: 
req.dll: Wbemdisp.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# ISWbemServicesEx::Put


## -description


The 
<b>Put</b> method of the 
<a href="https://msdn.microsoft.com/def514a9-eca4-41de-87cd-c9f964a71f68">SWbemServicesEx</a> object saves the object to the namespace bound to the 
 object and returns an 
<a href="https://msdn.microsoft.com/f2cf489d-d2a9-4926-84cf-fb33fe3d726a">SWbemObjectPath</a> object that contains the path of the object to which the data was written.

This method is called in the semisynchronous mode. For more information, see <a href="https://msdn.microsoft.com/7a1eda93-014e-4067-b6d0-361a3d2fd1df">Calling a Method</a>.

For an explanation of this syntax, see 
<a href="https://msdn.microsoft.com/889e6322-96f6-4a24-a084-e3b7bfa94a40">Document Conventions for the Scripting API</a>.


## -parameters




### -param objWbemObject

Required. The new object to be put in the namespace. This can be either a newly created object or a modified object.


### -param iFlags [optional]

This parameter determines if the call creates or updates the object and if the call returns immediately. This parameter can accept the following values.



#### wbemChangeFlagUpdateCompatible (0 (0x0))

Allows a class to be updated if there are no derived classes and there are no instances for that class. It also allows updates in all cases if the change is only to unimportant qualifiers (for example, the <b>Description</b> qualifier). This is the default behavior for this call and is used for compatibility with previous versions of WMI. If the class has instances, the update fails.



#### wbemChangeFlagUpdateSafeMode (32 (0x20))

Allows updates of classes even if there are child classes, when the change does not cause any conflicts with child classes. You can use this flag when adding a new property to a base class that was not previously mentioned in any of the child classes. If the class has instances, the update fails.



#### wbemChangeFlagUpdateForceMode (64 (0x40))

This flag forces updates of classes when conflicting child classes exist. For example, this flag  forces an update if a class qualifier was defined in a child class, and the base class tries to add the same qualifier in conflict with the existing one. In the force mode, this conflict is resolved by deleting the conflicting qualifier in the child class. If the class has instances, the update  fails.

The use of the force mode to update a static class causes the deletion of all instances of that class. A forced update on a provider class does not delete instances of the class.



#### wbemChangeFlagCreateOrUpdate (0 (0x0))

Causes the class or instance to be created if it does not exist, or overwritten if it already exists.



#### wbemChangeFlagCreateOnly (2 (0x2))

Used for creation only. The call fails if the class or instance already exists.



#### wbemChangeFlagUpdateOnly (1 (0x1))

Causes this call to only do an update. The class or instance must exist for the call to be successful.



#### wbemFlagReturnImmediately (16 (0x10))

Causes the call to return immediately.



#### wbemFlagReturnWhenComplete (0 (0x0))

Causes this call to block until the operation has completed. This flag calls the method in the synchronous mode.



#### wbemFlagUseAmendedQualifiers (131072 (0x20000))

Causes WMI to write class amendment data as well as the base class definition. For more information, see 
<a href="https://msdn.microsoft.com/01e1cee5-d882-45b6-ac93-68533c2c6c9d">Localizing WMI Class Information</a>.


### -param objWbemNamedValueSet [optional]

Typically, this is undefined. Otherwise, this is an 
<a href="https://msdn.microsoft.com/7d1c3a28-d0d3-4108-9628-74ad483e328e">SWbemNamedValueSet</a> object whose elements represent the context information that can be used by the provider that  services the request. A provider that supports or requires such information must document the recognized value names, data type of the value, allowed values, and semantics.


### -param objWbemObjectPath






## -returns



If the call is successful, an 
<a href="https://msdn.microsoft.com/f2cf489d-d2a9-4926-84cf-fb33fe3d726a">SWbemObjectPath</a> object is returned. This object contains the object path of the instance or class that has been successfully committed to WMI.



