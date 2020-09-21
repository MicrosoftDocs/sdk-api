---
UID: NS:dsclient._DOMAINDESC
title: DOMAINDESC (dsclient.h)
description: Contains data about an element in a domain tree obtained with the IDsBrowseDomainTree::GetDomains method.
helpviewer_keywords: ["*LPDOMAINDESC","*PDOMAIN_DESC","DOMAINDESC","DOMAINDESC structure [Active Directory]","DOMAIN_DESC","DOMAIN_DESC structure [Active Directory]","LPDOMAINDESC","LPDOMAINDESC structure pointer [Active Directory]","PDOMAIN_DESC","PDOMAIN_DESC structure pointer [Active Directory]","_glines_domaindesc","ad.domaindesc","dsclient/DOMAINDESC","dsclient/LPDOMAINDESC","dsclient/PDOMAIN_DESC"]
old-location: ad\domaindesc.htm
tech.root: ad
ms.assetid: c788d106-2cc7-4d67-8568-23e858c0075f
ms.date: 12/05/2018
ms.keywords: '*LPDOMAINDESC, *PDOMAIN_DESC, DOMAINDESC, DOMAINDESC structure [Active Directory], DOMAIN_DESC, DOMAIN_DESC structure [Active Directory], LPDOMAINDESC, LPDOMAINDESC structure pointer [Active Directory], PDOMAIN_DESC, PDOMAIN_DESC structure pointer [Active Directory], _glines_domaindesc, ad.domaindesc, dsclient/DOMAINDESC, dsclient/LPDOMAINDESC, dsclient/PDOMAIN_DESC'
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
req.typenames: DOMAIN_DESC, DOMAINDESC, *PDOMAIN_DESC, *LPDOMAINDESC
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _DOMAINDESC
 - dsclient/_DOMAINDESC
 - PDOMAIN_DESC
 - dsclient/PDOMAIN_DESC
 - DOMAINDESC
 - dsclient/DOMAINDESC
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
 - DOMAIN_DESC
---

# DOMAINDESC structure


## -description

The <b>DOMAINDESC</b> structure contains data about an element in a domain tree obtained with the <a href="/windows/desktop/api/dsclient/nf-dsclient-idsbrowsedomaintree-getdomains">IDsBrowseDomainTree::GetDomains</a> method. This structure is contained in the <a href="/windows/desktop/api/dsclient/ns-dsclient-domain_tree">DOMAINTREE</a> structure.

## -struct-fields

### -field pszName

Pointer to a Unicode string that contains the domain name.

### -field pszPath

Pointer to a Unicode string that contains the path of the domain. Reserved.

### -field pszNCName

Pointer to a Unicode string that contains the fully qualified name of the domain in the form "DC=myDom, DC=Fabrikam, DC=com". This member is  blank if the <b>DBDTF_RETURNFQDN</b> flag is not set in the <i>dwFlags</i> parameter in <a href="/windows/desktop/api/dsclient/nf-dsclient-idsbrowsedomaintree-getdomains">IDsBrowseDomainTree::GetDomains</a>.

### -field pszTrustParent

Pointer to a Unicode string that contains the name of the parent domain. This member is <b>NULL</b> if the domain has no parent.

### -field pszObjectClass

Pointer to a Unicode string that contains the object class name of the domain.

### -field ulFlags

Contains a set of flags that specify the attributes of the trust. For more information, and a list of possible values, see the <i>Flags</i> parameter of <a href="/windows/desktop/api/dsgetdc/nf-dsgetdc-dsenumeratedomaintrustsa">DsEnumerateDomainTrusts</a>.

### -field fDownLevel

Contains a nonzero value if the domain is a down-level domain or zero otherwise.

### -field pdChildList

Contains a pointer to a <b>DOMAINDESC</b> structure that represents the first child of the domain. Obtain subsequent children by accessing the <b>pdNextSibling</b> member of the child structure. This member is <b>NULL</b> if the domain has no children.

### -field pdNextSibling

Contains a pointer to a <b>DOMAINDESC</b> structure that represents the next sibling of the domain. Obtain subsequent siblings by accessing the <b>pdNextSibling</b> member of the sibling structure. This member is <b>NULL</b> if the domain has no siblings.

## -remarks

For more information about how to access and use the information in this structure, see <a href="/windows/desktop/AD/domain-browser">Domain Browser</a>.

## -see-also

<a href="/windows/desktop/api/dsclient/ns-dsclient-domain_tree">DOMAINTREE</a>



<a href="/windows/desktop/AD/display-structures-in-active-directory-domain-services">Display Structures in Active Directory Domain Services</a>



<a href="/windows/desktop/AD/domain-browser">Domain Browser</a>



<a href="/windows/desktop/api/dsgetdc/nf-dsgetdc-dsenumeratedomaintrustsa">DsEnumerateDomainTrusts</a>