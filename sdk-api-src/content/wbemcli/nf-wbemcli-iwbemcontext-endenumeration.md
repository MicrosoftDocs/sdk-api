---
UID: NF:wbemcli.IWbemContext.EndEnumeration
title: IWbemContext::EndEnumeration
author: windows-sdk-content
description: The IWbemContext::EndEnumeration method ends an enumeration sequence that begins with IWbemContext::BeginEnumeration. This call is not required, but it releases as early as possible any system resources associated with the enumeration.
old-location: wmi\iwbemcontext_endenumeration.htm
old-project: WmiSdk
ms.assetid: bbd12aec-55ee-4cee-bf27-85f12467e06f
ms.author: windowssdkdev
ms.date: 08/03/2018
ms.keywords: EndEnumeration, EndEnumeration method [Windows Management Instrumentation], EndEnumeration method [Windows Management Instrumentation],IWbemContext interface, IWbemContext interface [Windows Management Instrumentation],EndEnumeration method, IWbemContext.EndEnumeration, IWbemContext::EndEnumeration, _hmm_iwbemcontext_endenumeration, wbemcli/IWbemContext::EndEnumeration, wmi.iwbemcontext_endenumeration
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
 - IWbemContext.EndEnumeration
product: Windows
targetos: Windows
req.lib: Wbemuuid.lib
req.dll: Esscli.dll; Fastprox.dll; FrameDyn.dll; FrameDynOS.dll; Wbemcomn.dll; Wbemcore.dll; Wbemess.dll; Wmipjobj.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# IWbemContext::EndEnumeration


## -description


The 
<b>IWbemContext::EndEnumeration</b> method ends an enumeration sequence that begins with 
<a href="https://msdn.microsoft.com/34106c63-3b50-4078-babf-12173bd702ba">IWbemContext::BeginEnumeration</a>. This call is not required, but it releases as early as possible any system resources associated with the enumeration.


## -parameters






## -returns



This method returns an <b>HRESULT</b>HRESULT indicating the status of the method call. The following list lists the value contained withinan <b>HRESULT</b>HRESULT.




## -see-also




<a href="https://msdn.microsoft.com/458bd455-6984-414b-a0b7-62887d9dad7c">IWbemContext</a>



<a href="https://msdn.microsoft.com/34106c63-3b50-4078-babf-12173bd702ba">IWbemContext::BeginEnumeration</a>



<a href="https://msdn.microsoft.com/e316564c-a739-472b-b7a8-8acbf71e1c58">IWbemContext::Next</a>
 

 

