---
UID: NN:mswmdm.ISCPSession
title: ISCPSession (mswmdm.h)
description: The ISCPSession interface provides efficient common state management for multiple operations.A secure content provider (SCP) session is useful when transferring multiple files.
old-location: wmdm\iscpsession.htm
tech.root: WMDM
ms.assetid: 4efd8e5a-490b-435b-b34d-7099198891b1
ms.date: 12/05/2018
ms.keywords: ISCPSession, ISCPSession interface [windows Media Device Manager], ISCPSession interface [windows Media Device Manager],described, ISCPSessionInterface, mswmdm/ISCPSession, wmdm.iscpsession
ms.topic: interface
f1_keywords:
- mswmdm/ISCPSession
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
- ISCPSession
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ISCPSession interface


## -description



The <b>ISCPSession</b> interface provides efficient common state management for multiple operations.

A secure content provider (SCP) session is useful when transferring multiple files. In that case, the session can help SCP do some of the operations only once instead of once for every file transfer. This results in better transfer performance.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ISCPSession</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>ISCPSession</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ISCPSession</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mswmdm/nf-mswmdm-iscpsession-beginsession">BeginSession</a>
</td>
<td align="left" width="63%">
Indicates the beginning of a session.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mswmdm/nf-mswmdm-iscpsession-endsession">EndSession</a>
</td>
<td align="left" width="63%">
Indicates the end of a session.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mswmdm/nf-mswmdm-iscpsession-getsecurequery">GetSecureQuery</a>
</td>
<td align="left" width="63%">
Obtains a secure query object for to the session.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/WMDM/interfaces-for-secure-content-providers">Interfaces for Secure Content Providers</a>
 

 

