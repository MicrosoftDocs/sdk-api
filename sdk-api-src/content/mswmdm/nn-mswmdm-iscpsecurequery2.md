---
UID: NN:mswmdm.ISCPSecureQuery2
title: ISCPSecureQuery2 (mswmdm.h)
description: The ISCPSecureQuery2 interface extends ISCPSecureQuery through functionality that determines whether the secure content provider is responsible for the content, and if so, providing a URL for updating revoked components and determining which components have been revoked.helpviewer_keywords: ["ISCPSecureQuery2","ISCPSecureQuery2 interface [windows Media Device Manager]","ISCPSecureQuery2 interface [windows Media Device Manager]","described","ISCPSecureQuery2Interface","mswmdm/ISCPSecureQuery2","wmdm.iscpsecurequery2"]
old-location: wmdm\iscpsecurequery2.htm
tech.root: WMDM
ms.assetid: fe5ae201-355d-4402-8d57-a721aecfdbde
ms.date: 12/05/2018
ms.keywords: ISCPSecureQuery2, ISCPSecureQuery2 interface [windows Media Device Manager], ISCPSecureQuery2 interface [windows Media Device Manager],described, ISCPSecureQuery2Interface, mswmdm/ISCPSecureQuery2, wmdm.iscpsecurequery2
f1_keywords:
- mswmdm/ISCPSecureQuery2
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
- ISCPSecureQuery2
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ISCPSecureQuery2 interface


## -description



The <b>ISCPSecureQuery2</b> interface extends <a href="https://docs.microsoft.com/windows/desktop/api/mswmdm/nn-mswmdm-iscpsecurequery">ISCPSecureQuery</a> through functionality that determines whether the secure content provider is responsible for the content, and if so, providing a URL for updating revoked components and determining which components have been revoked.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ISCPSecureQuery2</b> interface inherits from <a href="https://docs.microsoft.com/windows/desktop/api/mswmdm/nn-mswmdm-iscpsecurequery">ISCPSecureQuery</a>. <b>ISCPSecureQuery2</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ISCPSecureQuery2</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mswmdm/nf-mswmdm-iscpsecurequery2-makedecision2">MakeDecision2</a>
</td>
<td align="left" width="63%">
Determines whether the secure content provider is responsible for the content by examining data that Windows Media Device Manager passes to this method.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/mswmdm/nn-mswmdm-iscpsecurequery">ISCPSecureQuery Interface</a>



<a href="https://docs.microsoft.com/windows/desktop/api/mswmdm/nn-mswmdm-iscpsecurequery3">ISCPSecureQuery3 Interface</a>



<a href="https://docs.microsoft.com/windows/desktop/WMDM/interfaces-for-secure-content-providers">Interfaces for Secure Content Providers</a>
 

 

