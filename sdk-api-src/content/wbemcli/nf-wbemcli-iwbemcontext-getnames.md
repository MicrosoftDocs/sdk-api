---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
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
 

 

