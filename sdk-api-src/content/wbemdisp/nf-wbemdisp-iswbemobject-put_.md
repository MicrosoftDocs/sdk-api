---
UID: NF:wbemdisp.ISWbemObject.Put_
title: ISWbemObject::Put_
author: windows-sdk-content
description: The Put_ method of SWbemObject creates or updates an instance or a class object to Windows Management Instrumentation (WMI). You can use this method after you modify any properties or methods in an SWbemObject, and your changes are written to WMI.
old-location: wmi\swbemobject_put_.htm
old-project: WmiSdk
ms.assetid: c636ff95-9f3e-4ba9-adf3-30b981be02a4
ms.author: windowssdkdev
ms.date: 08/03/2018
ms.keywords: ISWbemObject interface [Windows Management Instrumentation],Put_ method, ISWbemObject.Put_, ISWbemObject::Put_, Put_, Put_ method [Windows Management Instrumentation], Put_ method [Windows Management Instrumentation],ISWbemObject interface, Put_ method [Windows Management Instrumentation],SWbemObject object, SWbemObject object [Windows Management Instrumentation],Put_ method, SWbemObject.Put_, WbemChangeFlagUpdateForceMode, _hmm_swbemobject.put_, wbemChangeFlagCreateOnly, wbemChangeFlagCreateOrUpdate, wbemChangeFlagUpdateCompatible, wbemChangeFlagUpdateOnly, wbemChangeFlagUpdateSafeMode, wbemFlagReturnImmediately, wbemFlagReturnWhenComplete, wbemFlagUseAmendedQualifiers, wmi.swbemobject_put_
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
 - SWbemObject.Put_
 - ISWbemObject.Put_
 - ISWbemObject.Put_
product: Windows
targetos: Windows
req.lib: 
req.dll: Wbemdisp.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# ISWbemObject::Put_


## -description


The 
<b>Put_</b> method of <a href="https://msdn.microsoft.com/d303ec1a-5e0c-4a5e-8ed3-ed353a138755">SWbemObject</a> creates or updates an instance or a class object to Windows Management Instrumentation (WMI). You can use this method after you modify any properties or methods in an 
<b>SWbemObject</b>, and your changes are written to WMI.

For an explanation of this syntax, see 
<a href="https://msdn.microsoft.com/889e6322-96f6-4a24-a084-e3b7bfa94a40">Document Conventions for the Scripting API</a>.


## -parameters




### -param iFlags [in, optional]

This parameter determines if the call creates or updates the class or instance and if the call returns immediately. This parameter can accept the following values.



#### wbemChangeFlagUpdateCompatible (0 (0x0))

Allows a class to be updated if there are no derived classes and there are no instances for that class. It also allows updates in all cases if the change is just to unimportant qualifiers (for example, the <b>Description</b> qualifier). This is the default behavior for this call and is used for compatibility with previous versions of WMI. If the class has instances the update fails.



#### wbemChangeFlagUpdateSafeMode (32 (0x20))

Allows updates of classes even if there are child classes if the change does not cause any conflicts with child classes. You can use this flag when adding a new property to a base class that was not previously mentioned in any of the child classes. If the class has instances the update fails. If the class has instances the update fails.



#### WbemChangeFlagUpdateForceMode (64 (0x40))

This flag forces updates of classes when conflicting child classes exist. For example, this flag will force an update if a class qualifier was defined in a child class, and the base class tries to add the same qualifier and in conflict with the existing one. In force mode this conflict would be resolved by deleting the conflicting qualifier in the child class. If the class has instances the update will fail.

Using force mode to update a static class results in the deletion of all instances of that class. A forced update on a provider class does not delete instances of the class.



#### wbemChangeFlagCreateOrUpdate (0 (0x0))

Causes the class or instance to be created if it does not exist or overwritten if it exists already.



#### wbemChangeFlagCreateOnly (2 (0x2))

Used for creation only. The call fails if the class or instance already exists.



#### wbemChangeFlagUpdateOnly (1 (0x1))

Causes this call to update. The class or instance must exist for the call to be successful.



#### wbemFlagReturnImmediately (16 (0x10))

Causes the call to return immediately.



#### wbemFlagReturnWhenComplete (0 (0x0))

Causes this call to block until the query has completed.



#### wbemFlagUseAmendedQualifiers (131072 (0x20000))

Causes WMI to write class amendment data as well as the base class definition. 
For more information about amended qualifiers, see <a href="https://msdn.microsoft.com/01e1cee5-d882-45b6-ac93-68533c2c6c9d">Localizing WMI Class Information</a>.


### -param objWbemNamedValueSet




### -param objWbemObjectPath






#### - objwbemNamedValueSet [in, optional]

Typically, this is undefined. Otherwise, this is an 
<a href="https://msdn.microsoft.com/f2cf489d-d2a9-4926-84cf-fb33fe3d726a">SWbemObjectPath</a> object whose elements represent the context information that can be used by the provider that is servicing the request. A provider that supports or requires such information must document the recognized value names, data type of the value, allowed values, and semantics.


## -returns



If the call is successful, an 
<a href="https://msdn.microsoft.com/f2cf489d-d2a9-4926-84cf-fb33fe3d726a">SWbemObjectPath</a> object is returned. This object contains the object path of the instance or class that has been successfully committed to WMI.




## -see-also




<a href="https://msdn.microsoft.com/d303ec1a-5e0c-4a5e-8ed3-ed353a138755">SWbemObject</a>



<a href="https://msdn.microsoft.com/60123963-31be-4112-9d06-611b4c599fd4">SWbemObjectPath.Class</a>



<a href="https://msdn.microsoft.com/2ddcfffa-a7b4-4fd6-926d-411de27f6212">SWbemProperty</a>



<a href="https://msdn.microsoft.com/b5dbe98a-e1d8-4679-a563-c88760d08b79">SWbemQualifier</a>
 

 

