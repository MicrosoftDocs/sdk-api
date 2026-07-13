---
UID: NS:dsclient.DOMAIN_TREE
title: DOMAIN_TREE (dsclient.h)
description: The DOMAINTREE structure contains data about a node in a domain tree obtained with the IDsBrowseDomainTree::GetDomains method. Each of the domains in the tree node are represented by a DOMAINDESC structure.
helpviewer_keywords: ["*LPDOMAINTREE","*PDOMAIN_TREE","DOMAINTREE","DOMAINTREE structure [Active Directory]","DOMAIN_TREE","DOMAIN_TREE structure [Active Directory]","LPDOMAINTREE","LPDOMAINTREE structure pointer [Active Directory]","PDOMAIN_TREE","PDOMAIN_TREE structure pointer [Active Directory]","_glines_domaintree","ad.domaintree","dsclient/DOMAINTREE","dsclient/DOMAIN_TREE","dsclient/LPDOMAINTREE","dsclient/PDOMAIN_TREE"]
old-location: ad\domaintree.htm
tech.root: ad
ms.assetid: c4b3f81c-0632-407c-834e-8eec6fefde68
ms.date: 12/05/2018
ms.keywords: '*LPDOMAINTREE, *PDOMAIN_TREE, DOMAINTREE, DOMAINTREE structure [Active Directory], DOMAIN_TREE, DOMAIN_TREE structure [Active Directory], LPDOMAINTREE, LPDOMAINTREE structure pointer [Active Directory], PDOMAIN_TREE, PDOMAIN_TREE structure pointer [Active Directory], _glines_domaintree, ad.domaintree, dsclient/DOMAINTREE, dsclient/DOMAIN_TREE, dsclient/LPDOMAINTREE, dsclient/PDOMAIN_TREE'
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
req.dll: 
req.irql: 
targetos: Windows
req.typenames: DOMAIN_TREE, DOMAINTREE, *PDOMAIN_TREE, *LPDOMAINTREE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - PDOMAIN_TREE
 - dsclient/PDOMAIN_TREE
 - DOMAIN_TREE
 - dsclient/DOMAIN_TREE
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Dsclient.h
api_name:
 - DOMAINTREE
---

# DOMAIN_TREE structure


## -description

The <b>DOMAINTREE</b> structure contains  data about a node in a domain tree obtained with the <a href="/windows/desktop/api/dsclient/nf-dsclient-idsbrowsedomaintree-getdomains">IDsBrowseDomainTree::GetDomains</a> method. Each of the domains in the tree  node are represented by a 
<a href="/windows/desktop/api/dsclient/ns-dsclient-domaindesc">DOMAINDESC</a> structure.

## -struct-fields

### -field dsSize

Contains the size, in bytes, of the <b>DOMAINTREE</b> structure and all <a href="/windows/desktop/api/dsclient/ns-dsclient-domaindesc">DOMAINDESC</a> structures in this <b>DOMAINTREE</b> structure.

### -field dwCount

Contains the number of  <a href="/windows/desktop/api/dsclient/ns-dsclient-domaindesc">DOMAINDESC</a> structures in the <b>aDomains</b> array.

### -field aDomains

Contains an array of <a href="/windows/desktop/api/dsclient/ns-dsclient-domaindesc">DOMAINDESC</a> structures that represent the domains. The array does not contain any child or sibling relational data. The relational data is contained within the <b>DOMAINDESC</b> structures.

## -remarks

For more information about how to access and use the data in this structure, see <a href="/windows/desktop/AD/domain-browser">Domain Browser</a>.

## -see-also

<a href="/windows/desktop/api/dsclient/ns-dsclient-domaindesc">DOMAINDESC</a>



<a href="/windows/desktop/AD/domain-browser">Domain Browser</a>



<a href="/windows/desktop/api/dsclient/nf-dsclient-idsbrowsedomaintree-freedomains">IDsBrowseDomainTree::FreeDomains</a>



<a href="/windows/desktop/api/dsclient/nf-dsclient-idsbrowsedomaintree-getdomains">IDsBrowseDomainTree::GetDomains</a>

