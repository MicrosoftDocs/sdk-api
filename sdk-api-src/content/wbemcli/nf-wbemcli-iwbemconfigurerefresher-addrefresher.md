---
UID: NF:wbemcli.IWbemConfigureRefresher.AddRefresher
title: IWbemConfigureRefresher::AddRefresher
author: windows-sdk-content
description: The IWbemConfigureRefresher::AddRefresher method adds a refresher to a refresher.
old-location: wmi\iwbemconfigurerefresher_addrefresher.htm
old-project: WmiSdk
ms.assetid: 17eaf6b0-e2e1-4a23-952d-2439da89f765
ms.author: windowssdkdev
ms.date: 06/07/2018
ms.keywords: AddRefresher, AddRefresher method [Windows Management Instrumentation], AddRefresher method [Windows Management Instrumentation],IWbemConfigureRefresher interface, IWbemConfigureRefresher interface [Windows Management Instrumentation],AddRefresher method, IWbemConfigureRefresher.AddRefresher, IWbemConfigureRefresher::AddRefresher, _hmm_iwbemconfigurerefresher_addrefresher, wbemcli/IWbemConfigureRefresher::AddRefresher, wmi.iwbemconfigurerefresher_addrefresher
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
 - Wbemuuid.lib
 - Wbemuuid.dll
api_name:
 - IWbemConfigureRefresher.AddRefresher
product: Windows
targetos: Windows
req.lib: Wbemuuid.lib
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
---

# IWbemConfigureRefresher::AddRefresher


## -description


The 
<b>IWbemConfigureRefresher::AddRefresher</b> method adds a refresher to a refresher. The newly added refresher is called a "child refresher" or "nested refresher". You can use this method to create a single refresher containing more than one refresher that can be updated using a single call to the 
<a href="https://msdn.microsoft.com/6de85040-c938-41dc-8240-0e21e89c7716">Refresh</a> method.


## -parameters




### -param pRefresher [in]

Pointer to a 
<a href="https://msdn.microsoft.com/cd1d652a-f0ce-401c-9a5e-074e6bb4d9ed">IWbemRefresher</a> object to nest in this refresher.


### -param lFlags

Reserved. This parameter must be 0 (zero).


### -param plId [out]

Pointer to an integer returned by the provider that uniquely identifies the refreshable object.


## -returns



This method returns an <b>HRESULT</b> indicating the status of the method call. The following list lists the value contained within an <b>HRESULT</b>.




## -remarks



Users should not add recursively nested refreshers. The returned identifier can be used by the 
<a href="https://msdn.microsoft.com/library/windows/hardware/hh439492">Remove</a> function to remove the refresher. Although it is not necessary for the client to explicitly remove added refreshers, the client must call <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nf-unknwn-iunknown-release">Release</a> on the refreshers when they are no longer required.




## -see-also




<a href="https://msdn.microsoft.com/ee0a2ead-f53a-4651-a287-04a62eba3f84">Accessing Performance Data in C++</a>



<a href="https://msdn.microsoft.com/9dd56891-5f2f-4b0e-9f70-fd75cb9bbd43">IWbemConfigureRefresher</a>



<a href="https://msdn.microsoft.com/6a22d6f7-d9e2-45fa-876d-921a4bc4f574">Making an Instance Provider into a High-Performance Provider</a>



<a href="https://msdn.microsoft.com/2c7206e7-f5f8-4d40-b993-56122e48069b">Performance Counter Provider</a>
 

 

