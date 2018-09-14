---
UID: NF:wdstptmgmt.IWdsTransportCacheable.Commit
title: IWdsTransportCacheable::Commit
author: windows-sdk-content
description: Commits object data members to the underlying data store if the IWdsTransportCacheable::Dirty property has been set. Otherwise, the method returns with no action.
old-location: wds\iwdstransportcacheable_commit.htm
tech.root: wds
ms.assetid: bd651e56-3945-48ca-a490-e20db88eb2fb
ms.author: windowssdkdev
ms.date: 09/13/2018
ms.keywords: Commit, Commit method [Windows Deployment Services], Commit method [Windows Deployment Services],IWdsTransportCacheable interface, IWdsTransportCacheable interface [Windows Deployment Services],Commit method, IWdsTransportCacheable.Commit, IWdsTransportCacheable::Commit, wds.iwdstransportcacheable_commit, wdstptmgmt/IWdsTransportCacheable::Commit
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
 - IWdsTransportCacheable.Commit
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IWdsTransportCacheable::Commit


## -description


Commits object data members to the underlying data store if the <a href="https://msdn.microsoft.com/f73e3013-e060-45bc-987c-d41cd01beef7">IWdsTransportCacheable::Dirty</a> property has been set. Otherwise, the method returns with no action.


## -parameters






## -remarks



Upon successful completion, this method clears the <a href="https://msdn.microsoft.com/f73e3013-e060-45bc-987c-d41cd01beef7">Dirty</a> property.






## -see-also




<a href="https://msdn.microsoft.com/2245d198-056c-467f-aae7-b1bb02f188e2">IWdsTransportCacheable</a>
 

 

