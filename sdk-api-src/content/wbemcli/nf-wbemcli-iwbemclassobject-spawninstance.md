---
UID: NF:wbemcli.IWbemClassObject.SpawnInstance
title: IWbemClassObject::SpawnInstance
author: windows-sdk-content
description: Use the IWbemClassObject::SpawnInstance method to create a new instance of a class.
old-location: wmi\iwbemclassobject_spawninstance.htm
tech.root: WmiSdk
ms.assetid: 3f244c1b-60ed-41ff-8464-5ac66737a5da
ms.author: windowssdkdev
ms.date: 10/09/2018
ms.keywords: IWbemClassObject interface [Windows Management Instrumentation],SpawnInstance method, IWbemClassObject.SpawnInstance, IWbemClassObject::SpawnInstance, SpawnInstance, SpawnInstance method [Windows Management Instrumentation], SpawnInstance method [Windows Management Instrumentation],IWbemClassObject interface, _hmm_iwbemclassobject_spawninstance, wbemcli/IWbemClassObject::SpawnInstance, wmi.iwbemclassobject_spawninstance
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
 - IWbemClassObject.SpawnInstance
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IWbemClassObject::SpawnInstance


## -description


Use the 
<b>IWbemClassObject::SpawnInstance</b> method to create a new instance of a class. The current object must be a class definition obtained from Windows Management using 
<a href="https://msdn.microsoft.com/68150273-c4ec-46f1-a3e6-d7169824b69d">IWbemServices::GetObject</a>, 
<a href="https://msdn.microsoft.com/23122b38-5671-4454-be79-85c6bc34daa0">IWbemServices::CreateClassEnum</a>, or 
<a href="https://msdn.microsoft.com/02b81f48-c6a0-44db-86b9-936331b15cc4">IWbemServices::CreateClassEnumAsync</a> Then, use this class definition to create new instances.

A call to 
<a href="https://msdn.microsoft.com/1e07b328-40f7-4e14-bf53-9a5cebfc23f6">IWbemServices::PutInstance</a> is required to actually write the instance to Windows Management. If you intend to discard the object before calling 
<b>IWbemServices::PutInstance</b>, simply make a call to <b>IWbemClassObject::Release</b>.

Note that spawning an instance from an instance is supported but the returned instance will be empty.


## -parameters




### -param lFlags [in]

Reserved. This parameter must be 0.


### -param ppNewInstance [out]

Cannot be <b>NULL</b>. It receives a new instance of the class. The caller must invoke <b>IWbemClassObject::Release</b> when the pointer is no longer required. On error, a new object is not returned and the pointer is left unmodified.


## -returns



This method returns an <b>HRESULT</b> indicating the status of the method call. The following list lists the value contained within an <b>HRESULT</b>. For general <b>HRESULT</b> values, see <a href="https://msdn.microsoft.com/4a3a8feb-a05f-4614-8f04-1f507da7e5b7">System Error Codes</a>.




## -see-also




<a href="https://msdn.microsoft.com/a3ce37d7-5580-4b84-9119-78412c8e0d27">IWbemClassObject</a>



<a href="https://msdn.microsoft.com/68150273-c4ec-46f1-a3e6-d7169824b69d">IWbemServices::GetObject</a>



<a href="https://msdn.microsoft.com/1e07b328-40f7-4e14-bf53-9a5cebfc23f6">IWbemServices::PutInstance</a>
 

 

