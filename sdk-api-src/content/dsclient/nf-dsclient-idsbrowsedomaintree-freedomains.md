---
UID: NF:dsclient.IDsBrowseDomainTree.FreeDomains
title: IDsBrowseDomainTree::FreeDomains (dsclient.h)
description: The IDsBrowseDomainTree::FreeDomains method frees the memory allocated by the IDsBrowseDomainTree::GetDomains method.helpviewer_keywords: ["FreeDomains","FreeDomains method [Active Directory]","FreeDomains method [Active Directory]","IDsBrowseDomainTree interface","IDsBrowseDomainTree interface [Active Directory]","FreeDomains method","IDsBrowseDomainTree.FreeDomains","IDsBrowseDomainTree::FreeDomains","_glines_idsbrowsedomaintree_freedomains","ad.idsbrowsedomaintree__freedomains","ad.idsbrowsedomaintree_freedomains","dsclient/IDsBrowseDomainTree::FreeDomains"]
old-location: ad\idsbrowsedomaintree_freedomains.htm
tech.root: ad
ms.assetid: d9334f4c-d5b0-445a-ad1b-8628f206b715
ms.date: 12/05/2018
ms.keywords: FreeDomains, FreeDomains method [Active Directory], FreeDomains method [Active Directory],IDsBrowseDomainTree interface, IDsBrowseDomainTree interface [Active Directory],FreeDomains method, IDsBrowseDomainTree.FreeDomains, IDsBrowseDomainTree::FreeDomains, _glines_idsbrowsedomaintree_freedomains, ad.idsbrowsedomaintree__freedomains, ad.idsbrowsedomaintree_freedomains, dsclient/IDsBrowseDomainTree::FreeDomains
f1_keywords:
- dsclient/IDsBrowseDomainTree.FreeDomains
dev_langs:
- c++
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
- IDsBrowseDomainTree.FreeDomains
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IDsBrowseDomainTree::FreeDomains


## -description


The <b>IDsBrowseDomainTree::FreeDomains</b> method frees the memory allocated by the <a href="https://docs.microsoft.com/windows/desktop/api/dsclient/nf-dsclient-idsbrowsedomaintree-getdomains">IDsBrowseDomainTree::GetDomains</a> method.


## -parameters




### -param ppDomainTree [in]

Pointer to the 
<a href="https://docs.microsoft.com/windows/desktop/api/dsclient/ns-dsclient-domain_tree">DOMAINTREE</a> data structure.


## -returns



Returns a standard <b>HRESULT</b> value including the following.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/dsclient/nn-dsclient-idsbrowsedomaintree">IDsBrowseDomainTree</a>



<a href="https://docs.microsoft.com/windows/desktop/api/dsclient/nf-dsclient-idsbrowsedomaintree-getdomains">IDsBrowseDomainTree::GetDomains</a>
 

 

