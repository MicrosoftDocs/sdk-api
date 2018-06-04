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
 

 

