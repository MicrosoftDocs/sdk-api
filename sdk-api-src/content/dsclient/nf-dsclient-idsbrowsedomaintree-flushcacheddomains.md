---
UID: NF:dsclient.IDsBrowseDomainTree.FlushCachedDomains
title: IDsBrowseDomainTree::FlushCachedDomains
author: windows-sdk-content
description: The IDsBrowseDomainTree::FlushCachedDomains method frees the cached domain list.
old-location: ad\idsbrowsedomaintree_flushcacheddomains.htm
tech.root: AD
ms.assetid: e6f4dbbb-5e2f-470a-bfc0-5bb6e96c7a6c
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: FlushCachedDomains, FlushCachedDomains method [Active Directory], FlushCachedDomains method [Active Directory],IDsBrowseDomainTree interface, IDsBrowseDomainTree interface [Active Directory],FlushCachedDomains method, IDsBrowseDomainTree.FlushCachedDomains, IDsBrowseDomainTree::FlushCachedDomains, _glines_idsbrowsedomaintree_flushcacheddomains, ad.idsbrowsedomaintree__flushcacheddomains, ad.idsbrowsedomaintree_flushcacheddomains, dsclient/IDsBrowseDomainTree::FlushCachedDomains
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: dsclient.h
req.include-header: 
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
req.lib: 
req.dll: Dsadmin.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Dsadmin.dll
api_name:
 - IDsBrowseDomainTree.FlushCachedDomains
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDsBrowseDomainTree::FlushCachedDomains


## -description


The <b>IDsBrowseDomainTree::FlushCachedDomains</b> method frees the cached domain list.


## -parameters






## -returns



Returns a standard <b>HRESULT</b> value including the following.




## -remarks



This method frees the internal cached domain data. This method must  be called before calling 
<a href="https://msdn.microsoft.com/1e070673-ce8d-4f68-a066-5baf38180745">IDsBrowseDomainTree::SetComputer</a> to retarget to a computer of a different domain.




## -see-also




<a href="https://msdn.microsoft.com/f50caa34-d29e-4ad1-98b0-ef5c1f5550bf">IDsBrowseDomainTree</a>



<a href="https://msdn.microsoft.com/1e070673-ce8d-4f68-a066-5baf38180745">IDsBrowseDomainTree::SetComputer</a>
 

 

