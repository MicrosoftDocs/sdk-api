---
UID: NF:wdstptmgmt.IWdsTransportCacheable.Refresh
title: IWdsTransportCacheable::Refresh
author: windows-sdk-content
description: Refreshes the object data members by rereading their values from the underlying data store. This is allowed only if the object's IWdsTransportCacheable::Dirty property has been set.
old-location: wds\iwdstransportcacheable_refresh.htm
tech.root: wds
ms.assetid: 2fd838b5-5623-4133-9ad8-ec051b2b698d
ms.author: windowssdkdev
ms.date: 09/14/2018
ms.keywords: IWdsTransportCacheable interface [Windows Deployment Services],Refresh method, IWdsTransportCacheable.Refresh, IWdsTransportCacheable::Refresh, Refresh, Refresh method [Windows Deployment Services], Refresh method [Windows Deployment Services],IWdsTransportCacheable interface, wds.iwdstransportcacheable_refresh, wdstptmgmt/IWdsTransportCacheable::Refresh
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: wdstptmgmt.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: Wdstptmgmt.tlb
req.lib: 
req.dll: Wdstptmgmt.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Wdstptmgmt.dll
api_name:
 - IWdsTransportCacheable.Refresh
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IWdsTransportCacheable::Refresh


## -description


Refreshes the object data members by rereading their values from the underlying data store. This is allowed only if the object's <a href="https://msdn.microsoft.com/f73e3013-e060-45bc-987c-d41cd01beef7">IWdsTransportCacheable::Dirty</a> property has been set.


## -parameters






## -remarks



When called on an object whose <a href="https://msdn.microsoft.com/f73e3013-e060-45bc-987c-d41cd01beef7">Dirty</a> property has been set, this method fails in order to avoid inadvertently losing changes made to the object. If the caller wants to ignore current changes and reread the stored data, the caller should call the <a href="https://msdn.microsoft.com/5c8495b9-6c76-4bb0-8237-5f9008cefc91">IWdsTransportCacheable::Discard</a> method instead.




## -see-also




<a href="https://msdn.microsoft.com/2245d198-056c-467f-aae7-b1bb02f188e2">IWdsTransportCacheable</a>
 

 

