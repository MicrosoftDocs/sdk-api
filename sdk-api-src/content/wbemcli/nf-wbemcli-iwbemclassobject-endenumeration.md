---
UID: NF:wbemcli.IWbemClassObject.EndEnumeration
title: IWbemClassObject::EndEnumeration
author: windows-sdk-content
description: The IWbemClassObject::EndEnumeration method terminates an enumeration sequence started with IWbemClassObject::BeginEnumeration.
old-location: wmi\iwbemclassobject_endenumeration.htm
old-project: WmiSdk
ms.assetid: a9fa8567-7504-4d59-a874-1dc7b2620a0b
ms.author: windowssdkdev
ms.date: 08/03/2018
ms.keywords: EndEnumeration, EndEnumeration method [Windows Management Instrumentation], EndEnumeration method [Windows Management Instrumentation],IWbemClassObject interface, IWbemClassObject interface [Windows Management Instrumentation],EndEnumeration method, IWbemClassObject.EndEnumeration, IWbemClassObject::EndEnumeration, _hmm_iwbemclassobject_endenumeration, wbemcli/IWbemClassObject::EndEnumeration, wmi.iwbemclassobject_endenumeration
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
 - IWbemClassObject.EndEnumeration
product: Windows
targetos: Windows
req.lib: WbemUuid.lib
req.dll: CIMWin32.dll; Esscli.dll; Fastprox.dll; FrameDyn.dll; FrameDynOS.dll; Krnlprov.dll; Ncprov.dll; Wbemcore.dll; Wbemess.dll; Wmipiprt.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# IWbemClassObject::EndEnumeration


## -description


The 
<b>IWbemClassObject::EndEnumeration</b> method terminates an enumeration sequence started with 
<a href="https://msdn.microsoft.com/c7ece530-5309-4f0d-9096-73d01b4a7fde">IWbemClassObject::BeginEnumeration</a>. This call is not required, but it is recommended to developers because it releases resources associated with the enumeration. However, the resources are deallocated automatically when the next enumeration is started or the object is released.


## -parameters






## -returns



This method returns an <b>HRESULT</b> indicating the status of the method call. The following list lists the value contained within an <b>HRESULT</b>. For general <b>HRESULT</b> values, see <a href="https://msdn.microsoft.com/4a3a8feb-a05f-4614-8f04-1f507da7e5b7">System Error Codes</a>.




## -see-also




<a href="https://msdn.microsoft.com/a3ce37d7-5580-4b84-9119-78412c8e0d27">IWbemClassObject</a>



<a href="https://msdn.microsoft.com/c7ece530-5309-4f0d-9096-73d01b4a7fde">IWbemClassObject::BeginEnumeration</a>



<a href="https://msdn.microsoft.com/6d0e8aa3-ae64-4934-9000-2c526ceb7fb6">IWbemClassObject::Next</a>
 

 

