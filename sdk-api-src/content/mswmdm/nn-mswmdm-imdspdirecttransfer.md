---
UID: NN:mswmdm.IMDSPDirectTransfer
title: IMDSPDirectTransfer (mswmdm.h)
description: The IMDSPDirectTransfer interface enables Windows Media Device Manager to delegate content transfer to the service provider.helpviewer_keywords: ["IMDSPDirectTransfer","IMDSPDirectTransfer interface [windows Media Device Manager]","IMDSPDirectTransfer interface [windows Media Device Manager]","described","IMDSPDirectTransferInterface","mswmdm/IMDSPDirectTransfer","wmdm.imdspdirecttransfer"]
old-location: wmdm\imdspdirecttransfer.htm
tech.root: WMDM
ms.assetid: b053158c-9a1e-4da4-a428-7edceeaaee1e
ms.date: 12/05/2018
ms.keywords: IMDSPDirectTransfer, IMDSPDirectTransfer interface [windows Media Device Manager], IMDSPDirectTransfer interface [windows Media Device Manager],described, IMDSPDirectTransferInterface, mswmdm/IMDSPDirectTransfer, wmdm.imdspdirecttransfer
f1_keywords:
- mswmdm/IMDSPDirectTransfer
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
- IMDSPDirectTransfer
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IMDSPDirectTransfer interface


## -description



The <b>IMDSPDirectTransfer</b> interface enables Windows Media Device Manager to delegate content transfer to the service provider. In this case Windows Media Device Manager does not do any processing of the content before sending it to the service provider. The service provider gets full control of the source.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMDSPDirectTransfer</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IMDSPDirectTransfer</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IMDSPDirectTransfer</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mswmdm/nf-mswmdm-imdspdirecttransfer-transfertodevice">TransferToDevice</a>
</td>
<td align="left" width="63%">
Called by Windows Media Device Manager to delegate content transfer to the service provider.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/WMDM/interfaces-for-service-providers">Interfaces for Service Providers</a>
 

 

