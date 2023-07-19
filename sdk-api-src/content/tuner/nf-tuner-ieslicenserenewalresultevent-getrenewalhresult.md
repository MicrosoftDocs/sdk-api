---
UID: NF:tuner.IESLicenseRenewalResultEvent.GetRenewalHResult
title: IESLicenseRenewalResultEvent::GetRenewalHResult (tuner.h)
description: Gets the final HRESULT value from a LicenseRenewalResult event that is returned by a call to a COM interface method during the renewal process.
helpviewer_keywords: ["GetRenewalHResult","GetRenewalHResult method [DirectShow]","GetRenewalHResult method [DirectShow]","IESLicenseRenewalResultEvent interface","IESLicenseRenewalResultEvent interface [DirectShow]","GetRenewalHResult method","IESLicenseRenewalResultEvent.GetRenewalHResult","IESLicenseRenewalResultEvent::GetRenewalHResult","mstv.ieslicenserenewalresultevent_getrenewalhresult","tuner/IESLicenseRenewalResultEvent::GetRenewalHResult"]
old-location: mstv\ieslicenserenewalresultevent_getrenewalhresult.htm
tech.root: mstv
ms.assetid: ed823c23-ae7d-4e2d-8546-92f04bd3b212
ms.date: 12/05/2018
ms.keywords: GetRenewalHResult, GetRenewalHResult method [DirectShow], GetRenewalHResult method [DirectShow],IESLicenseRenewalResultEvent interface, IESLicenseRenewalResultEvent interface [DirectShow],GetRenewalHResult method, IESLicenseRenewalResultEvent.GetRenewalHResult, IESLicenseRenewalResultEvent::GetRenewalHResult, mstv.ieslicenserenewalresultevent_getrenewalhresult, tuner/IESLicenseRenewalResultEvent::GetRenewalHResult
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
 - IESLicenseRenewalResultEvent::GetRenewalHResult
 - tuner/IESLicenseRenewalResultEvent::GetRenewalHResult
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
 - IESLicenseRenewalResultEvent.GetRenewalHResult
---

# IESLicenseRenewalResultEvent::GetRenewalHResult


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

Gets the final <b>HRESULT</b> value from a  <b>LicenseRenewalResult</b> event that is returned by a call to a COM interface method during the renewal process.

## -parameters

### -param phr [out, retval]

Receives the <b>HRESULT</b> value.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/previous-versions/windows/desktop/api/tuner/nn-tuner-ieslicenserenewalresultevent">IESLicenseRenewalResultEvent</a>