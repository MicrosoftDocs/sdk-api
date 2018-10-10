---
UID: NF:wbemcli.IWbemClassObject.BeginEnumeration
title: IWbemClassObject::BeginEnumeration
author: windows-sdk-content
description: Resets an enumeration back to the beginning of the enumeration.
old-location: wmi\iwbemclassobject_beginenumeration.htm
tech.root: WmiSdk
ms.assetid: c7ece530-5309-4f0d-9096-73d01b4a7fde
ms.author: windowssdkdev
ms.date: 10/09/2018
ms.keywords: BeginEnumeration, BeginEnumeration method [Windows Management Instrumentation], BeginEnumeration method [Windows Management Instrumentation],IWbemClassObject interface, IWbemClassObject interface [Windows Management Instrumentation],BeginEnumeration method, IWbemClassObject.BeginEnumeration, IWbemClassObject::BeginEnumeration, _hmm_iwbemclassobject_beginenumeration, wbemcli/IWbemClassObject::BeginEnumeration, wmi.iwbemclassobject_beginenumeration
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
 - IWbemClassObject.BeginEnumeration
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IWbemClassObject::BeginEnumeration


## -description


The 
<b>IWbemClassObject::BeginEnumeration</b> method resets an enumeration back to the beginning of the enumeration. The caller must call this method prior to the first call to 
<a href="https://msdn.microsoft.com/6d0e8aa3-ae64-4934-9000-2c526ceb7fb6">IWbemClassObject::Next</a> to enumerate all of the properties on an object. The order in which properties are enumerated is guaranteed to be invariant for a given instance of 
<a href="https://msdn.microsoft.com/a3ce37d7-5580-4b84-9119-78412c8e0d27">IWbemClassObject</a>.


## -parameters




### -param lEnumFlags [in]

Combination of flags described in Remarks.


## -returns



This method returns an <b>HRESULT</b> indicating the status of the method call. The following list lists the value contained within an <b>HRESULT</b>. For general <b>HRESULT</b> values, see <a href="https://msdn.microsoft.com/4a3a8feb-a05f-4614-8f04-1f507da7e5b7">System Error Codes</a>.




## -remarks



You can control the properties included in the enumeration by specifying a combination of the following flags. You can combine one flag from each group with any flag from any other group. However, flags from the same group are mutually exclusive.

GROUP 1



GROUP 2






## -see-also




<a href="https://msdn.microsoft.com/a3ce37d7-5580-4b84-9119-78412c8e0d27">IWbemClassObject</a>



<a href="https://msdn.microsoft.com/a9fa8567-7504-4d59-a874-1dc7b2620a0b">IWbemClassObject::EndEnumeration</a>



<a href="https://msdn.microsoft.com/6d0e8aa3-ae64-4934-9000-2c526ceb7fb6">IWbemClassObject::Next</a>



<a href="https://msdn.microsoft.com/e812c0cb-3e08-4cac-8d05-2cd7abc922d1">WMI System Properties</a>
 

 

