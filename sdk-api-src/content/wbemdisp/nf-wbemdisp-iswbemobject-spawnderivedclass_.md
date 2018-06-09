---
UID: NF:wbemdisp.ISWbemObject.SpawnDerivedClass_
title: ISWbemObject::SpawnDerivedClass_
author: windows-sdk-content
description: Use the SpawnDerivedClass_ method of the SWbemObject object to create a derived class object from the current object. The object must be a class definition that becomes the parent class of the spawned object.
old-location: wmi\swbemobject_spawnderivedclass_.htm
old-project: WmiSdk
ms.assetid: 1b5aaea7-50f4-40bd-ab2a-f4ff55cc22fc
ms.author: windowssdkdev
ms.date: 06/07/2018
ms.keywords: ISWbemObject interface [Windows Management Instrumentation],SpawnDerivedClass_ method, ISWbemObject.SpawnDerivedClass_, ISWbemObject::SpawnDerivedClass_, SWbemObject object [Windows Management Instrumentation],SpawnDerivedClass_ method, SWbemObject.SpawnDerivedClass_, SpawnDerivedClass_, SpawnDerivedClass_ method [Windows Management Instrumentation], SpawnDerivedClass_ method [Windows Management Instrumentation],ISWbemObject interface, SpawnDerivedClass_ method [Windows Management Instrumentation],SWbemObject object, _hmm_swbemobject.spawnderivedclass_, wmi.swbemobject_spawnderivedclass_
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
 - SWbemObject.SpawnDerivedClass_
 - ISWbemObject.SpawnDerivedClass_
 - ISWbemObject.SpawnDerivedClass_
product: Windows
targetos: Windows
req.lib: 
req.dll: Wbemdisp.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# ISWbemObject::SpawnDerivedClass_


## -description


Use the 
<b>SpawnDerivedClass_</b> method of the 
<a href="https://msdn.microsoft.com/d303ec1a-5e0c-4a5e-8ed3-ed353a138755">SWbemObject</a> object to create a derived class object from the current object. The object must be a class definition that becomes the parent class of the spawned object.

For an explanation of this syntax, see 
<a href="https://msdn.microsoft.com/889e6322-96f6-4a24-a084-e3b7bfa94a40">Document Conventions for the Scripting API</a>.


## -parameters




### -param iFlags [optional]

Reserved and must be 0 (zero) if specified.


### -param objWbemObject






## -returns



If the call is successful, the 
<a href="https://msdn.microsoft.com/d303ec1a-5e0c-4a5e-8ed3-ed353a138755">SWbemObject</a> object contains the new class definition object. No object returns when there is an error.




## -remarks



The object that is returned automatically becomes a subclass of the current object. This behavior cannot be overridden. There is no other method by which you can create derived classes.

You cannot create a derived class from a class that is local to your own client process. Before use this method to create a derived class, you must create the base class. To create the base class, call 
<a href="https://msdn.microsoft.com/c636ff95-9f3e-4ba9-adf3-30b981be02a4">SWbemObject.Put_</a>, and retrieve the base class using 
<a href="https://msdn.microsoft.com/3071aeb2-adab-47aa-a10c-9796766bb630">SWbemServices.Get</a>.



