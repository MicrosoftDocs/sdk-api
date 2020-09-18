---
UID: NF:dsclient.IDsBrowseDomainTree.SetComputer
title: IDsBrowseDomainTree::SetComputer (dsclient.h)
description: Specifies the computer and credentials to be used by this instance of the IDsBrowseDomainTree interface.
helpviewer_keywords: ["IDsBrowseDomainTree interface [Active Directory]","SetComputer method","IDsBrowseDomainTree.SetComputer","IDsBrowseDomainTree::SetComputer","SetComputer","SetComputer method [Active Directory]","SetComputer method [Active Directory]","IDsBrowseDomainTree interface","_glines_idsbrowsedomaintree_setcomputer","ad.idsbrowsedomaintree__setcomputer","ad.idsbrowsedomaintree_setcomputer","dsclient/IDsBrowseDomainTree::SetComputer"]
old-location: ad\idsbrowsedomaintree_setcomputer.htm
tech.root: ad
ms.assetid: 1e070673-ce8d-4f68-a066-5baf38180745
ms.date: 12/05/2018
ms.keywords: IDsBrowseDomainTree interface [Active Directory],SetComputer method, IDsBrowseDomainTree.SetComputer, IDsBrowseDomainTree::SetComputer, SetComputer, SetComputer method [Active Directory], SetComputer method [Active Directory],IDsBrowseDomainTree interface, _glines_idsbrowsedomaintree_setcomputer, ad.idsbrowsedomaintree__setcomputer, ad.idsbrowsedomaintree_setcomputer, dsclient/IDsBrowseDomainTree::SetComputer
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
 - IDsBrowseDomainTree::SetComputer
 - dsclient/IDsBrowseDomainTree::SetComputer
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
 - IDsBrowseDomainTree.SetComputer
---

# IDsBrowseDomainTree::SetComputer


## -description

The <b>IDsBrowseDomainTree::SetComputer</b> method specifies the computer and credentials to be used by this instance of the <a href="/windows/desktop/api/dsclient/nn-dsclient-idsbrowsedomaintree">IDsBrowseDomainTree</a> interface.

## -parameters

### -param pszComputerName [in]

Pointer to a null-terminated Unicode string that contains the name of the target computer.

### -param pszUserName [in]

Pointer to a null-terminated Unicode string that contains the user name used to access the  computer.

### -param pszPassword [in]

Pointer to a null-terminated Unicode string that contains the password used to access the  computer.

## -returns

Returns a standard <b>HRESULT</b> value including the following.

## -remarks

If this method is not called, the local host is assumed as the default computer.

When <b>SetComputer</b> is called on a particular <a href="/windows/desktop/api/dsclient/nn-dsclient-idsbrowsedomaintree">IDsBrowseDomainTree</a> instance, <a href="/windows/desktop/api/dsclient/nf-dsclient-idsbrowsedomaintree-flushcacheddomains">IDsBrowseDomainTree::FlushCachedDomains</a> must be called before <b>SetComputer</b> is called again.

## -see-also

<a href="/windows/desktop/api/dsclient/nn-dsclient-idsbrowsedomaintree">IDsBrowseDomainTree</a>



<a href="/windows/desktop/api/dsclient/nf-dsclient-idsbrowsedomaintree-flushcacheddomains">IDsBrowseDomainTree::FlushCachedDomains</a>