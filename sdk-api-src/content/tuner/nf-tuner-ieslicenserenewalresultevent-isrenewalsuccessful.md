---
UID: NF:tuner.IESLicenseRenewalResultEvent.IsRenewalSuccessful
title: IESLicenseRenewalResultEvent::IsRenewalSuccessful (tuner.h)
description: Gets a flag from a LicenseRenewalResult event that indicates whether the renewal was successful. In the event of failure, a client can call the GetRenewalResultCode or GetRenewalHResult method to get information about the reason for the failure.
helpviewer_keywords: ["IESLicenseRenewalResultEvent interface [DirectShow]","IsRenewalSuccessful method","IESLicenseRenewalResultEvent.IsRenewalSuccessful","IESLicenseRenewalResultEvent::IsRenewalSuccessful","IsRenewalSuccessful","IsRenewalSuccessful method [DirectShow]","IsRenewalSuccessful method [DirectShow]","IESLicenseRenewalResultEvent interface","mstv.ieslicenserenewalresultevent_isrenewalsuccessful","tuner/IESLicenseRenewalResultEvent::IsRenewalSuccessful"]
old-location: mstv\ieslicenserenewalresultevent_isrenewalsuccessful.htm
tech.root: mstv
ms.assetid: 0c57e4e4-ee93-4e86-b1f8-eed5dd5aa931
ms.date: 12/05/2018
ms.keywords: IESLicenseRenewalResultEvent interface [DirectShow],IsRenewalSuccessful method, IESLicenseRenewalResultEvent.IsRenewalSuccessful, IESLicenseRenewalResultEvent::IsRenewalSuccessful, IsRenewalSuccessful, IsRenewalSuccessful method [DirectShow], IsRenewalSuccessful method [DirectShow],IESLicenseRenewalResultEvent interface, mstv.ieslicenserenewalresultevent_isrenewalsuccessful, tuner/IESLicenseRenewalResultEvent::IsRenewalSuccessful
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
 - IESLicenseRenewalResultEvent::IsRenewalSuccessful
 - tuner/IESLicenseRenewalResultEvent::IsRenewalSuccessful
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
 - IESLicenseRenewalResultEvent.IsRenewalSuccessful
---

# IESLicenseRenewalResultEvent::IsRenewalSuccessful


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

 Gets a flag from a  <b>LicenseRenewalResult</b> event that indicates whether the renewal was successful. In the event of failure, a client can call the  <a href="/previous-versions/windows/desktop/api/tuner/nf-tuner-ieslicenserenewalresultevent-getrenewalresultcode">GetRenewalResultCode</a> or <a href="/previous-versions/windows/desktop/api/tuner/nf-tuner-ieslicenserenewalresultevent-getrenewalhresult">GetRenewalHResult</a> method to get information about the reason for the failure.

## -parameters

### -param pfRenewalSuccessful [out, retval]

Receives the renewal success flag: 1 indicates success; 0 indicates failure.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/previous-versions/windows/desktop/api/tuner/nf-tuner-ieslicenserenewalresultevent-getrenewalhresult">GetRenewalHResult</a>



<a href="/previous-versions/windows/desktop/api/tuner/nf-tuner-ieslicenserenewalresultevent-getrenewalresultcode">GetRenewalResultCode</a>



<a href="/previous-versions/windows/desktop/api/tuner/nn-tuner-ieslicenserenewalresultevent">IESLicenseRenewalResultEvent</a>