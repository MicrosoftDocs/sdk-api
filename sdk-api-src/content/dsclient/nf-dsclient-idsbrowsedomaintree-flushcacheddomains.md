---
UID: NF:dsclient.IDsBrowseDomainTree.FlushCachedDomains
title: IDsBrowseDomainTree::FlushCachedDomains (dsclient.h)
description: The IDsBrowseDomainTree::FlushCachedDomains method frees the cached domain list.
helpviewer_keywords: ["FlushCachedDomains","FlushCachedDomains method [Active Directory]","FlushCachedDomains method [Active Directory]","IDsBrowseDomainTree interface","IDsBrowseDomainTree interface [Active Directory]","FlushCachedDomains method","IDsBrowseDomainTree.FlushCachedDomains","IDsBrowseDomainTree::FlushCachedDomains","_glines_idsbrowsedomaintree_flushcacheddomains","ad.idsbrowsedomaintree__flushcacheddomains","ad.idsbrowsedomaintree_flushcacheddomains","dsclient/IDsBrowseDomainTree::FlushCachedDomains"]
old-location: ad\idsbrowsedomaintree_flushcacheddomains.htm
tech.root: ad
ms.assetid: e6f4dbbb-5e2f-470a-bfc0-5bb6e96c7a6c
ms.date: 12/05/2018
ms.keywords: FlushCachedDomains, FlushCachedDomains method [Active Directory], FlushCachedDomains method [Active Directory],IDsBrowseDomainTree interface, IDsBrowseDomainTree interface [Active Directory],FlushCachedDomains method, IDsBrowseDomainTree.FlushCachedDomains, IDsBrowseDomainTree::FlushCachedDomains, _glines_idsbrowsedomaintree_flushcacheddomains, ad.idsbrowsedomaintree__flushcacheddomains, ad.idsbrowsedomaintree_flushcacheddomains, dsclient/IDsBrowseDomainTree::FlushCachedDomains
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IDsBrowseDomainTree::FlushCachedDomains
 - dsclient/IDsBrowseDomainTree::FlushCachedDomains
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Dsadmin.dll
api_name:
 - IDsBrowseDomainTree.FlushCachedDomains
---

# IDsBrowseDomainTree::FlushCachedDomains


## -description

The <b>IDsBrowseDomainTree::FlushCachedDomains</b> method frees the cached domain list.



## -returns

Returns a standard <b>HRESULT</b> value including the following.

## -remarks

This method frees the internal cached domain data. This method must  be called before calling 
<a href="/windows/desktop/api/dsclient/nf-dsclient-idsbrowsedomaintree-setcomputer">IDsBrowseDomainTree::SetComputer</a> to retarget to a computer of a different domain.

## -see-also

<a href="/windows/desktop/api/dsclient/nn-dsclient-idsbrowsedomaintree">IDsBrowseDomainTree</a>



<a href="/windows/desktop/api/dsclient/nf-dsclient-idsbrowsedomaintree-setcomputer">IDsBrowseDomainTree::SetComputer</a>
