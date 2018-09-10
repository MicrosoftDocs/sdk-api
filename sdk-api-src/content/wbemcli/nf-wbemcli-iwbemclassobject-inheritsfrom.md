---
UID: NF:wbemcli.IWbemClassObject.InheritsFrom
title: IWbemClassObject::InheritsFrom
author: windows-sdk-content
description: The IWbemClassObject::InheritsFrom method determines if the current class or instance derives from a specified parent class.
old-location: wmi\iwbemclassobject_inheritsfrom.htm
tech.root: WmiSdk
ms.assetid: 05431e05-440e-4241-bde9-0dbd32039921
ms.author: windowssdkdev
ms.date: 08/28/2018
ms.keywords: IWbemClassObject interface [Windows Management Instrumentation],InheritsFrom method, IWbemClassObject.InheritsFrom, IWbemClassObject::InheritsFrom, InheritsFrom, InheritsFrom method [Windows Management Instrumentation], InheritsFrom method [Windows Management Instrumentation],IWbemClassObject interface, _hmm_iwbemclassobject_inheritsfrom, wbemcli/IWbemClassObject::InheritsFrom, wmi.iwbemclassobject_inheritsfrom
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
 - IWbemClassObject.InheritsFrom
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IWbemClassObject::InheritsFrom


## -description


The 
<b>IWbemClassObject::InheritsFrom</b> method determines if the current class or instance derives from a specified parent class.


## -parameters




### -param strAncestor

TBD




#### - wszAncestor [in]

Cannot be <b>NULL</b>. It contains the class name that is being tested. If the current object has this class for one of its ancestor classes, <b>WBEM_S_NO_ERROR</b> returns. This must point to a valid <b>LPCWSTR</b>, which is treated as read-only.


## -returns



This method returns an <b>HRESULT</b> indicating the status of the method call. The following list lists the value contained within an <b>HRESULT</b>. For general <b>HRESULT</b> values, see <a href="https://msdn.microsoft.com/4a3a8feb-a05f-4614-8f04-1f507da7e5b7">System Error Codes</a>.




## -see-also




<a href="https://msdn.microsoft.com/05228d88-baa2-4e89-a8c8-139f9ffea86c">GetPropertyOrigin</a>



<a href="https://msdn.microsoft.com/a3ce37d7-5580-4b84-9119-78412c8e0d27">IWbemClassObject</a>
 

 

