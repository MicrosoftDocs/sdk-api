---
UID: NF:wbemcli.IWbemContext.Clone
title: IWbemContext::Clone
author: windows-sdk-content
description: The IWbemContext::Clone method makes a logical copy of the current IWbemContext object. This method can be useful when many calls must be made which have largely identical IWbemContext objects.
old-location: wmi\iwbemcontext_clone.htm
tech.root: WmiSdk
ms.assetid: a832f4b0-a450-4f74-a6ec-d205f57c1656
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: Clone, Clone method [Windows Management Instrumentation], Clone method [Windows Management Instrumentation],IWbemContext interface, IWbemContext interface [Windows Management Instrumentation],Clone method, IWbemContext.Clone, IWbemContext::Clone, _hmm_iwbemcontext_clone, wbemcli/IWbemContext::Clone, wmi.iwbemcontext_clone
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
req.lib: Wbemuuid.lib
req.dll: Esscli.dll; Fastprox.dll; FrameDyn.dll; FrameDynOS.dll; Wbemcomn.dll; Wbemcore.dll; Wbemess.dll; Wmipjobj.dll
req.irql: 
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
 - IWbemContext.Clone
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IWbemContext::Clone


## -description


The 
<b>IWbemContext::Clone</b> method makes a logical copy of the current 
<a href="https://msdn.microsoft.com/458bd455-6984-414b-a0b7-62887d9dad7c">IWbemContext</a> object. This method can be useful when many calls must be made which have largely identical 
<b>IWbemContext</b> objects.


## -parameters




### -param ppNewCopy [out]

Must point to <b>NULL</b> on entry. It receives a pointer to the new object containing the clone of the current object. The returned pointer has a positive reference count. The caller must call <b>IWbemServices::Release</b> on this pointer when it is no longer needed. On error, this pointer is left unmodified, and a new object is not returned.


## -returns



This method returns an <b>HRESULT</b>HRESULT indicating the status of the method call. The following list lists the value contained withinan <b>HRESULT</b>HRESULT.



