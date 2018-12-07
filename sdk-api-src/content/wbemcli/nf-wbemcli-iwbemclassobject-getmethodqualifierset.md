---
UID: NF:wbemcli.IWbemClassObject.GetMethodQualifierSet
title: IWbemClassObject::GetMethodQualifierSet
author: windows-sdk-content
description: The IWbemClassObject::GetMethodQualifierSet is used to retrieve the qualifier set for a particular method.
old-location: wmi\iwbemclassobject_getmethodqualifierset.htm
tech.root: WmiSdk
ms.assetid: ba328f43-b08a-4b09-8aff-d7075cb6d419
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: GetMethodQualifierSet, GetMethodQualifierSet method [Windows Management Instrumentation], GetMethodQualifierSet method [Windows Management Instrumentation],IWbemClassObject interface, IWbemClassObject interface [Windows Management Instrumentation],GetMethodQualifierSet method, IWbemClassObject.GetMethodQualifierSet, IWbemClassObject::GetMethodQualifierSet, _hmm_iwbemclassobject_getmethodqualifierset, wbemcli/IWbemClassObject::GetMethodQualifierSet, wmi.iwbemclassobject_getmethodqualifierset
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
 - IWbemClassObject.GetMethodQualifierSet
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IWbemClassObject::GetMethodQualifierSet


## -description


The 
<b>IWbemClassObject::GetMethodQualifierSet</b> is used to retrieve the qualifier set for a particular method.

This call is supported only if the current object is a CIM class definition. Method manipulation is not available from 
<a href="https://msdn.microsoft.com/a3ce37d7-5580-4b84-9119-78412c8e0d27">IWbemClassObject</a> pointers, which point to CIM instances.


## -parameters




### -param wszMethod [in]

Must point to a valid <b>LPCWSTR</b> containing the method name.


### -param ppQualSet [out]

Receives the interface pointer that allows access to the qualifiers for the method. The returned object has a positive reference count upon return from the call. The caller must call <b>IWbemQualifierSet::Release</b> when the object is no longer needed. This parameter cannot be <b>NULL</b>. On error, a new object is not returned, and the pointer is set to point to <b>NULL</b>.


## -returns



This method returns an <b>HRESULT</b> indicating the status of the method call. The following list lists the value contained within an <b>HRESULT</b>. For general <b>HRESULT</b> values, see <a href="https://msdn.microsoft.com/4a3a8feb-a05f-4614-8f04-1f507da7e5b7">System Error Codes</a>.




## -remarks



Because each method may have its own qualifiers, use this call to retrieve the 
<a href="https://msdn.microsoft.com/8b36bd32-4931-4641-a019-cbaa3547edd0">IWbemQualifierSet</a> pointer, which allows the caller to add, edit, or delete such qualifiers.



