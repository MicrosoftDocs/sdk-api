---
UID: NN:identityprovider.IIdentityAdvise
title: IIdentityAdvise (identityprovider.h)

description: Allows an identity provider to notify a calling application when an identity is updated.
old-location: security\iidentityadvise.htm
tech.root: SecAuthN
ms.assetid: fa348d46-bcd2-4009-89d6-11e738d4a82b

ms.date: 12/05/2018
ms.keywords: IIdentityAdvise, IIdentityAdvise interface [Security], IIdentityAdvise interface [Security],described, identityprovider/IIdentityAdvise, identitystore/IIdentityAdvise, security.iidentityadvise
ms.topic: interface
f1_keywords: 
 - "identityprovider/IIdentityAdvise"
dev_langs:
 - c++
req.header: identityprovider.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - IdentityProvider.h
 - Identitystore.h
api_name:
 - IIdentityAdvise
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IIdentityAdvise interface


## -description


The <b>IIdentityAdvise</b> interface allows an identity provider to notify a calling application when an identity is updated.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IIdentityAdvise</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IIdentityAdvise</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IIdentityAdvise</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/identityprovider/nf-identityprovider-iidentityadvise-identityupdated">IdentityUpdated</a>
</td>
<td align="left" width="63%">
Is called by an identity provider to notify a calling application that an identity event occurred.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/identityprovider/nn-identityprovider-iidentityprovider">IIdentityProvider</a>



<a href="https://docs.microsoft.com/windows/desktop/api/identityprovider/nf-identityprovider-iidentityprovider-advise">IIdentityProvider::Advise</a>
 

 

