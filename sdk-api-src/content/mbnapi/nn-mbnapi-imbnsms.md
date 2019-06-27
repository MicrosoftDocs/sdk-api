---
UID: NN:mbnapi.IMbnSms
title: IMbnSms (mbnapi.h)
author: windows-sdk-content
description: SMS interface for sending and receiving messages as well as controlling the messaging configuration.
old-location: mbn\imbnsms.htm
tech.root: mbn
ms.assetid: 4a5fae5a-91d5-4a94-ac54-cb641147e8dc
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IMbnSms, IMbnSms interface [Microsoft Broadband Networks], IMbnSms interface [Microsoft Broadband Networks],described, mbn.imbnsms, mbnapi/IMbnSms
ms.topic: interface
f1_keywords: 
 - "mbnapi/IMbnSms"
req.header: mbnapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: None supported
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Mbnapi.idl
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
 - mbnapi.h
api_name:
 - IMbnSms
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IMbnSms interface


## -description


SMS interface for sending and receiving messages as well as controlling the messaging configuration.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMbnSms</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IMbnSms</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IMbnSms</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mbnapi/nf-mbnapi-imbnsms-getsmsconfiguration">GetSmsConfiguration</a>
</td>
<td align="left" width="63%">
Gets the SMS configuration.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mbnapi/nf-mbnapi-imbnsms-getsmsstatus">GetSmsStatus</a>
</td>
<td align="left" width="63%">
Gets the SMS status.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mbnapi/nf-mbnapi-imbnsms-setsmsconfiguration">SetSmsConfiguration</a>
</td>
<td align="left" width="63%">
Updates the SMS configuration.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mbnapi/nf-mbnapi-imbnsms-smsdelete">SmsDelete</a>
</td>
<td align="left" width="63%">
Deletes a set of SMS messages.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mbnapi/nf-mbnapi-imbnsms-smsread">SmsRead</a>
</td>
<td align="left" width="63%">
Reads a set of SMS messages.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mbnapi/nf-mbnapi-imbnsms-smssendcdma">SmsSendCdma</a>
</td>
<td align="left" width="63%">
Sends a message in CDMA format.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mbnapi/nf-mbnapi-imbnsms-smssendcdmapdu">SmsSendCdmaPdu</a>
</td>
<td align="left" width="63%">
Sends a message in CDMA binary format.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mbnapi/nf-mbnapi-imbnsms-smssendpdu">SmsSendPdu</a>
</td>
<td align="left" width="63%">
Sends a message in PDU format.

</td>
</tr>
</table> 


## -remarks



The calling application can acquire this interface by calling the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q_)">QueryInterface</a> method of <a href="https://docs.microsoft.com/windows/desktop/api/mbnapi/nn-mbnapi-imbninterface">IMbnInterface</a>




