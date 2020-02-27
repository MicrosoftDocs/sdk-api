---
UID: NN:certpol.INDESPolicy
title: INDESPolicy (certpol.h)
description: The NDES Policy Module Interface. When installed against an enterprise CA, NDES generates a password after checking that the user has enrollment permission on the configured NDES templates, both user and machine templates.
old-location: security\indespolicy.htm
tech.root: SecCrypto
ms.assetid: 9ed31493-832a-4f66-bb95-02ef1ad7ca15
ms.date: 12/05/2018
ms.keywords: INDESPolicy, INDESPolicy interface [Security], INDESPolicy interface [Security],described, certpol/INDESPolicy, security.indespolicy
f1_keywords:
- certpol/INDESPolicy
dev_langs:
- c++
req.header: certpol.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Certpol.idl
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
- certpol.h
api_name:
- INDESPolicy
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# INDESPolicy interface


## -description


The NDES Policy Module Interface.  When installed against an enterprise CA, NDES generates a password after checking that the user has enrollment permission on the configured NDES templates, both user and machine templates.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">INDESPolicy</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>INDESPolicy</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>INDESPolicy</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/certpol/nf-certpol-indespolicy-generatechallenge">GenerateChallenge</a>
</td>
<td align="left" width="63%">
Performs the policy decision whether to issue a challenge password to the SCEP client.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/certpol/nf-certpol-indespolicy-initialize">Initialize</a>
</td>
<td align="left" width="63%">
Initializes the NDES policy module.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/certpol/nf-certpol-indespolicy-notify">Notify</a>
</td>
<td align="left" width="63%">
Notifies the plug-in of the transaction status of the SCEP certificate request.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/certpol/nf-certpol-indespolicy-uninitialize">Uninitialize</a>
</td>
<td align="left" width="63%">
Uninitializes the NDES policy module.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/certpol/nf-certpol-indespolicy-verifyrequest">VerifyRequest</a>
</td>
<td align="left" width="63%">
Verifies the NDES certificate request for submission to the CA.

</td>
</tr>
</table> 

