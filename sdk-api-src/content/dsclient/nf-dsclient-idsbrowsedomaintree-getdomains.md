---
UID: NF:dsclient.IDsBrowseDomainTree.GetDomains
title: IDsBrowseDomainTree::GetDomains (dsclient.h)
description: The IDsBrowseDomainTree::GetDomains method retrieves the trust domains of the current computer. The current computer is set using the IDsBrowseDomainTree::SetComputer method.
helpviewer_keywords: ["DBDTF_RETURNEXTERNAL","DBDTF_RETURNFQDN","DBDTF_RETURNINBOUND","DBDTF_RETURNINOUTBOUND","DBDTF_RETURNMIXEDDOMAINS","GetDomains","GetDomains method [Active Directory]","GetDomains method [Active Directory]","IDsBrowseDomainTree interface","IDsBrowseDomainTree interface [Active Directory]","GetDomains method","IDsBrowseDomainTree.GetDomains","IDsBrowseDomainTree::GetDomains","_glines_idsbrowsedomaintree_getdomains","ad.idsbrowsedomaintree__getdomains","ad.idsbrowsedomaintree_getdomains","dsclient/IDsBrowseDomainTree::GetDomains"]
old-location: ad\idsbrowsedomaintree_getdomains.htm
tech.root: ad
ms.assetid: 42cd38c2-7470-49b5-9b64-d971f2a915c6
ms.date: 12/05/2018
ms.keywords: DBDTF_RETURNEXTERNAL, DBDTF_RETURNFQDN, DBDTF_RETURNINBOUND, DBDTF_RETURNINOUTBOUND, DBDTF_RETURNMIXEDDOMAINS, GetDomains, GetDomains method [Active Directory], GetDomains method [Active Directory],IDsBrowseDomainTree interface, IDsBrowseDomainTree interface [Active Directory],GetDomains method, IDsBrowseDomainTree.GetDomains, IDsBrowseDomainTree::GetDomains, _glines_idsbrowsedomaintree_getdomains, ad.idsbrowsedomaintree__getdomains, ad.idsbrowsedomaintree_getdomains, dsclient/IDsBrowseDomainTree::GetDomains
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
 - IDsBrowseDomainTree::GetDomains
 - dsclient/IDsBrowseDomainTree::GetDomains
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
 - IDsBrowseDomainTree.GetDomains
---

# IDsBrowseDomainTree::GetDomains


## -description

The <b>IDsBrowseDomainTree::GetDomains</b> method retrieves the trust domains of the current computer.
  The current computer is set using the <a href="/windows/desktop/api/dsclient/nf-dsclient-idsbrowsedomaintree-setcomputer">IDsBrowseDomainTree::SetComputer</a> method.

## -parameters

### -param ppDomainTree [in]

Pointer to a <a href="/windows/desktop/api/dsclient/ns-dsclient-domain_tree">DOMAINTREE</a> structure pointer that receives the trust domain data. The caller must free this memory when no longer required by calling <a href="/windows/desktop/api/dsclient/nf-dsclient-idsbrowsedomaintree-freedomains">IDsBrowseDomainTree::FreeDomains</a>.

### -param dwFlags [in]

Contains a set of flags that modify the domain contents. This can be zero or a combination of one or more of the following values.



#### DBDTF_RETURNFQDN

The <b>pszNCName</b> members of the <a href="/windows/desktop/api/dsclient/ns-dsclient-domaindesc">DOMAINDESC</a> structures will receive the fully qualified domain names. The fully qualified domain name takes the form "DC=myDom, DC=Fabrikam, DC=com" as opposed to "myDom.Fabrikam.com".



#### DBDTF_RETURNMIXEDDOMAINS

The method will return downlevel trust domains.



#### DBDTF_RETURNEXTERNAL

The method will return external trust domains.



#### DBDTF_RETURNINBOUND

If this flag is set, the method returns trusting domains. If this flag is not set, the method returns trusted domains.



#### DBDTF_RETURNINOUTBOUND

The method will return both trusted and trusting domains.

## -returns

Returns a standard <b>HRESULT</b> value including the following.

## -remarks

For more information about how to access and use the data provided by this method, see <a href="/windows/desktop/AD/domain-browser">Domain Browser</a>.

## -see-also

<a href="/windows/desktop/api/dsclient/ns-dsclient-domaindesc">DOMAINDESC</a>



<a href="/windows/desktop/api/dsclient/ns-dsclient-domain_tree">DOMAINTREE</a>



<a href="/windows/desktop/AD/domain-browser">Domain Browser</a>



<a href="/windows/desktop/api/dsclient/nn-dsclient-idsbrowsedomaintree">IDsBrowseDomainTree</a>



<a href="/windows/desktop/api/dsclient/nf-dsclient-idsbrowsedomaintree-freedomains">IDsBrowseDomainTree::FreeDomains</a>