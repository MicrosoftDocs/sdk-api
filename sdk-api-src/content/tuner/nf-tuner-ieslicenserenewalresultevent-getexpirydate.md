---
UID: NF:tuner.IESLicenseRenewalResultEvent.GetExpiryDate
title: IESLicenseRenewalResultEvent::GetExpiryDate (tuner.h)
description: Gets the expiry date of a renewed protected-content license from a LicenseRenewalResult event.
helpviewer_keywords: ["GetExpiryDate","GetExpiryDate method [DirectShow]","GetExpiryDate method [DirectShow]","IESLicenseRenewalResultEvent interface","IESLicenseRenewalResultEvent interface [DirectShow]","GetExpiryDate method","IESLicenseRenewalResultEvent.GetExpiryDate","IESLicenseRenewalResultEvent::GetExpiryDate","mstv.ieslicenserenewalresultevent_getexpirydate","tuner/IESLicenseRenewalResultEvent::GetExpiryDate"]
old-location: mstv\ieslicenserenewalresultevent_getexpirydate.htm
tech.root: mstv
ms.assetid: b237eeb3-d04f-432a-8c7a-538882b5ad02
ms.date: 12/05/2018
ms.keywords: GetExpiryDate, GetExpiryDate method [DirectShow], GetExpiryDate method [DirectShow],IESLicenseRenewalResultEvent interface, IESLicenseRenewalResultEvent interface [DirectShow],GetExpiryDate method, IESLicenseRenewalResultEvent.GetExpiryDate, IESLicenseRenewalResultEvent::GetExpiryDate, mstv.ieslicenserenewalresultevent_getexpirydate, tuner/IESLicenseRenewalResultEvent::GetExpiryDate
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
 - IESLicenseRenewalResultEvent::GetExpiryDate
 - tuner/IESLicenseRenewalResultEvent::GetExpiryDate
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
 - IESLicenseRenewalResultEvent.GetExpiryDate
---

# IESLicenseRenewalResultEvent::GetExpiryDate


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

 Gets the expiry date of a renewed protected-content license from a <b>LicenseRenewalResult</b> event.

## -parameters

### -param pqwExpiryDate [out, retval]

Receives the expiry date in number of seconds since epoch.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/previous-versions/windows/desktop/api/tuner/nn-tuner-ieslicenserenewalresultevent">IESLicenseRenewalResultEvent</a>