---
UID: NN:wsdattachment.IWSDOutboundAttachment
title: IWSDOutboundAttachment (wsdattachment.h)
author: windows-sdk-content
description: Enables applications to send attachment data in a message using a MIME container.
old-location: ncd\iwsdoutboundattachment.htm
tech.root: WsdApi
ms.assetid: ba2f2038-e6ef-4ad4-a1fb-50e225394c60
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IWSDOutboundAttachment, IWSDOutboundAttachment interface, IWSDOutboundAttachment interface,described, ncd.iwsdoutboundattachment, wsdattachment/IWSDOutboundAttachment
ms.topic: interface
f1_keywords: 
 - "wsdattachment/IWSDOutboundAttachment"
req.header: wsdattachment.h
req.include-header: Wsdapi.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: WsdAttachment.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: Wsdapi.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Wsdapi.dll
api_name:
 - IWSDOutboundAttachment
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IWSDOutboundAttachment interface


## -description


Enables applications to send attachment data in a message using a MIME container.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWSDOutboundAttachment</b> interface inherits from <a href="https://docs.microsoft.com/windows/desktop/api/wsdattachment/nn-wsdattachment-iwsdattachment">IWSDAttachment</a>. <b>IWSDOutboundAttachment</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IWSDOutboundAttachment</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wsdattachment/nf-wsdattachment-iwsdoutboundattachment-abort">Abort</a>
</td>
<td align="left" width="63%">
Aborts the transfer of data on the attachment MIME data stream.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wsdattachment/nf-wsdattachment-iwsdoutboundattachment-close">Close</a>
</td>
<td align="left" width="63%">
Closes current attachment MIME data stream.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wsdattachment/nf-wsdattachment-iwsdoutboundattachment-write">Write</a>
</td>
<td align="left" width="63%">
Sends attachment data to the remote host.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/wsdattachment/nn-wsdattachment-iwsdattachment">IWSDAttachment</a>
 

 

