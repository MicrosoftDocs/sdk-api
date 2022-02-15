---
UID: NN:dsclient.IDsBrowseDomainTree
title: IDsBrowseDomainTree (dsclient.h)
description: The IDsBrowseDomainTree interface is used by an application to display a domain browser dialog box and/or obtain a list of trust domains related to a given computer.
helpviewer_keywords: ["IDsBrowseDomainTree","IDsBrowseDomainTree interface [Active Directory]","IDsBrowseDomainTree interface [Active Directory]","described","_glines_idsbrowsedomaintree","ad.idsbrowsedomaintree","dsclient/IDsBrowseDomainTree"]
old-location: ad\idsbrowsedomaintree.htm
tech.root: ad
ms.assetid: f50caa34-d29e-4ad1-98b0-ef5c1f5550bf
ms.date: 12/05/2018
ms.keywords: IDsBrowseDomainTree, IDsBrowseDomainTree interface [Active Directory], IDsBrowseDomainTree interface [Active Directory],described, _glines_idsbrowsedomaintree, ad.idsbrowsedomaintree, dsclient/IDsBrowseDomainTree
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
 - IDsBrowseDomainTree
 - dsclient/IDsBrowseDomainTree
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
 - IDsBrowseDomainTree
---

# IDsBrowseDomainTree interface


## -description

The <b>IDsBrowseDomainTree</b> interface is used by an application to display a domain browser dialog box and/or obtain a list of trust domains related to a given computer.

## -inheritance

The <b>IDsBrowseDomainTree</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IDsBrowseDomainTree</b> also has these types of members:

## -remarks

An instance of this interface is created by calling <a href="/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance">CoCreateInstance</a> with the <b>CLSID_DsDomainTreeBrowser</b> class identifier as shown below.


```cpp
HRESULT hr = S_OK;
IDsBrowseDomainTree *pDSB = NULL;

hr = CoCreateInstance(    CLSID_DsDomainTreeBrowser,
                          NULL,
                          CLSCTX_INPROC_SERVER,
                          IID_IDsBrowseDomainTree,
                          (void**)&pDSB);

if(SUCCEEDED(hr))
{
    //use the IDsBrowseDomainTree object

    //release the IDsBrowseDomainTree object
    pDSB->Release();
}
```

## -see-also

<a href="/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance">CoCreateInstance</a>
