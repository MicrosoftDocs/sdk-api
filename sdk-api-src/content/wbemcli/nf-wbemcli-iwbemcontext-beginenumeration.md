---
UID: NF:wbemcli.IWbemContext.BeginEnumeration
title: IWbemContext::BeginEnumeration
author: windows-sdk-content
description: The IWbemContext::BeginEnumeration method resets the enumeration of all the context values in the object.
old-location: wmi\iwbemcontext_beginenumeration.htm
old-project: WmiSdk
ms.assetid: 34106c63-3b50-4078-babf-12173bd702ba
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: BeginEnumeration, BeginEnumeration method [Windows Management Instrumentation], BeginEnumeration method [Windows Management Instrumentation],IWbemContext interface, IWbemContext interface [Windows Management Instrumentation],BeginEnumeration method, IWbemContext.BeginEnumeration, IWbemContext::BeginEnumeration, _hmm_iwbemcontext_beginenumeration, wbemcli/IWbemContext::BeginEnumeration, wmi.iwbemcontext_beginenumeration
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
req.idl: 
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
 - Esscli.dll
 - Fastprox.dll
 - FrameDyn.dll
 - FrameDynOS.dll
 - Wbemcomn.dll
 - Wbemcore.dll
 - Wbemess.dll
 - Wmipjobj.dll
api_name:
 - IWbemContext.BeginEnumeration
product: Windows
targetos: Windows
req.lib: Wbemuuid.lib
req.dll: Esscli.dll; Fastprox.dll; FrameDyn.dll; FrameDynOS.dll; Wbemcomn.dll; Wbemcore.dll; Wbemess.dll; Wmipjobj.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# IWbemContext::BeginEnumeration


## -description


The 
<b>IWbemContext::BeginEnumeration</b> method resets the enumeration of all the context values in the object. This method must be called before the first call to 
<a href="https://msdn.microsoft.com/e316564c-a739-472b-b7a8-8acbf71e1c58">IWbemContext::Next</a> to enumerate all of the context values in the object. The order in which context values are enumerated is guaranteed to be invariant for a given instance of 
<a href="https://msdn.microsoft.com/458bd455-6984-414b-a0b7-62887d9dad7c">IWbemContext</a>.


## -parameters




### -param lFlags [in]

Reserved. This parameter must be 0.


## -returns



This method returns an <b>HRESULT</b>HRESULT indicating the status of the method call. The following list lists the value contained withinan <b>HRESULT</b>HRESULT.




## -see-also




<a href="https://msdn.microsoft.com/458bd455-6984-414b-a0b7-62887d9dad7c">IWbemContext</a>



<a href="https://msdn.microsoft.com/bbd12aec-55ee-4cee-bf27-85f12467e06f">IWbemContext::EndEnumeration</a>



<a href="https://msdn.microsoft.com/e316564c-a739-472b-b7a8-8acbf71e1c58">IWbemContext::Next</a>
 

 

