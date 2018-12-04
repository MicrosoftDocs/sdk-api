---
UID: NF:wbemcli.IWbemConfigureRefresher.Remove
title: IWbemConfigureRefresher::Remove
author: windows-sdk-content
description: The IWbemConfigureRefresher::Remove method is used to remove an object, enumerator, or nested refresher from a refresher.
old-location: wmi\iwbemconfigurerefresher_remove.htm
tech.root: WmiSdk
ms.assetid: f6e68b95-e9d1-473e-add4-823b6db51709
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: IWbemConfigureRefresher interface [Windows Management Instrumentation],Remove method, IWbemConfigureRefresher.Remove, IWbemConfigureRefresher::Remove, Remove, Remove method [Windows Management Instrumentation], Remove method [Windows Management Instrumentation],IWbemConfigureRefresher interface, _hmm_iwbemconfigurerefresher_remove, wbemcli/IWbemConfigureRefresher::Remove, wmi.iwbemconfigurerefresher_remove
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
req.lib: Wbemuuid.lib
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Wbemuuid.lib
 - Wbemuuid.dll
api_name:
 - IWbemConfigureRefresher.Remove
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IWbemConfigureRefresher::Remove


## -description


The 
<b>IWbemConfigureRefresher::Remove</b> method is used to remove an object, enumerator, or nested refresher from a refresher.


## -parameters




### -param lId [in]

Integer that uniquely identifies the object to remove. You obtain this identifier when you first add an object to the refresher by calling 
<a href="https://msdn.microsoft.com/85721e0c-863b-45af-91ca-8ee14af37181">IWbemConfigureRefresher::AddObjectByPath</a>, 
<a href="https://msdn.microsoft.com/c3f25484-7c6c-4625-9d26-1c01d15b10c4">IWbemConfigureRefresher::AddObjectByTemplate</a>, 
<a href="https://msdn.microsoft.com/5b013267-78bc-4372-b55a-58e330acf927">IWbemConfigureRefresher::AddEnum</a>, or 
<a href="https://msdn.microsoft.com/17eaf6b0-e2e1-4a23-952d-2439da89f765">IWbemConfigureRefresher::AddRefresher</a>.


### -param lFlags [in]

Bitmask of flags that modify the behavior of the 
<b>Remove</b> method. If this parameter is set to. <b>WBEM_FLAG_REFRESH_AUTO_RECONNECT</b>, the refresher attempts to automatically reconnect to a remote provider if the connection is broken. This is default behavior for this method. Specify <b>WBEM_FLAG_REFRESH_NO_AUTO_RECONNECT</b> if you do not want the refresher to attempt to reconnect to a remote provider.


## -returns



This method returns an <b>HRESULT</b> indicating the status of the method call. The following list lists the value contained within an <b>HRESULT</b>.




## -see-also




<a href="https://msdn.microsoft.com/ee0a2ead-f53a-4651-a287-04a62eba3f84">Accessing Performance Data in C++</a>



<a href="https://msdn.microsoft.com/9dd56891-5f2f-4b0e-9f70-fd75cb9bbd43">IWbemConfigureRefresher</a>



<a href="https://msdn.microsoft.com/eb0d12c0-d746-4bae-b47d-50350d33447a">IWbemHiPerfProvider</a>



<a href="https://msdn.microsoft.com/6a22d6f7-d9e2-45fa-876d-921a4bc4f574">Making an Instance Provider into a High-Performance Provider</a>



<a href="https://msdn.microsoft.com/2c7206e7-f5f8-4d40-b993-56122e48069b">Performance Counter Provider</a>
 

 

