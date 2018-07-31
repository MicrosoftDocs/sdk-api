---
UID: NF:wdstptmgmt.IWdsTransportCacheable.get_Dirty
title: IWdsTransportCacheable::get_Dirty
author: windows-sdk-content
description: Receives a value that indicates whether object data has been modified.
old-location: wds\iwdstransportcacheable_dirty.htm
old-project: Wds
ms.assetid: f73e3013-e060-45bc-987c-d41cd01beef7
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: Dirty property [Windows Deployment Services], Dirty property [Windows Deployment Services],IWdsTransportCacheable interface, IWdsTransportCacheable interface [Windows Deployment Services],Dirty property, IWdsTransportCacheable.Dirty, IWdsTransportCacheable.get_Dirty, IWdsTransportCacheable::Dirty, IWdsTransportCacheable::get_Dirty, get_Dirty, wds.iwdstransportcacheable_dirty, wdstptmgmt/IWdsTransportCacheable::Dirty, wdstptmgmt/IWdsTransportCacheable::get_Dirty
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: WDSTRANSPORT_TFTP_CAPABILITY, *PWDSTRANSPORT_TFTP_CAPABILITY
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Wdstptmgmt.dll
api_name:
 - IWdsTransportCacheable.Dirty
 - IWdsTransportCacheable.get_Dirty
product: Windows
targetos: Windows
req.lib: 
req.dll: Wdstptmgmt.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# IWdsTransportCacheable::get_Dirty


## -description


Receives a value that indicates whether object data has been modified. 

This property is read-only.


## -parameters


## -remarks



All objects of the <a href="https://msdn.microsoft.com/2245d198-056c-467f-aae7-b1bb02f188e2">IWdsTransportCacheable</a> interface start with the <b>Dirty</b> property cleared. After any property is modified, <b>Dirty</b> is set to indicate that the object now contains changes not yet committed to its backing store. The <b>Dirty</b> property is cleared if the changes are committed or explicitly discarded via the appropriate methods.




## -see-also




<a href="https://msdn.microsoft.com/2245d198-056c-467f-aae7-b1bb02f188e2">IWdsTransportCacheable</a>
 

 

