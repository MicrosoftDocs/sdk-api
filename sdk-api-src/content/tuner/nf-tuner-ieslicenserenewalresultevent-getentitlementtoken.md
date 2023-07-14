---
UID: NF:tuner.IESLicenseRenewalResultEvent.GetEntitlementToken
title: IESLicenseRenewalResultEvent::GetEntitlementToken (tuner.h)
description: Gets the entitlement token in a protected-content license from a LicenseRenewalResult event. Clients can call the GetEntitlementTokenLength method to get the number of bytes to read from this buffer.
helpviewer_keywords: ["GetEntitlementToken","GetEntitlementToken method [DirectShow]","GetEntitlementToken method [DirectShow]","IESLicenseRenewalResultEvent interface","IESLicenseRenewalResultEvent interface [DirectShow]","GetEntitlementToken method","IESLicenseRenewalResultEvent.GetEntitlementToken","IESLicenseRenewalResultEvent::GetEntitlementToken","mstv.ieslicenserenewalresultevent_getentitlementtoken","tuner/IESLicenseRenewalResultEvent::GetEntitlementToken"]
old-location: mstv\ieslicenserenewalresultevent_getentitlementtoken.htm
tech.root: mstv
ms.assetid: 6178a884-df87-4fcb-a069-3791726d4335
ms.date: 12/05/2018
ms.keywords: GetEntitlementToken, GetEntitlementToken method [DirectShow], GetEntitlementToken method [DirectShow],IESLicenseRenewalResultEvent interface, IESLicenseRenewalResultEvent interface [DirectShow],GetEntitlementToken method, IESLicenseRenewalResultEvent.GetEntitlementToken, IESLicenseRenewalResultEvent::GetEntitlementToken, mstv.ieslicenserenewalresultevent_getentitlementtoken, tuner/IESLicenseRenewalResultEvent::GetEntitlementToken
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
 - IESLicenseRenewalResultEvent::GetEntitlementToken
 - tuner/IESLicenseRenewalResultEvent::GetEntitlementToken
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
 - IESLicenseRenewalResultEvent.GetEntitlementToken
---

# IESLicenseRenewalResultEvent::GetEntitlementToken


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

 Gets the entitlement token in a protected-content license from a <b>LicenseRenewalResult</b> event. Clients can call the <a href="/previous-versions/windows/desktop/api/tuner/nf-tuner-ieslicenserenewalresultevent-getentitlementtokenlength">GetEntitlementTokenLength</a> method to get the number of bytes to read from this buffer.

## -parameters

### -param pbData [out, retval]

Pointer to a buffer that receives the entitlement token.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/previous-versions/windows/desktop/api/tuner/nf-tuner-ieslicenserenewalresultevent-getentitlementtokenlength">GetEntitlementTokenLength</a>



<a href="/previous-versions/windows/desktop/api/tuner/nn-tuner-ieslicenserenewalresultevent">IESLicenseRenewalResultEvent</a>