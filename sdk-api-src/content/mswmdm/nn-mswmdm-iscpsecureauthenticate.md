---
UID: NN:mswmdm.ISCPSecureAuthenticate
title: ISCPSecureAuthenticate (mswmdm.h)
description: The ISCPSecureAuthenticate interface is the primary interface of the secure content provider, which Windows Media Device Manager queries to authenticate the secure content provider and to be authenticated by the secure content provider.
old-location: wmdm\iscpsecureauthenticate.htm
tech.root: WMDM
ms.assetid: dfe37b41-f80b-4992-84c1-c23581cc4b69
ms.date: 12/05/2018
ms.keywords: ISCPSecureAuthenticate, ISCPSecureAuthenticate interface [windows Media Device Manager], ISCPSecureAuthenticate interface [windows Media Device Manager],described, ISCPSecureAuthenticateInterface, mswmdm/ISCPSecureAuthenticate, wmdm.iscpsecureauthenticate
ms.topic: interface
f1_keywords:
- mswmdm/ISCPSecureAuthenticate
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
- ISCPSecureAuthenticate
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ISCPSecureAuthenticate interface


## -description



The <b>ISCPSecureAuthenticate</b> interface is the primary interface of the secure content provider, which Windows Media Device Manager queries to authenticate the secure content provider and to be authenticated by the secure content provider. This interface is used to pass information about the content to the secure content provider module, which the provider uses to report back whether it is responsible for the content. Windows Media Device Manager consults this interface whenever an application downloads content to a media device.

The secure content provider implements this interface, and Windows Media Device Manager calls its methods.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ISCPSecureAuthenticate</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>ISCPSecureAuthenticate</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ISCPSecureAuthenticate</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mswmdm/nf-mswmdm-iscpsecureauthenticate-getsecurequery">GetSecureQuery</a>
</td>
<td align="left" width="63%">
Gets a pointer to an <a href="https://docs.microsoft.com/windows/desktop/api/mswmdm/nn-mswmdm-iscpsecurequery">ISCPSecureQuery</a> interface.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/mswmdm/nn-mswmdm-iscpsecurequery">ISCPSecureQuery Interface</a>



<a href="https://docs.microsoft.com/windows/desktop/WMDM/interfaces-for-secure-content-providers">Interfaces for Secure Content Providers</a>
 

 

