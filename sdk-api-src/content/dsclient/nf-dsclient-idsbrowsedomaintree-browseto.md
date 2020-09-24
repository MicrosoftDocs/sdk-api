---
UID: NF:dsclient.IDsBrowseDomainTree.BrowseTo
title: IDsBrowseDomainTree::BrowseTo (dsclient.h)
description: The IDsBrowseDomainTree::BrowseTo method displays a dialog box used to browse for a domain.
helpviewer_keywords: ["BrowseTo","BrowseTo method [Active Directory]","BrowseTo method [Active Directory]","IDsBrowseDomainTree interface","DBDTF_RETURNEXTERNAL","DBDTF_RETURNFQDN","DBDTF_RETURNINBOUND","DBDTF_RETURNINOUTBOUND","DBDTF_RETURNMIXEDDOMAINS","IDsBrowseDomainTree interface [Active Directory]","BrowseTo method","IDsBrowseDomainTree.BrowseTo","IDsBrowseDomainTree::BrowseTo","_glines_idsbrowsedomaintree_browseto","ad.idsbrowsedomaintree__browseto","ad.idsbrowsedomaintree_browseto","dsclient/IDsBrowseDomainTree::BrowseTo"]
old-location: ad\idsbrowsedomaintree_browseto.htm
tech.root: ad
ms.assetid: 22b719fc-bd46-44c6-a690-af6e9767f9ce
ms.date: 12/05/2018
ms.keywords: BrowseTo, BrowseTo method [Active Directory], BrowseTo method [Active Directory],IDsBrowseDomainTree interface, DBDTF_RETURNEXTERNAL, DBDTF_RETURNFQDN, DBDTF_RETURNINBOUND, DBDTF_RETURNINOUTBOUND, DBDTF_RETURNMIXEDDOMAINS, IDsBrowseDomainTree interface [Active Directory],BrowseTo method, IDsBrowseDomainTree.BrowseTo, IDsBrowseDomainTree::BrowseTo, _glines_idsbrowsedomaintree_browseto, ad.idsbrowsedomaintree__browseto, ad.idsbrowsedomaintree_browseto, dsclient/IDsBrowseDomainTree::BrowseTo
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
 - IDsBrowseDomainTree::BrowseTo
 - dsclient/IDsBrowseDomainTree::BrowseTo
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
 - IDsBrowseDomainTree.BrowseTo
---

# IDsBrowseDomainTree::BrowseTo


## -description

The <b>IDsBrowseDomainTree::BrowseTo</b> method displays a dialog box used to browse for a domain.

## -parameters

### -param hwndParent [in]

Handle of the window that will be the owner of the domain browser dialog box.

### -param ppszTargetPath [out]

Pointer to a Unicode string pointer that receives the path string of the domain selected in the domain browser. This memory must be freed when it is no longer required by calling <a href="/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree">CoTaskMemFree</a>. By default, this path takes the form "myDom.Fabrikam.com". If <i>dwFlags</i> contains the <b>DBDTF_RETURNFQDN</b> flag, the path takes the form "DC=myDom, DC=Fabrikam, DC=com".

### -param dwFlags [in]

Contains a set of flags that modify the behavior of the domain browser dialog box. This can be zero or a combination of one or more of the following values.



#### DBDTF_RETURNFQDN

The domain browser will place the fully qualified domain name in <i>ppszTargetPath</i>. The fully qualified domain name takes the form "DC=myDom, DC=Fabrikam, DC=com" as opposed to "myDom.Fabrikam.com".



#### DBDTF_RETURNMIXEDDOMAINS

The domain browser will display downlevel trust domains.



#### DBDTF_RETURNEXTERNAL

The domain browser will display external trust domains.



#### DBDTF_RETURNINBOUND

If this flag is set, the domain browser will display trusting domains. Otherwise, the domain browser will display trusted domains.



#### DBDTF_RETURNINOUTBOUND

The domain browser will display both trusted and trusting domains.

## -returns

Returns a standard <b>HRESULT</b> value including the following.

## -see-also

<a href="/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree">CoTaskMemFree</a>



<a href="/windows/desktop/api/dsclient/nn-dsclient-idsbrowsedomaintree">IDsBrowseDomainTree</a>