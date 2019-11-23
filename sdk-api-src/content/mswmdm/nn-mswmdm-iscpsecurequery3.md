---
UID: NN:mswmdm.ISCPSecureQuery3
title: ISCPSecureQuery3 (mswmdm.h)

description: The ISCPSecureQuery3 interface extends ISCPSecureQuery2 by providing a set of new methods for retrieving the rights and making decision on a clear channel.
old-location: wmdm\iscpsecurequery3.htm
tech.root: WMDM
ms.assetid: 3d600ae9-5d5b-48f6-a162-e52f78beb983

ms.date: 12/05/2018
ms.keywords: ISCPSecureQuery3, ISCPSecureQuery3 interface [windows Media Device Manager], ISCPSecureQuery3 interface [windows Media Device Manager],described, ISCPSecureQuery3Interface, mswmdm/ISCPSecureQuery3, wmdm.iscpsecurequery3
ms.topic: interface
f1_keywords: 
 - "mswmdm/ISCPSecureQuery3"
dev_langs:
 - c++
req.header: mswmdm.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
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
 - mswmdm.h
api_name:
 - ISCPSecureQuery3
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ISCPSecureQuery3 interface


## -description



The <b>ISCPSecureQuery3</b> interface extends <a href="https://docs.microsoft.com/windows/desktop/api/mswmdm/nn-mswmdm-iscpsecurequery2">ISCPSecureQuery2</a> by providing a set of new methods for retrieving the rights and making decision on a clear channel. These methods are more efficient because they do not involve encrypting and decrypting of parameters, which happens on a secure channel.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ISCPSecureQuery3</b> interface inherits from <a href="https://docs.microsoft.com/windows/desktop/api/mswmdm/nn-mswmdm-iscpsecurequery2">ISCPSecureQuery2</a>. <b>ISCPSecureQuery3</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ISCPSecureQuery3</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mswmdm/nf-mswmdm-iscpsecurequery3-getrightsonclearchannel">GetRightsOnClearChannel</a>
</td>
<td align="left" width="63%">
Retrieves the rights on a clear channel.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mswmdm/nf-mswmdm-iscpsecurequery3-makedecisiononclearchannel">MakeDecisionOnClearChannel</a>
</td>
<td align="left" width="63%">
Makes decisions on a clear channel.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/mswmdm/nn-mswmdm-iscpsecurequery">ISCPSecureQuery Interface</a>



<a href="https://docs.microsoft.com/windows/desktop/api/mswmdm/nn-mswmdm-iscpsecurequery2">ISCPSecureQuery2 Interface</a>



<a href="https://docs.microsoft.com/windows/desktop/WMDM/interfaces-for-secure-content-providers">Interfaces for Secure Content Providers</a>
 

 

