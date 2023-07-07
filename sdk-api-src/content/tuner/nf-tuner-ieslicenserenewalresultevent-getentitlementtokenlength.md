---
UID: NF:tuner.IESLicenseRenewalResultEvent.GetEntitlementTokenLength
title: IESLicenseRenewalResultEvent::GetEntitlementTokenLength (tuner.h)
description: Gets the length of the entitlement token in a protected-content license from a LicenseRenewalResult event.
helpviewer_keywords: ["GetEntitlementTokenLength","GetEntitlementTokenLength method [DirectShow]","GetEntitlementTokenLength method [DirectShow]","IESLicenseRenewalResultEvent interface","IESLicenseRenewalResultEvent interface [DirectShow]","GetEntitlementTokenLength method","IESLicenseRenewalResultEvent.GetEntitlementTokenLength","IESLicenseRenewalResultEvent::GetEntitlementTokenLength","mstv.ieslicenserenewalresultevent_getentitlementtokenlength","tuner/IESLicenseRenewalResultEvent::GetEntitlementTokenLength"]
old-location: mstv\ieslicenserenewalresultevent_getentitlementtokenlength.htm
tech.root: mstv
ms.assetid: e1c8f12c-c2f1-48c1-90fc-051ac87863d5
ms.date: 12/05/2018
ms.keywords: GetEntitlementTokenLength, GetEntitlementTokenLength method [DirectShow], GetEntitlementTokenLength method [DirectShow],IESLicenseRenewalResultEvent interface, IESLicenseRenewalResultEvent interface [DirectShow],GetEntitlementTokenLength method, IESLicenseRenewalResultEvent.GetEntitlementTokenLength, IESLicenseRenewalResultEvent::GetEntitlementTokenLength, mstv.ieslicenserenewalresultevent_getentitlementtokenlength, tuner/IESLicenseRenewalResultEvent::GetEntitlementTokenLength
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
 - IESLicenseRenewalResultEvent::GetEntitlementTokenLength
 - tuner/IESLicenseRenewalResultEvent::GetEntitlementTokenLength
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
 - IESLicenseRenewalResultEvent.GetEntitlementTokenLength
---

# IESLicenseRenewalResultEvent::GetEntitlementTokenLength


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

Gets the length of the entitlement token in a protected-content license from a <b>LicenseRenewalResult</b> event.

## -parameters

### -param pdwLength [out, retval]

Receives the length of the entitlement token, in bytes.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/previous-versions/windows/desktop/api/tuner/nn-tuner-ieslicenserenewalresultevent">IESLicenseRenewalResultEvent</a>