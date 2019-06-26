---
UID: NN:mswmdm.IMDSPRevoked
title: IMDSPRevoked (mswmdm.h)
author: windows-sdk-content
description: The IMDSPRevoked interface retrieves the URL from which updated components can be downloaded. Implementing this interface is optional. For more information, see Mandatory and Optional Interfaces.
old-location: wmdm\imdsprevoked.htm
tech.root: WMDM
ms.assetid: 8df545b9-52f5-422e-a0c1-2316c628d89f
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IMDSPRevoked, IMDSPRevoked interface [windows Media Device Manager], IMDSPRevoked interface [windows Media Device Manager],described, IMDSPRevokedInterface, mswmdm/IMDSPRevoked, wmdm.imdsprevoked
ms.topic: interface
f1_keywords: 
 - "mswmdm/IMDSPRevoked"
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
 - IMDSPRevoked
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IMDSPRevoked interface


## -description



The <b>IMDSPRevoked</b> interface retrieves the URL from which updated components can be downloaded. Implementing this interface is optional. For more information, see <a href="https://docs.microsoft.com/windows/desktop/WMDM/mandatory-and-optional-interfaces">Mandatory and Optional Interfaces</a>.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMDSPRevoked</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IMDSPRevoked</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IMDSPRevoked</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mswmdm/nf-mswmdm-imdsprevoked-getrevocationurl">GetRevocationURL</a>
</td>
<td align="left" width="63%">
Retrieves the URL from which updated components can be downloaded.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/WMDM/interfaces-for-service-providers">Interfaces for Service Providers</a>
 

 

