---
UID: NF:tuner.IESLicenseRenewalResultEvent.GetRenewalResultCode
title: IESLicenseRenewalResultEvent::GetRenewalResultCode (tuner.h)
description: Gets a constant from a Protected Broadcast Driver Architecture (PBDA) LicenseRenewalResult event that indicates which step in the renewal process caused the renewal to succeed or fail.
helpviewer_keywords: ["GetRenewalResultCode","GetRenewalResultCode method [DirectShow]","GetRenewalResultCode method [DirectShow]","IESLicenseRenewalResultEvent interface","IESLicenseRenewalResultEvent interface [DirectShow]","GetRenewalResultCode method","IESLicenseRenewalResultEvent.GetRenewalResultCode","IESLicenseRenewalResultEvent::GetRenewalResultCode","mstv.ieslicenserenewalresultevent_getrenewalresultcode","tuner/IESLicenseRenewalResultEvent::GetRenewalResultCode"]
old-location: mstv\ieslicenserenewalresultevent_getrenewalresultcode.htm
tech.root: mstv
ms.assetid: 99b46541-8c94-4456-aae9-d266fc52a6a9
ms.date: 12/05/2018
ms.keywords: GetRenewalResultCode, GetRenewalResultCode method [DirectShow], GetRenewalResultCode method [DirectShow],IESLicenseRenewalResultEvent interface, IESLicenseRenewalResultEvent interface [DirectShow],GetRenewalResultCode method, IESLicenseRenewalResultEvent.GetRenewalResultCode, IESLicenseRenewalResultEvent::GetRenewalResultCode, mstv.ieslicenserenewalresultevent_getrenewalresultcode, tuner/IESLicenseRenewalResultEvent::GetRenewalResultCode
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IESLicenseRenewalResultEvent::GetRenewalResultCode
 - tuner/IESLicenseRenewalResultEvent::GetRenewalResultCode
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - tuner.h
api_name:
 - IESLicenseRenewalResultEvent.GetRenewalResultCode
---

# IESLicenseRenewalResultEvent::GetRenewalResultCode


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

Gets a constant from a Protected Broadcast Driver Architecture (PBDA) <b>LicenseRenewalResult</b> event that indicates which step in the renewal process caused the renewal to succeed or fail. A client can call the <a href="/previous-versions/windows/desktop/api/tuner/nf-tuner-ieslicenserenewalresultevent-isrenewalsuccessful">IsRenewalSuccessful</a> method to determine if the renewal was successful, and then call this method to get information about the reason for any failure.

## -parameters

### -param pdwRenewalResultCode [out, retval]

Receives the result code. The result code indicates the license renewal step that failed and can be any of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt>LBE_RenewalStage_Invalid</dt>
</dl>
</td>
<td width="60%">
Received license was invalid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>LRE_RenewalStage_RenewalFailed</dt>
</dl>
</td>
<td width="60%">
Renewal attempt failed.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>LRE_RenewalStage_CheckForRenewableLicense</dt>
</dl>
</td>
<td width="60%">
Renewal attempt failed during the check for a renewable license.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>LRE_RenewalStage_RenewLicenseAtTuner</dt>
</dl>
</td>
<td width="60%">
Renewal attempt failed at the tuner.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>LRE_RenewalStage_StoreLicenseInDRM</dt>
</dl>
</td>
<td width="60%">
Renewal attempt failed during license storage.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>LRE_RenewalStage_RenewalSuccessful</dt>
</dl>
</td>
<td width="60%">
License renewal was successful.

</td>
</tr>
</table>

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/previous-versions/windows/desktop/api/tuner/nn-tuner-ieslicenserenewalresultevent">IESLicenseRenewalResultEvent</a>