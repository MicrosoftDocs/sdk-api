---
UID: NN:certpol.INDESPolicy
title: INDESPolicy
author: windows-sdk-content
description: The NDES Policy Module Interface. When installed against an enterprise CA, NDES generates a password after checking that the user has enrollment permission on the configured NDES templates, both user and machine templates.
old-location: security\indespolicy.htm
tech.root: seccrypto
ms.assetid: 9ed31493-832a-4f66-bb95-02ef1ad7ca15
ms.author: windowssdkdev
ms.date: 10/01/2018
ms.keywords: INDESPolicy, INDESPolicy interface [Security], INDESPolicy interface [Security],described, certpol/INDESPolicy, security.indespolicy
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# INDESPolicy interface


## -description


The NDES Policy Module Interface.  When installed against an enterprise CA, NDES generates a password after checking that the user has enrollment permission on the configured NDES templates, both user and machine templates.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">INDESPolicy</b> interface inherits from the <a href="https://msdn.microsoft.com/en-us/library/ms680509(v=VS.85).aspx">IUnknown</a> interface. <b>INDESPolicy</b> also has these types of members:
<ul>
<li><a href="https://msdn.microsoft.com/en-us/library/ms684591(v=VS.85).aspx">Methods</a></li>
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
<a href="https://msdn.microsoft.com/en-us/library/Dn383667(v=VS.85).aspx">GenerateChallenge</a>
</td>
<td align="left" width="63%">
Performs the policy decision whether to issue a challenge password to the SCEP client.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dn383668(v=VS.85).aspx">Initialize</a>
</td>
<td align="left" width="63%">
Initializes the NDES policy module.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dn383670(v=VS.85).aspx">Notify</a>
</td>
<td align="left" width="63%">
Notifies the plug-in of the transaction status of the SCEP certificate request.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dn383671(v=VS.85).aspx">Uninitialize</a>
</td>
<td align="left" width="63%">
Uninitializes the NDES policy module.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dn383672(v=VS.85).aspx">VerifyRequest</a>
</td>
<td align="left" width="63%">
Verifies the NDES certificate request for submission to the CA.

</td>
</tr>
</table> 

