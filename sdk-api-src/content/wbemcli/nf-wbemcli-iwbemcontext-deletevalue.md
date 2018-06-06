---
UID: NF:wbemcli.IWbemContext.DeleteValue
title: IWbemContext::DeleteValue
author: windows-sdk-content
description: The IWbemContext::DeleteValue method deletes a named context value created by IWbemContext::SetValue.
old-location: wmi\iwbemcontext_deletevalue.htm
old-project: WmiSdk
ms.assetid: 5f2956cf-8901-441f-b1bd-4b2f21d74683
ms.author: windowssdkdev
ms.date: 05/30/2018
ms.keywords: DeleteValue, DeleteValue method [Windows Management Instrumentation], DeleteValue method [Windows Management Instrumentation],IWbemContext interface, IWbemContext interface [Windows Management Instrumentation],DeleteValue method, IWbemContext.DeleteValue, IWbemContext::DeleteValue, _hmm_iwbemcontext_deletevalue, wbemcli/IWbemContext::DeleteValue, wmi.iwbemcontext_deletevalue
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
 - IWbemContext.DeleteValue
product: Windows
targetos: Windows
req.lib: Wbemuuid.lib
req.dll: Esscli.dll; Fastprox.dll; FrameDyn.dll; FrameDynOS.dll; Wbemcomn.dll; Wbemcore.dll; Wbemess.dll; Wmipjobj.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# IWbemContext::DeleteValue


## -description


The 
<b>IWbemContext::DeleteValue</b> method deletes a named context value created by 
<a href="https://msdn.microsoft.com/074d5ac7-aa86-44d8-99f9-959ef99a8004">IWbemContext::SetValue</a>.


## -parameters




### -param wszName




### -param lFlags [in]

Reserved. This parameter must be 0.


#### - strName [in]

Pointer to a valid <b>BSTR</b> containing the named context value to delete. The pointer is treated as read-only.


## -returns



This method returns an <b>HRESULT</b>HRESULT indicating the status of the method call. The following list lists the value contained withinan <b>HRESULT</b>HRESULT.




## -see-also




<a href="https://msdn.microsoft.com/458bd455-6984-414b-a0b7-62887d9dad7c">IWbemContext</a>



<a href="https://msdn.microsoft.com/e11fff37-aeb7-41c5-8639-ca0a7a144263">IWbemContext::GetValue</a>



<a href="https://msdn.microsoft.com/074d5ac7-aa86-44d8-99f9-959ef99a8004">IWbemContext::SetValue</a>
 

 

