---
UID: NF:wbemcli.IWbemClassObject.SpawnDerivedClass
title: IWbemClassObject::SpawnDerivedClass
author: windows-sdk-content
description: Use the IWbemClassObject::SpawnDerivedClass method to create a newly derived class object from the current object.
old-location: wmi\iwbemclassobject_spawnderivedclass.htm
tech.root: WmiSdk
ms.assetid: 9b27c984-2261-4263-a32e-977aba5e3f06
ms.author: windowssdkdev
ms.date: 09/27/2018
ms.keywords: IWbemClassObject interface [Windows Management Instrumentation],SpawnDerivedClass method, IWbemClassObject.SpawnDerivedClass, IWbemClassObject::SpawnDerivedClass, SpawnDerivedClass, SpawnDerivedClass method [Windows Management Instrumentation], SpawnDerivedClass method [Windows Management Instrumentation],IWbemClassObject interface, _hmm_iwbemclassobject_spawnderivedclass, wbemcli/IWbemClassObject::SpawnDerivedClass, wmi.iwbemclassobject_spawnderivedclass
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: wbemcli.h
req.include-header: Wbemidl.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: WbemCli.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: WbemUuid.lib
req.dll: CIMWin32.dll; Esscli.dll; Fastprox.dll; FrameDyn.dll; FrameDynOS.dll; Krnlprov.dll; Ncprov.dll; Wbemcore.dll; Wbemess.dll; Wmipiprt.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - CIMWin32.dll
 - Esscli.dll
 - Fastprox.dll
 - FrameDyn.dll
 - FrameDynOS.dll
 - Krnlprov.dll
 - Ncprov.dll
 - Wbemcore.dll
 - Wbemess.dll
 - Wmipiprt.dll
api_name:
 - IWbemClassObject.SpawnDerivedClass
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IWbemClassObject::SpawnDerivedClass


## -description


Use the 
<b>IWbemClassObject::SpawnDerivedClass</b> method to create a newly derived class object from the current object. The current object must be a class definition that becomes the parent class of the spawned object. The returned object becomes a subclass of the current object.


## -parameters




### -param lFlags [in]

Reserved. This parameter must be 0.


### -param ppNewClass [out]

Cannot be <b>NULL</b>. This receives the pointer to the new class definition object. The caller must invoke <b>IWbemClassObject::Release</b> when the object is no longer required, typically after you have invoked 
<a href="https://msdn.microsoft.com/fcb8694e-6bf1-426d-bc1d-18cf9925f1e0">IWbemServices::PutClass</a> to write the class definition. On error, a new object is not returned, and <i>ppNewClass</i> is left unmodified.


## -returns



This method returns an <b>HRESULT</b> indicating the status of the method call. The following list lists the value contained within an <b>HRESULT</b>. For general <b>HRESULT</b> values, see <a href="https://msdn.microsoft.com/4a3a8feb-a05f-4614-8f04-1f507da7e5b7">System Error Codes</a>.




## -remarks



The new object returned in <i>ppNewClass</i> automatically becomes a subclass of the current object. This behavior cannot be overridden. There is no other method by which subclasses (derived classes) can be created.

You cannot create a derived class from a class that is local to your own client process. The parent class (base class) must be created and registered with Windows Management using 
<a href="https://msdn.microsoft.com/fcb8694e-6bf1-426d-bc1d-18cf9925f1e0">IWbemServices::PutClass</a>, and then retrieved using 
<a href="https://msdn.microsoft.com/68150273-c4ec-46f1-a3e6-d7169824b69d">IWbemServices::GetObject</a> before this method can be used to create a derived class.

To create a class hierarchy, you must create the initial class with 
<a href="https://msdn.microsoft.com/fcb8694e-6bf1-426d-bc1d-18cf9925f1e0">IWbemServices::PutClass</a>, retrieve it using 
<a href="https://msdn.microsoft.com/68150273-c4ec-46f1-a3e6-d7169824b69d">IWbemServices::GetObject</a>, and use the retrieved object to create the newly derived class. Then, this newly derived class must be created using 
<b>IWbemServices::PutClass</b>. To create other derived classes, you must call 
<b>IWbemServices::GetObject</b>, then call 
<b>IWbemClassObject::SpawnDerivedClass</b>, and so on, in a cycle for each new derivation level. You must follow this procedure to prevent version errors and concurrency conflicts. For more information about creating a class with no parent, see 
<a href="https://msdn.microsoft.com/06b75910-f126-48b6-8e43-4a9ed4661732">Creating a Class</a>.




## -see-also




<a href="https://msdn.microsoft.com/a3ce37d7-5580-4b84-9119-78412c8e0d27">IWbemClassObject</a>



<a href="https://msdn.microsoft.com/68150273-c4ec-46f1-a3e6-d7169824b69d">IWbemServices::GetObject</a>



<a href="https://msdn.microsoft.com/fcb8694e-6bf1-426d-bc1d-18cf9925f1e0">IWbemServices::PutClass</a>
 

 

