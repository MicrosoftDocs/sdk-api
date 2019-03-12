---
UID: NF:wsddisco.IWSDiscoveryProviderNotify.Remove
title: IWSDiscoveryProviderNotify::Remove
author: windows-sdk-content
description: Provides information on a recently departed discovery host (from a Bye message).
old-location: ncd\iwsdiscoveryprovidernotify_remove.htm
tech.root: WsdApi
ms.assetid: 776fc1d5-9dfe-445f-9af6-36faf971bf37
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IWSDiscoveryProviderNotify interface,Remove method, IWSDiscoveryProviderNotify.Remove, IWSDiscoveryProviderNotify::Remove, Remove, Remove method, Remove method,IWSDiscoveryProviderNotify interface, ncd.iwsdiscoveryprovidernotify_remove, wsddisco/IWSDiscoveryProviderNotify::Remove
ms.topic: method
req.header: wsddisco.h
req.include-header: Wsdapi.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Wsddisco.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: Wsdapi.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Wsdapi.dll
api_name:
 - IWSDiscoveryProviderNotify.Remove
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IWSDiscoveryProviderNotify::Remove


## -description


Provides information on a recently departed discovery host (from a Bye message).


## -parameters




### -param pService [in]

A pointer to an <a href="https://msdn.microsoft.com/6516098a-e440-4dec-b275-165ea3072d49">IWSDiscoveredService</a> interface that represents a remote discovery host.


## -returns



The return value is not meaningful. An implementer should return S_OK.




## -remarks



<b>Remove</b> will be called once per announcement of a departing discovery host.

<div class="alert"><b>Note</b>  Multiple simultaneous calls may be made to <b>Remove</b> by the provider, so it is essential that shared data be synchronized when implementing this callback routine.</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/e186f721-14d9-4d9b-942a-1c05ada2bee6">IWSDiscoveryProviderNotify</a>
 

 

