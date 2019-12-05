---
UID: NF:wbemcli.IWbemClassObject.SpawnInstance
title: IWbemClassObject::SpawnInstance (wbemcli.h)
description: Use the IWbemClassObject::SpawnInstance method to create a new instance of a class.
old-location: wmi\iwbemclassobject_spawninstance.htm
tech.root: WmiSdk
ms.assetid: 3f244c1b-60ed-41ff-8464-5ac66737a5da
ms.date: 12/05/2018
ms.keywords: IWbemClassObject interface [Windows Management Instrumentation],SpawnInstance method, IWbemClassObject.SpawnInstance, IWbemClassObject::SpawnInstance, SpawnInstance, SpawnInstance method [Windows Management Instrumentation], SpawnInstance method [Windows Management Instrumentation],IWbemClassObject interface, _hmm_iwbemclassobject_spawninstance, wbemcli/IWbemClassObject::SpawnInstance, wmi.iwbemclassobject_spawninstance
ms.topic: method
f1_keywords:
- wbemcli/IWbemClassObject.SpawnInstance
dev_langs:
- c++
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IWbemClassObject::SpawnInstance


## -description


Use the 
<b>IWbemClassObject::SpawnInstance</b> method to create a new instance of a class. The current object must be a class definition obtained from Windows Management using 
<a href="https://docs.microsoft.com/windows/desktop/api/wbemcli/nf-wbemcli-iwbemservices-getobject">IWbemServices::GetObject</a>, 
<a href="https://docs.microsoft.com/windows/desktop/api/wbemcli/nf-wbemcli-iwbemservices-createclassenum">IWbemServices::CreateClassEnum</a>, or 
<a href="https://docs.microsoft.com/windows/desktop/api/wbemcli/nf-wbemcli-iwbemservices-createclassenumasync">IWbemServices::CreateClassEnumAsync</a> Then, use this class definition to create new instances.

A call to 
<a href="https://docs.microsoft.com/windows/desktop/api/wbemcli/nf-wbemcli-iwbemservices-putinstance">IWbemServices::PutInstance</a> is required to actually write the instance to Windows Management. If you intend to discard the object before calling 
<b>IWbemServices::PutInstance</b>, simply make a call to <b>IWbemClassObject::Release</b>.

Note that spawning an instance from an instance is supported but the returned instance will be empty.


## -parameters




### -param lFlags [in]

Reserved. This parameter must be 0.


### -param ppNewInstance [out]

Cannot be <b>NULL</b>. It receives a new instance of the class. The caller must invoke <b>IWbemClassObject::Release</b> when the pointer is no longer required. On error, a new object is not returned and the pointer is left unmodified.


## -returns



This method returns an <b>HRESULT</b> indicating the status of the method call. The following list lists the value contained within an <b>HRESULT</b>. For general <b>HRESULT</b> values, see <a href="https://docs.microsoft.com/windows/desktop/Debug/system-error-codes">System Error Codes</a>.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/wbemcli/nn-wbemcli-iwbemclassobject">IWbemClassObject</a>



<a href="https://docs.microsoft.com/windows/desktop/api/wbemcli/nf-wbemcli-iwbemservices-getobject">IWbemServices::GetObject</a>



<a href="https://docs.microsoft.com/windows/desktop/api/wbemcli/nf-wbemcli-iwbemservices-putinstance">IWbemServices::PutInstance</a>
 

 

