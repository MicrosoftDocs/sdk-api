---
UID: NF:wbemdisp.ISWbemObject.SpawnInstance_
title: ISWbemObject::SpawnInstance_
author: windows-sdk-content
description: Use the SpawnInstance_ method of the SWbemObject object to create a new instance of a class.
old-location: wmi\swbemobject_spawninstance_.htm
old-project: WmiSdk
ms.assetid: 4761bdb2-455a-48c4-9e22-bfba6a1036ec
ms.author: windowssdkdev
ms.date: 08/03/2018
ms.keywords: ISWbemObject interface [Windows Management Instrumentation],SpawnInstance_ method, ISWbemObject.SpawnInstance_, ISWbemObject::SpawnInstance_, SWbemObject object [Windows Management Instrumentation],SpawnInstance_ method, SWbemObject.SpawnInstance_, SpawnInstance_, SpawnInstance_ method [Windows Management Instrumentation], SpawnInstance_ method [Windows Management Instrumentation],ISWbemObject interface, SpawnInstance_ method [Windows Management Instrumentation],SWbemObject object, _hmm_swbemobject.spawninstance_, wmi.swbemobject_spawninstance_
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
 - SWbemObject.SpawnInstance_
 - ISWbemObject.SpawnInstance_
 - ISWbemObject.SpawnInstance_
product: Windows
targetos: Windows
req.lib: 
req.dll: Wbemdisp.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# ISWbemObject::SpawnInstance_


## -description


Use the 
<b>SpawnInstance_</b> method of the 
<a href="https://msdn.microsoft.com/d303ec1a-5e0c-4a5e-8ed3-ed353a138755">SWbemObject</a> object to create a new instance of a class. The current object must be a class definition obtained from WMI via a method such as 
<a href="https://msdn.microsoft.com/3071aeb2-adab-47aa-a10c-9796766bb630">SWbemServices.Get</a> or 
<a href="https://msdn.microsoft.com/06b9d4c9-cd72-49b2-92b0-d18d94dfbd9f">SWbemServices.ExecQuery</a>. Then, use this class definition to create new instances. Create each new instance locally within the process, and then call 
<a href="https://msdn.microsoft.com/c636ff95-9f3e-4ba9-adf3-30b981be02a4">SWbemObject.Put_</a> to actually create the instance within WMI.
<div class="alert"><b>Note</b>  Spawning an instance from an instance is supported, but the returned instance is empty.</div><div> </div>For an explanation of this syntax, see 
<a href="https://msdn.microsoft.com/889e6322-96f6-4a24-a084-e3b7bfa94a40">Document Conventions for the Scripting API</a>.


## -parameters




### -param iFlags [in, optional]

Reserved and must be zero if specified.


### -param objWbemObject






## -returns



If successful, this call returns an 
<a href="https://msdn.microsoft.com/d303ec1a-5e0c-4a5e-8ed3-ed353a138755">SWbemObject</a> object that contains a new instance of the class.




## -see-also




<a href="https://msdn.microsoft.com/d303ec1a-5e0c-4a5e-8ed3-ed353a138755">SWbemObject</a>



<a href="https://msdn.microsoft.com/c636ff95-9f3e-4ba9-adf3-30b981be02a4">SWbemObject.Put_</a>



<a href="https://msdn.microsoft.com/3071aeb2-adab-47aa-a10c-9796766bb630">SWbemServices.Get</a>
 

 

