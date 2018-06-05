---
UID: NF:wbemcli.IWbemClassObject.GetMethodOrigin
title: IWbemClassObject::GetMethodOrigin
author: windows-sdk-content
description: The IWbemClassObject::GetMethodOrigin method is used to determine the class for which a method was declared.
old-location: wmi\iwbemclassobject_getmethodorigin.htm
old-project: WmiSdk
ms.assetid: e3d55b1f-f9bd-40d1-9ad5-990c264524d5
ms.author: windowssdkdev
ms.date: 05/30/2018
ms.keywords: GetMethodOrigin, GetMethodOrigin method [Windows Management Instrumentation], GetMethodOrigin method [Windows Management Instrumentation],IWbemClassObject interface, IWbemClassObject interface [Windows Management Instrumentation],GetMethodOrigin method, IWbemClassObject.GetMethodOrigin, IWbemClassObject::GetMethodOrigin, _hmm_iwbemclassobject_getmethodorigin, wbemcli/IWbemClassObject::GetMethodOrigin, wmi.iwbemclassobject_getmethodorigin
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
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
-	IWbemClassObject.GetMethodOrigin
product: Windows
targetos: Windows
req.lib: WbemUuid.lib
req.dll: CIMWin32.dll; Esscli.dll; Fastprox.dll; FrameDyn.dll; FrameDynOS.dll; Krnlprov.dll; Ncprov.dll; Wbemcore.dll; Wbemess.dll; Wmipiprt.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# IWbemClassObject::GetMethodOrigin


## -description


The 
<b>IWbemClassObject::GetMethodOrigin</b> method is used to determine the class for which a method was declared.

This call is only supported if the current object is a CIM class definition. Method manipulation is not available from 
<a href="https://msdn.microsoft.com/a3ce37d7-5580-4b84-9119-78412c8e0d27">IWbemClassObject</a> pointers which point to CIM instances.


## -parameters




### -param wszMethodName [in]

Name of the method for the object whose owning class is being requested.


### -param pstrClassName [out]

Receives the name of the class which owns the method. The user must call <b>SysFreeString </b>on the returned <i>BSTR</i> when it is no longer required.


## -returns



This method returns an <b>HRESULT</b> indicating the status of the method call. The following list lists the value contained within an <b>HRESULT</b>. For general <b>HRESULT</b> values, see <a href="https://msdn.microsoft.com/4a3a8feb-a05f-4614-8f04-1f507da7e5b7">System Error Codes</a>.




## -remarks



Because methods are inherited from class to class, it is often desirable to determine the owning class for a given method.



