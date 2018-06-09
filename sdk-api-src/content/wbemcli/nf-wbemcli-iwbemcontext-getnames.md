---
UID: NF:wbemcli.IWbemContext.GetNames
title: IWbemContext::GetNames
author: windows-sdk-content
description: The IWbemContext::GetNames method returns a SAFEARRAY structure of all of the names of the named context values.
old-location: wmi\iwbemcontext_getnames.htm
old-project: WmiSdk
ms.assetid: 781c4a13-ff9e-4448-8a83-3c4d8653324a
ms.author: windowssdkdev
ms.date: 06/07/2018
ms.keywords: GetNames, GetNames method [Windows Management Instrumentation], GetNames method [Windows Management Instrumentation],IWbemContext interface, IWbemContext interface [Windows Management Instrumentation],GetNames method, IWbemContext.GetNames, IWbemContext::GetNames, _hmm_iwbemcontext_getnames, wbemcli/IWbemContext::GetNames, wmi.iwbemcontext_getnames
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
 - IWbemContext.GetNames
product: Windows
targetos: Windows
req.lib: Wbemuuid.lib
req.dll: Esscli.dll; Fastprox.dll; FrameDyn.dll; FrameDynOS.dll; Wbemcomn.dll; Wbemcore.dll; Wbemess.dll; Wmipjobj.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# IWbemContext::GetNames


## -description


The 
<b>IWbemContext::GetNames</b> method returns a <b>SAFEARRAY</b> structure of all of the names of the named context values. After all the names are known, 
<a href="https://msdn.microsoft.com/library/windows/hardware/ff597624">GetValue</a> can be called on each name to retrieve the value. This technique is a way of accessing the context values that is different from calling the 
<a href="https://msdn.microsoft.com/34106c63-3b50-4078-babf-12173bd702ba">BeginEnumeration</a>, 
<a href="https://msdn.microsoft.com/library/windows/hardware/dn926903">Next</a>, and 
<a href="https://msdn.microsoft.com/bbd12aec-55ee-4cee-bf27-85f12467e06f">EndEnumeration</a> methods.


## -parameters




### -param lFlags [in]

Reserved. This parameter must be 0.


### -param pNames [out]

This parameter cannot be <b>NULL</b>, but on entry it must point to <b>NULL</b>. If no error is returned, on exit <i>pstrNames</i> receives a pointer to a new <b>SAFEARRAY</b> structure of type VT_BSTR containing all the context value names. The caller must call <b>SafeArrayDestroy</b> on the returned pointer when the array is no longer required. If an error code is returned, the pointer is left unmodified.

<div class="alert"><b>Note</b>  If there are no named values in the object, the call succeeds and returns an array of length 0.</div>
<div> </div>

## -returns



This method returns an <b>HRESULT</b> indicating the status of the method call. The following list lists the value contained within an <b>HRESULT</b>.




## -remarks



For more information about using <b>SAFEARRAY</b> structures of <b>BSTR</b> values, see 
<a href="https://msdn.microsoft.com/6cc26b26-adc9-4a8a-b51e-9db94eb4295f">Retrieving Part of a WMI Instance</a>.




## -see-also




<a href="https://msdn.microsoft.com/458bd455-6984-414b-a0b7-62887d9dad7c">IWbemContext</a>



<a href="https://msdn.microsoft.com/34106c63-3b50-4078-babf-12173bd702ba">IWbemContext::BeginEnumeration</a>



<a href="https://msdn.microsoft.com/e11fff37-aeb7-41c5-8639-ca0a7a144263">IWbemContext::GetValue</a>
 

 

