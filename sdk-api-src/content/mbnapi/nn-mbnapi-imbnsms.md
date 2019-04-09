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
---

# IMbnSms interface


## -description


SMS interface for sending and receiving messages as well as controlling the messaging configuration.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMbnSms</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IMbnSms</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/b868bb6f-3ac0-4d77-82dd-b9bc94882a8b">GetSmsConfiguration</a>
</td>
<td align="left" width="63%">
Gets the SMS configuration.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/58cb60dd-160c-4e1c-a244-7f20b5e79b64">GetSmsStatus</a>
</td>
<td align="left" width="63%">
Gets the SMS status.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/8ed3af39-345b-4bfb-aea1-072a64f7921a">SetSmsConfiguration</a>
</td>
<td align="left" width="63%">
Updates the SMS configuration.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/cd37582e-891d-4f6a-aba3-01ad3101a6b9">SmsDelete</a>
</td>
<td align="left" width="63%">
Deletes a set of SMS messages.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d15eab89-c2bb-45af-8a6b-077517973fb1">SmsRead</a>
</td>
<td align="left" width="63%">
Reads a set of SMS messages.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/5a370e00-929f-4ff9-861f-d0edc880f51d">SmsSendCdma</a>
</td>
<td align="left" width="63%">
Sends a message in CDMA format.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/8bc0cad6-dee3-4325-b5e9-397bbd346a87">SmsSendCdmaPdu</a>
</td>
<td align="left" width="63%">
Sends a message in CDMA binary format.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/c8f5bde5-d28c-4799-9f46-7b02745e6bfb">SmsSendPdu</a>
</td>
<td align="left" width="63%">
Sends a message in PDU format.

</td>
</tr>
</table> 


## -remarks



The calling application can acquire this interface by calling the <a href="https://msdn.microsoft.com/en-us/library/ms682521(v=VS.85).aspx">QueryInterface</a> method of <a href="https://msdn.microsoft.com/958bce42-4772-4706-8900-1f83c5d3d52b">IMbnInterface</a>




