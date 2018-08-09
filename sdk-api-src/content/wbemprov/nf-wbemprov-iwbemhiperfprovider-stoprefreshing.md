---
UID: NF:wbemprov.IWbemHiPerfProvider.StopRefreshing
title: IWbemHiPerfProvider::StopRefreshing
author: windows-sdk-content
description: Stops refreshing the object or enumerator corresponding to the supplied identifier.
old-location: wmi\iwbemhiperfprovider_stoprefreshing.htm
old-project: WmiSdk
ms.assetid: d1de54de-b57b-4e15-84b3-96cc36bf023b
ms.author: windowssdkdev
ms.date: 08/03/2018
ms.keywords: IWbemHiPerfProvider interface [Windows Management Instrumentation],StopRefreshing method, IWbemHiPerfProvider.StopRefreshing, IWbemHiPerfProvider::StopRefreshing, StopRefreshing, StopRefreshing method [Windows Management Instrumentation], StopRefreshing method [Windows Management Instrumentation],IWbemHiPerfProvider interface, _hmm_iwbemhiperfprovider_stoprefreshing, wbemprov/IWbemHiPerfProvider::StopRefreshing, wmi.iwbemhiperfprovider_stoprefreshing
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: wbemprov.h
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
req.typenames: WbemTimeout
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Wmiprvsd.dll
api_name:
 - IWbemHiPerfProvider.StopRefreshing
product: Windows
targetos: Windows
req.lib: Wbemuuid.lib
req.dll: Wmiprvsd.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# IWbemHiPerfProvider::StopRefreshing


## -description


The 
<b>IWbemHiPerfProvider::StopRefreshing</b> method stops refreshing the object or enumerator corresponding to the supplied identifier. The WMI Refresher calls this method in response to a client request to <a href="https://msdn.microsoft.com/f6e68b95-e9d1-473e-add4-823b6db51709">IWbemConfiguratorRefresher::Remove</a>. The provider should check the objects and enumerators associated with the refresher for a matching identifier. When the provider finds an identifier, the provider should remove or release the enumerator.
<div class="alert"><b>Note</b>  If a provider does not implement this method, it must return <b>WBEM_E_PROVIDER_NOT_CAPABLE</b>. A provider should implement <b>StopRefreshing</b> if it implements 
<a href="https://msdn.microsoft.com/086a1717-b6e8-45c1-9397-ec894ee900a0">IWbemHiPerfProvider::CreateRefreshableEnum</a> or 
<a href="https://msdn.microsoft.com/1eb414e0-cdf6-4caa-88a5-8da17a32449c">IWbemHiPerfProvider::CreateRefreshableObject</a>.</div><div> </div>

## -parameters




### -param pRefresher [in]

A pointer to a 
<a href="https://msdn.microsoft.com/cd1d652a-f0ce-401c-9a5e-074e6bb4d9ed">IWbemRefresher</a> object that contains a refresher obtained by calling 
<a href="https://msdn.microsoft.com/5962f5f6-a121-4234-8dcd-24c0e2b53990">IWbemHiPerfProvider::CreateRefresher</a>.


### -param lId [in]

An integer containing a refresher identifier that uniquely identifies the object to stop refreshing.


### -param lFlags [in]

An integer containing the flags.


## -returns



This method returns an <b>HRESULT</b> indicating the status of the method call. The following list lists the value contained within an <b>HRESULT</b>.




## -remarks



It is not necessary to call 
<b>StopRefreshing</b> to clean up a refresher. It is sufficient simply to delete the refresher; that is, to release all references to it. Deleting the refresher causes the cleanup of all objects and enumerators within it.




## -see-also




<a href="https://msdn.microsoft.com/a4f537ba-9081-43b4-acff-4d206de3d9d7">Developing a WMI Provider</a>



<a href="https://msdn.microsoft.com/eb0d12c0-d746-4bae-b47d-50350d33447a">IWbemHiPerfProvider</a>



Making an Instance Provider into a High-Performance Provider



<a href="https://msdn.microsoft.com/2c7206e7-f5f8-4d40-b993-56122e48069b">Performance Counter Provider</a>



<a href="https://msdn.microsoft.com/6a22d6f7-d9e2-45fa-876d-921a4bc4f574">Writing an Instance Provider</a>
 

 

