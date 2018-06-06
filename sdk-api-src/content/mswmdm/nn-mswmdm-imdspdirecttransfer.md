---
UID: NN:mswmdm.IMDSPDirectTransfer
title: IMDSPDirectTransfer
author: windows-sdk-content
description: The IMDSPDirectTransfer interface enables Windows Media Device Manager to delegate content transfer to the service provider.
old-location: wmdm\imdspdirecttransfer.htm
old-project: WMDM
ms.assetid: b053158c-9a1e-4da4-a428-7edceeaaee1e
ms.author: windowssdkdev
ms.date: 05/22/2018
ms.keywords: IMDSPDirectTransfer, IMDSPDirectTransfer interface [windows Media Device Manager], IMDSPDirectTransfer interface [windows Media Device Manager],described, IMDSPDirectTransferInterface, mswmdm/IMDSPDirectTransfer, wmdm.imdspdirecttransfer
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
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
tech.root: 
req.typenames: MSVidCtlStateList
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mswmdm.h
api_name:
 - IMDSPDirectTransfer
product: Windows
targetos: Windows
req.lib: Mssachlp.lib
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# IMDSPDirectTransfer interface


## -description



The <b>IMDSPDirectTransfer</b> interface enables Windows Media Device Manager to delegate content transfer to the service provider. In this case Windows Media Device Manager does not do any processing of the content before sending it to the service provider. The service provider gets full control of the source.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMDSPDirectTransfer</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IMDSPDirectTransfer</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/7a95a23d-751e-4101-a150-3a1e47a14a95">TransferToDevice</a>
</td>
<td align="left" width="63%">
Called by Windows Media Device Manager to delegate content transfer to the service provider.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/bd61c5fa-047c-4d93-bae1-f3433696b95b">Interfaces for Service Providers</a>
 

 

