---
UID: NF:wsddisco.IWSDiscoveryProviderNotify.Add
title: IWSDiscoveryProviderNotify::Add
author: windows-sdk-content
description: Provides information on either a newly announced discovery host (from a Hello message), or a match to a user initiated query.
old-location: ncd\iwsdiscoveryprovidernotify_add.htm
old-project: wsdapi
ms.assetid: 4e36157f-444d-4e59-bc30-c6def9c51cea
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: Add, Add method, Add method,IWSDiscoveryProviderNotify interface, IWSDiscoveryProviderNotify interface,Add method, IWSDiscoveryProviderNotify.Add, IWSDiscoveryProviderNotify::Add, ncd.iwsdiscoveryprovidernotify_add, wsddisco/IWSDiscoveryProviderNotify::Add
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: WSD_SECURITY_SIGNATURE_VALIDATION, *PWSD_SECURITY_SIGNATURE_VALIDATION
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Wsdapi.dll
api_name:
 - IWSDiscoveryProviderNotify.Add
product: Windows
targetos: Windows
req.lib: 
req.dll: Wsdapi.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IWSDiscoveryProviderNotify::Add


## -description


Provides information on either a newly announced discovery host (from a Hello message), or a match to a user initiated query.


## -parameters




### -param pService [in]

A pointer to an <a href="https://msdn.microsoft.com/6516098a-e440-4dec-b275-165ea3072d49">IWSDiscoveredService</a> interface that represents a remote discovery host.


## -returns



The return value is not meaningful. An implementer should return S_OK.




## -remarks



<b>Add</b> will be called once for each successful match to an outstanding query, and once per announcement of a new discovery host.

<div class="alert"><b>Note</b>  Multiple simultaneous calls may be made to <b>Add</b> by the provider, so it is essential that shared data be synchronized when implementing this callback routine.</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/e186f721-14d9-4d9b-942a-1c05ada2bee6">IWSDiscoveryProviderNotify</a>
 

 

