---
UID: NF:wbemcli.IWbemClassObject.GetQualifierSet
title: IWbemClassObject::GetQualifierSet method
author: windows-driver-content
description: The IWbemClassObject::GetQualifierSet method returns an interface pointer that allows read and write operations on the set of qualifiers for the entire class object, whether the object is an instance or a class definition.
old-location: wmi\iwbemclassobject_getqualifierset.htm
old-project: WmiSdk
ms.assetid: da86b723-8126-44b9-95ec-120d88390ef3
ms.author: windowsdriverdev
ms.date: 4/11/2018
ms.keywords: GetQualifierSet method [Windows Management Instrumentation], GetQualifierSet method [Windows Management Instrumentation], IWbemClassObject interface, GetQualifierSet,IWbemClassObject.GetQualifierSet, IWbemClassObject, IWbemClassObject interface [Windows Management Instrumentation], GetQualifierSet method, IWbemClassObject::GetQualifierSet, _hmm_iwbemclassobject_getqualifierset, wbemcli/IWbemClassObject::GetQualifierSet, wmi.iwbemclassobject_getqualifierset
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
req.typenames: WMI_OBJ_TEXT
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	CIMWin32.dll
-	Esscli.dll
-	Fastprox.dll
-	FrameDyn.dll
-	FrameDynOS.dll
-	Krnlprov.dll
-	Ncprov.dll
-	Wbemcore.dll
-	Wbemess.dll
-	Wmipiprt.dll
api_name:
-	IWbemClassObject.GetQualifierSet
product: Windows
targetos: Windows
req.lib: WbemUuid.lib
req.dll: CIMWin32.dll; Esscli.dll; Fastprox.dll; FrameDyn.dll; FrameDynOS.dll; Krnlprov.dll; Ncprov.dll; Wbemcore.dll; Wbemess.dll; Wmipiprt.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# IWbemClassObject::GetQualifierSet method


## -description


The 
<b>IWbemClassObject::GetQualifierSet</b> method returns an interface pointer that allows read and write operations on the set of qualifiers for the entire class object, whether the object is an instance or a class definition. Any qualifiers added, deleted, or edited using the returned pointer apply to the entire instance or class definition.


## -parameters




### -param ppQualSet [out]

Receives the interface pointer that allows access to the qualifiers for the class object. The returned object has a positive reference count upon return from the call. The caller must call <b>IWbemQualifierSet::Release</b> when the object is no longer needed. This parameter cannot be <b>NULL</b>. On error, a new object is not returned and the pointer is left unmodified.


## -returns



This method returns an <b>HRESULT</b> indicating the status of the method call. The following list lists the value contained within an <b>HRESULT</b>. For general <b>HRESULT</b> values, see <a href="https://msdn.microsoft.com/4a3a8feb-a05f-4614-8f04-1f507da7e5b7">System Error Codes</a>.




## -see-also




<a href="https://msdn.microsoft.com/a3ce37d7-5580-4b84-9119-78412c8e0d27">IWbemClassObject</a>



<a href="https://msdn.microsoft.com/4bfca42e-7688-42e1-afa3-24b7eaaad9fe">IWbemClassObject::GetPropertyQualifierSet</a>



<a href="https://msdn.microsoft.com/8b36bd32-4931-4641-a019-cbaa3547edd0">IWbemQualifierSet</a>
 

 

