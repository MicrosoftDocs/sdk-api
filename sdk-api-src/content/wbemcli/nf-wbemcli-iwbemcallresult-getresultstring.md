---
UID: NF:wbemcli.IWbemCallResult.GetResultString
title: IWbemCallResult::GetResultString
author: windows-sdk-content
description: The IWbemCallResult::GetResultString method returns the assigned object path of an instance newly created by IWbemServices::PutInstance.
old-location: wmi\iwbemcallresult_getresultstring.htm
tech.root: WmiSdk
ms.assetid: 7a022519-c112-42d4-b777-c3828439f7dd
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: GetResultString, GetResultString method [Windows Management Instrumentation], GetResultString method [Windows Management Instrumentation],IWbemCallResult interface, IWbemCallResult interface [Windows Management Instrumentation],GetResultString method, IWbemCallResult.GetResultString, IWbemCallResult::GetResultString, _hmm_iwbemcallresult_getresultstring, wbemcli/IWbemCallResult::GetResultString, wmi.iwbemcallresult_getresultstring
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
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Wbemcli.h
api_name:
 - IWbemCallResult.GetResultString
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IWbemCallResult::GetResultString


## -description


The 
<b>IWbemCallResult::GetResultString</b> method returns the assigned object path of an instance newly created by 
<a href="https://msdn.microsoft.com/1e07b328-40f7-4e14-bf53-9a5cebfc23f6">IWbemServices::PutInstance</a>.
<div class="alert"><b>Note</b>  The call result object is primarily used when the 
<a href="https://msdn.microsoft.com/1e07b328-40f7-4e14-bf53-9a5cebfc23f6">PutInstance</a> call is carried out by a provider and the client needs to know the object path (the values of the key properties) assigned the provider. For example, if the class key property is a globally unique identifier (GUID), assigned by the provider during the 
<b>PutInstance</b> operation, the client would have no way of knowing this GUID unless the provider was able to return it in this way.</div><div> </div>

## -parameters




### -param lTimeout [in]

Specifies the maximum time in milliseconds that this call blocks before returning. If you use the constant <b>WBEM_INFINITE</b> (0xFFFFFFFF), the call blocks until the object path is available. If you use 0, the call immediately returns either the object path or a status code.


### -param pstrResultString [out]

Cannot be <b>NULL</b>. This parameter receives a pointer to the object path, which, in turn, leads to the newly created object. The returned string must be deallocated using the system call <i>SysFreeString</i>. On error, a new string is not returned.


## -returns



This method returns an <b>HRESULT</b> indicating the status of the method call. The following list lists the value contained withinan <b>HRESULT</b>.

On error, you can call the COM function <b>GetErrorInfo</b> to obtain more error information.

COM-specific error codes may also be returned if network problems cause you to lose the remote connection to Windows Management.




## -see-also




<a href="https://msdn.microsoft.com/f0aa0233-3b9b-4757-bfdc-26d9fd556ce9">IWbemCallResult</a>



<a href="https://msdn.microsoft.com/1e07b328-40f7-4e14-bf53-9a5cebfc23f6">IWbemServices::PutInstance</a>
 

 

