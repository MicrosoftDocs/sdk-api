---
UID: NN:mswmdm.IMDServiceProvider2
title: IMDServiceProvider2 (mswmdm.h)
description: The IMDServiceProvider2 interface extends the IMDServiceProvider interface by providing a way of obtaining IMDSPDevice object(s) for a given device path name. The device path name comes from the Plug and Play (PnP) subsystem.
old-location: wmdm\imdserviceprovider2.htm
tech.root: WMDM
ms.assetid: d9ffaea8-5616-4bc2-a27c-8b77ea177b6b
ms.date: 12/05/2018
ms.keywords: IMDServiceProvider2, IMDServiceProvider2 interface [windows Media Device Manager], IMDServiceProvider2 interface [windows Media Device Manager],described, IMDServiceProvider2Interface, mswmdm/IMDServiceProvider2, wmdm.imdserviceprovider2
ms.topic: interface
f1_keywords:
- mswmdm/IMDServiceProvider2
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
- IMDServiceProvider2
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IMDServiceProvider2 interface


## -description



The <b>IMDServiceProvider2</b> interface extends the <a href="https://docs.microsoft.com/windows/desktop/api/mswmdm/nn-mswmdm-imdserviceprovider">IMDServiceProvider</a> interface by providing a way of obtaining <a href="https://docs.microsoft.com/windows/desktop/api/mswmdm/nn-mswmdm-imdspdevice">IMDSPDevice</a> object(s) for a given device path name. The device path name comes from the Plug and Play (PnP) subsystem.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMDServiceProvider2</b> interface inherits from <a href="https://docs.microsoft.com/windows/desktop/api/mswmdm/nn-mswmdm-imdserviceprovider">IMDServiceProvider</a>. <b>IMDServiceProvider2</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IMDServiceProvider2</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mswmdm/nf-mswmdm-imdserviceprovider2-createdevice">CreateDevice</a>
</td>
<td align="left" width="63%">
Creates devices by using the device path.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/mswmdm/nn-mswmdm-imdserviceprovider">IMDServiceProvider Interface</a>



<a href="https://docs.microsoft.com/windows/desktop/WMDM/interfaces-for-service-providers">Interfaces for Service Providers</a>
 

 

