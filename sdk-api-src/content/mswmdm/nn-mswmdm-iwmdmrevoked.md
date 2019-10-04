---
UID: NN:mswmdm.IWMDMRevoked
title: IWMDMRevoked (mswmdm.h)
author: windows-sdk-content
description: The IWMDMRevoked interface retrieves the URL from which updated components can be downloaded, if a transfer fails with a revocation error.
old-location: wmdm\iwmdmrevoked.htm
tech.root: WMDM
ms.assetid: b627f243-3652-4db9-8a5e-6a2146b73424
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IWMDMRevoked, IWMDMRevoked interface [windows Media Device Manager], IWMDMRevoked interface [windows Media Device Manager],described, IWMDMRevokedInterface, mswmdm/IWMDMRevoked, wmdm.iwmdmrevoked
ms.topic: interface
f1_keywords: 
 - "mswmdm/IWMDMRevoked"
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
 - IWMDMRevoked
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IWMDMRevoked interface


## -description



The <b>IWMDMRevoked</b> interface retrieves the URL from which updated components can be downloaded, if a transfer fails with a revocation error. The secured content provider determines whether or not to allow a transfer, based on the application certificates of the components involved. You can access the <b>IWMDMRevoked</b> interface by calling <b>QueryInterface</b> on the <a href="https://docs.microsoft.com/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmstoragecontrol">IWMDMStorageControl</a> interface.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWMDMRevoked</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IWMDMRevoked</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IWMDMRevoked</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmrevoked-getrevocationurl">GetRevocationURL</a>
</td>
<td align="left" width="63%">
Retrieves the URL from which updated components can be downloaded.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmstoragecontrol">IWMDMStorageControl Interface</a>



<a href="https://docs.microsoft.com/windows/desktop/WMDM/interfaces-for-applications">Interfaces for Applications</a>
 

 

