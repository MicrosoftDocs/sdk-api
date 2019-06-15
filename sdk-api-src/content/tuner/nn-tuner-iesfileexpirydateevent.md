---
UID: NN:tuner.IESFileExpiryDateEvent
title: IESFileExpiryDateEvent (tuner.h)
author: windows-sdk-content
description: Gets information from a FileExpiryDate event.
old-location: mstv\iesfileexpirydateevent.htm
tech.root: mstv
ms.assetid: 6c89a3ee-7d69-4cde-b1e5-b566fa1c2ca3
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IESFileExpiryDateEvent, IESFileExpiryDateEvent interface [Microsoft TV Technologies], IESFileExpiryDateEvent interface [Microsoft TV Technologies],described, mstv.iesfileexpirydateevent, tuner/IESFileExpiryDateEvent
ms.topic: interface
req.header: tuner.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: None supported
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Tuner.idl
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
 - tuner.h
api_name:
 - IESFileExpiryDateEvent
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IESFileExpiryDateEvent interface


## -description


Gets information from a  <b>FileExpiryDate</b> event. A Protected Broadcast Driver Architecture (PBDA) media transform device (MTD) fires a <b>FileExpiryDate</b> event when it receives a new license for protected content that contains a new expiry date for that content. 


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IESFileExpiryDateEvent</b> interface inherits from <b>IESEvent</b>. <b>IESFileExpiryDateEvent</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IESFileExpiryDateEvent</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/tuner/nf-tuner-iesfileexpirydateevent-doesexpireafterfirstuse">DoesExpireAfterFirstUse</a>
</td>
<td align="left" width="63%">
Indicates whether the license expires after its first use.


</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/tuner/nf-tuner-iesfileexpirydateevent-getexpirydate">GetExpiryDate</a>
</td>
<td align="left" width="63%">
Extracts the expiry date from the event.


</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/tuner/nf-tuner-iesfileexpirydateevent-getfinalexpirydate">GetFinalExpiryDate</a>
</td>
<td align="left" width="63%">
Gets the final expiry date if the license includes earlier expiry dates, which indicates license renewals.


</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/tuner/nf-tuner-iesfileexpirydateevent-getmaxrenewalcount">GetMaxRenewalCount</a>
</td>
<td align="left" width="63%">
Gets the maximum number of allowable renewals from the event.


</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/tuner/nf-tuner-iesfileexpirydateevent-gettunerid">GetTunerId</a>
</td>
<td align="left" width="63%">
Gets an identifier for the tuner that generated or received the new license.


</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/tuner/nf-tuner-iesfileexpirydateevent-isentitlementtokenpresent">IsEntitlementTokenPresent</a>
</td>
<td align="left" width="63%">
Indicates whether the event includes an entitlement token.


</td>
</tr>
</table> 


## -remarks



To declare the interface identifier (IID) for this interface, use the <b>__uuidof</b> operator: <code>__uuidof(IESFileExpiryDateEvent)</code>.



