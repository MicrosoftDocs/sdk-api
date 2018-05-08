---
UID: NF:wbemcli.IWbemClassObject.GetPropertyQualifierSet
title: IWbemClassObject::GetPropertyQualifierSet
author: windows-driver-content
description: The IWbemClassObject::GetPropertyQualifierSet method gets the qualifier set for a particular property in the class object. You can use this method with properties that are a member of an instance or a class definition.
old-location: wmi\iwbemclassobject_getpropertyqualifierset.htm
old-project: WmiSdk
ms.assetid: 4bfca42e-7688-42e1-afa3-24b7eaaad9fe
ms.author: windowsdriverdev
ms.date: 4/11/2018
ms.keywords: GetPropertyQualifierSet, GetPropertyQualifierSet method [Windows Management Instrumentation], GetPropertyQualifierSet method [Windows Management Instrumentation],IWbemClassObject interface, IWbemClassObject interface [Windows Management Instrumentation],GetPropertyQualifierSet method, IWbemClassObject.GetPropertyQualifierSet, IWbemClassObject::GetPropertyQualifierSet, _hmm_iwbemclassobject_getpropertyqualifierset, wbemcli/IWbemClassObject::GetPropertyQualifierSet, wmi.iwbemclassobject_getpropertyqualifierset
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
-	IWbemClassObject.GetPropertyQualifierSet
product: Windows
targetos: Windows
req.lib: WbemUuid.lib
req.dll: CIMWin32.dll; Esscli.dll; Fastprox.dll; FrameDyn.dll; FrameDynOS.dll; Krnlprov.dll; Ncprov.dll; Wbemcore.dll; Wbemess.dll; Wmipiprt.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# IWbemClassObject::GetPropertyQualifierSet


## -description


The 
<b>IWbemClassObject::GetPropertyQualifierSet</b> method gets the qualifier set for a particular property in the class object. You can use this method with properties that are a member of an instance or a class definition.


## -parameters




### -param wszProperty [in]

Property for which the qualifier set is requested. This cannot be <b>NULL</b> and must point to a valid <b>LPCWSTR</b>. The property can be local or propagated from the parent class. Note that system properties have no qualifiers so this method returns the error code <b>WBEM_E_SYSTEM_PROPERTY</b> if you attempt to obtain the 
<a href="https://msdn.microsoft.com/8b36bd32-4931-4641-a019-cbaa3547edd0">IWbemQualifierSet</a> pointer for a system property.


### -param ppQualSet [out]

Receives an interface pointer that allows access to the qualifiers for the named property. The caller must call <b>IWbemQualifierSet::Release</b> on the pointer when access to the object is no longer required. The property is set to point to <b>NULL</b> when there are error conditions. A new object is not returned.


## -returns



This method returns an <b>HRESULT</b> indicating the status of the method call. The following list lists the value contained within an <b>HRESULT</b>. For general <b>HRESULT</b> values, see <a href="https://msdn.microsoft.com/4a3a8feb-a05f-4614-8f04-1f507da7e5b7">System Error Codes</a>.




## -see-also




<a href="https://msdn.microsoft.com/a3ce37d7-5580-4b84-9119-78412c8e0d27">IWbemClassObject</a>



<a href="https://msdn.microsoft.com/8b36bd32-4931-4641-a019-cbaa3547edd0">IWbemQualifierSet</a>
 

 

