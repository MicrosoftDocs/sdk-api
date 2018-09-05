---
UID: NF:wbemdisp.ISWbemObject.Clone_
title: ISWbemObject::Clone_
author: windows-sdk-content
description: The Clone_ method of the SWbemObject object returns a new object that is a clone of the current object.
old-location: wmi\swbemobject_clone_.htm
old-project: WmiSdk
ms.assetid: d0773c94-30b5-4217-8a9a-0bceb9e75f02
ms.author: windowssdkdev
ms.date: 08/28/2018
ms.keywords: Clone_, Clone_ method [Windows Management Instrumentation], Clone_ method [Windows Management Instrumentation],ISWbemObject interface, Clone_ method [Windows Management Instrumentation],SWbemObject object, ISWbemObject interface [Windows Management Instrumentation],Clone_ method, ISWbemObject.Clone_, ISWbemObject::Clone_, SWbemObject object [Windows Management Instrumentation],Clone_ method, SWbemObject.Clone_, _hmm_swbemobject.clone_, wmi.swbemobject_clone_
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
 - SWbemObject.Clone_
 - ISWbemObject.Clone_
 - ISWbemObject.Clone_
product: Windows
targetos: Windows
req.lib: 
req.dll: Wbemdisp.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# ISWbemObject::Clone_


## -description


The 
<b>Clone_</b> method of the 
<a href="https://msdn.microsoft.com/d303ec1a-5e0c-4a5e-8ed3-ed353a138755">SWbemObject</a> object returns a new object that is a clone of the current object.

For an explanation of this syntax, see 
<a href="https://msdn.microsoft.com/889e6322-96f6-4a24-a084-e3b7bfa94a40">Document Conventions for the Scripting API</a>.


## -parameters




### -param objWbemObject






## -returns



If successful, this method returns a new 
<a href="https://msdn.microsoft.com/d303ec1a-5e0c-4a5e-8ed3-ed353a138755">SWbemObject</a> object.




## -remarks



Use the 
<b>Clone_</b> method to duplicate a class definition or an instance. This is useful when you need the original copy of the object for backup purposes while you are modifying a new copy. Likewise, use this method to create many new instances from a single source instance. For example, use 
<a href="https://msdn.microsoft.com/4761bdb2-455a-48c4-9e22-bfba6a1036ec">SWbemObject.SpawnInstance_</a> to create a single starting instance, and use <b>SWbemObject.Clone_</b> to produce 100 copies of the instance quickly. Subsequently, you can modify the objects, giving each one specific values.

It is not possible to use this method to convert a class definition to an instance, or to convert an instance to a class definition.



