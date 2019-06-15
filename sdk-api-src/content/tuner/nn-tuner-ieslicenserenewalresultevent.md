---
UID: NN:tuner.IESLicenseRenewalResultEvent
title: IESLicenseRenewalResultEvent (tuner.h)
author: windows-sdk-content
description: Implements methods that get information from a LicenseRenewalResult event.
old-location: mstv\ieslicenserenewalresultevent.htm
tech.root: mstv
ms.assetid: 6f9cbec4-7934-41fc-b387-3f45aa273a72
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IESLicenseRenewalResultEvent, IESLicenseRenewalResultEvent interface [DirectShow], IESLicenseRenewalResultEvent interface [DirectShow],described, mstv.ieslicenserenewalresultevent, tuner/IESLicenseRenewalResultEvent
ms.topic: interface
f1_keywords: ["tuner/IESLicenseRenewalResultEvent"]
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
ms.custom: 19H1
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
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/tuner/nf-tuner-ieslicenserenewalresultevent-getcallersid">GetCallersId</a>
</td>
<td align="left" width="63%">
Gets the unique identifier for a client that attempts a license renewal.


</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/tuner/nf-tuner-ieslicenserenewalresultevent-getcasfailurecode">GetCASFailureCode</a>
</td>
<td align="left" width="63%">
Gets a code that indicates the reason that an attempt to access protected content failed.


</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/tuner/nf-tuner-ieslicenserenewalresultevent-getdescrambledstatus">GetDescrambledStatus</a>
</td>
<td align="left" width="63%">
Gets a status code from one of the license renewal steps.


</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/tuner/nf-tuner-ieslicenserenewalresultevent-getentitlementtoken">GetEntitlementToken</a>
</td>
<td align="left" width="63%">
Gets the entitlement token from the license.


</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/tuner/nf-tuner-ieslicenserenewalresultevent-getentitlementtokenlength">GetEntitlementTokenLength</a>
</td>
<td align="left" width="63%">
Gets the length of the entitlement token from the license.


</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/tuner/nf-tuner-ieslicenserenewalresultevent-getexpirydate">GetExpiryDate</a>
</td>
<td align="left" width="63%">
Gets the expiry date from the license.


</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/tuner/nf-tuner-ieslicenserenewalresultevent-getfilename">GetFileName</a>
</td>
<td align="left" width="63%">
Gets the file name for  the license to renew.


</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/tuner/nf-tuner-ieslicenserenewalresultevent-getrenewalhresult">GetRenewalHResult</a>
</td>
<td align="left" width="63%">
Gets the last <b>HRESULT</b> value returned by a call to a COM interface method during the renewal process.


</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/tuner/nf-tuner-ieslicenserenewalresultevent-getrenewalresultcode">GetRenewalResultCode</a>
</td>
<td align="left" width="63%">
Gets a constant that indicates which step in the renewal process caused the renewal to succeed or fail.


</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/tuner/nf-tuner-ieslicenserenewalresultevent-ischeckentitlementcallrequired">IsCheckEntitlementCallRequired</a>
</td>
<td align="left" width="63%">
Gets a flag that indicates whether the client should check the entitlement token in the license.


</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/tuner/nf-tuner-ieslicenserenewalresultevent-isrenewalsuccessful">IsRenewalSuccessful</a>
</td>
<td align="left" width="63%">
Gets a flag that indicates whether the license renewal is successful.


</td>
</tr>
</table> 


## -remarks



To declare the interface identifier (IID) for this interface, use the <b>__uuidof</b> operator: <code>__uuidof(IESLicenseRenewalResultEvent)</code>.



