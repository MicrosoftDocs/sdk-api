---
UID: NN:mswmdm.ISCPSecureExchange2
title: ISCPSecureExchange2 (mswmdm.h)
author: windows-sdk-content
description: The ISCPSecureExchange2 interface extends ISCPSecureExchange by providing a new version of the TransferContainerData method.
old-location: wmdm\iscpsecureexchange2.htm
tech.root: WMDM
ms.assetid: 815fd9b9-2186-40e2-8d72-e6bf91fd45c9
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: ISCPSecureExchange2, ISCPSecureExchange2 interface [windows Media Device Manager], ISCPSecureExchange2 interface [windows Media Device Manager],described, ISCPSecureExchange2Interface, mswmdm/ISCPSecureExchange2, wmdm.iscpsecureexchange2
ms.topic: interface
f1_keywords: 
 - "mswmdm/ISCPSecureExchange2"
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
 - ISCPSecureExchange2
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ISCPSecureExchange2 interface


## -description



The <b>ISCPSecureExchange2</b> interface extends <a href="https://docs.microsoft.com/windows/desktop/api/mswmdm/nn-mswmdm-iscpsecureexchange">ISCPSecureExchange</a> by providing a new version of the <b>TransferContainerData</b> method. <b>TransferContainerData2</b> accepts a progress callback on which the secure content provider can send progress notifications for any of the steps it needs to carry out.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ISCPSecureExchange2</b> interface inherits from <a href="https://docs.microsoft.com/windows/desktop/api/mswmdm/nn-mswmdm-iscpsecureexchange">ISCPSecureExchange</a>. <b>ISCPSecureExchange2</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ISCPSecureExchange2</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mswmdm/nf-mswmdm-iscpsecureexchange2-transfercontainerdata2">TransferContainerData2</a>
</td>
<td align="left" width="63%">
Transfers container file data to the secure content provider.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/mswmdm/nn-mswmdm-iscpsecureexchange">ISCPSecureExchange Interface</a>



<a href="https://docs.microsoft.com/windows/desktop/api/mswmdm/nn-mswmdm-iscpsecureexchange3">ISCPSecureExchange3 Interface</a>



<a href="https://docs.microsoft.com/windows/desktop/WMDM/interfaces-for-secure-content-providers">Interfaces for Secure Content Providers</a>
 

 

