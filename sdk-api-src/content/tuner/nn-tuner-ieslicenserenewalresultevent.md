---
UID: NN:tuner.IESLicenseRenewalResultEvent
title: IESLicenseRenewalResultEvent (tuner.h)
author: windows-sdk-content
description: Implements methods that get information from a LicenseRenewalResult event.
old-location: mstv\ieslicenserenewalresultevent.htm
tech.root: mstv
ms.assetid: 6f9cbec4-7934-41fc-b387-3f45aa273a72
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IESLicenseRenewalResultEvent, IESLicenseRenewalResultEvent interface [DirectShow], IESLicenseRenewalResultEvent interface [DirectShow],described, mstv.ieslicenserenewalresultevent, tuner/IESLicenseRenewalResultEvent
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
 - IESLicenseRenewalResultEvent
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IESLicenseRenewalResultEvent interface


## -description


Implements methods that get information from a  <b>LicenseRenewalResult</b> event. This event contains the results of an attempt to renew a license for protected content. If the attempt succeeds, the results contain the license; if the attempt fails, the results contain error information.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IESLicenseRenewalResultEvent</b> interface inherits from <b>IESEvent</b>. <b>IESLicenseRenewalResultEvent</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IESLicenseRenewalResultEvent</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/c1dfbd63-c165-4872-b992-3f536be9cad1">GetCallersId</a>
</td>
<td align="left" width="63%">
Gets the unique identifier for a client that attempts a license renewal.


</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d3569a5e-6bde-4daf-bf52-094f56b0891c">GetCASFailureCode</a>
</td>
<td align="left" width="63%">
Gets a code that indicates the reason that an attempt to access protected content failed.


</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ed09aea2-e000-40ce-bd94-a174e75a5001">GetDescrambledStatus</a>
</td>
<td align="left" width="63%">
Gets a status code from one of the license renewal steps.


</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/6178a884-df87-4fcb-a069-3791726d4335">GetEntitlementToken</a>
</td>
<td align="left" width="63%">
Gets the entitlement token from the license.


</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/e1c8f12c-c2f1-48c1-90fc-051ac87863d5">GetEntitlementTokenLength</a>
</td>
<td align="left" width="63%">
Gets the length of the entitlement token from the license.


</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/b237eeb3-d04f-432a-8c7a-538882b5ad02">GetExpiryDate</a>
</td>
<td align="left" width="63%">
Gets the expiry date from the license.


</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/6ef49a38-c005-4731-a1cb-d5a63ea94e71">GetFileName</a>
</td>
<td align="left" width="63%">
Gets the file name for  the license to renew.


</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ed823c23-ae7d-4e2d-8546-92f04bd3b212">GetRenewalHResult</a>
</td>
<td align="left" width="63%">
Gets the last <b>HRESULT</b> value returned by a call to a COM interface method during the renewal process.


</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/99b46541-8c94-4456-aae9-d266fc52a6a9">GetRenewalResultCode</a>
</td>
<td align="left" width="63%">
Gets a constant that indicates which step in the renewal process caused the renewal to succeed or fail.


</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/e19375c6-5999-43e9-9d91-3237b900cb07">IsCheckEntitlementCallRequired</a>
</td>
<td align="left" width="63%">
Gets a flag that indicates whether the client should check the entitlement token in the license.


</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/0c57e4e4-ee93-4e86-b1f8-eed5dd5aa931">IsRenewalSuccessful</a>
</td>
<td align="left" width="63%">
Gets a flag that indicates whether the license renewal is successful.


</td>
</tr>
</table> 


## -remarks



To declare the interface identifier (IID) for this interface, use the <b>__uuidof</b> operator: <code>__uuidof(IESLicenseRenewalResultEvent)</code>.



