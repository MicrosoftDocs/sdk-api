---
UID: NF:tuner.IESLicenseRenewalResultEvent.GetCASFailureCode
title: IESLicenseRenewalResultEvent::GetCASFailureCode (tuner.h)
description: Gets a code from a LicenseRenewalResult event that indicates the reason for the failure in the conditional access system (CAS).
helpviewer_keywords: ["GetCASFailureCode","GetCASFailureCode method [DirectShow]","GetCASFailureCode method [DirectShow]","IESLicenseRenewalResultEvent interface","IESLicenseRenewalResultEvent interface [DirectShow]","GetCASFailureCode method","IESLicenseRenewalResultEvent.GetCASFailureCode","IESLicenseRenewalResultEvent::GetCASFailureCode","mstv.ieslicenserenewalresultevent_getcasfailurecode","tuner/IESLicenseRenewalResultEvent::GetCASFailureCode"]
old-location: mstv\ieslicenserenewalresultevent_getcasfailurecode.htm
tech.root: mstv
ms.assetid: d3569a5e-6bde-4daf-bf52-094f56b0891c
ms.date: 12/05/2018
ms.keywords: GetCASFailureCode, GetCASFailureCode method [DirectShow], GetCASFailureCode method [DirectShow],IESLicenseRenewalResultEvent interface, IESLicenseRenewalResultEvent interface [DirectShow],GetCASFailureCode method, IESLicenseRenewalResultEvent.GetCASFailureCode, IESLicenseRenewalResultEvent::GetCASFailureCode, mstv.ieslicenserenewalresultevent_getcasfailurecode, tuner/IESLicenseRenewalResultEvent::GetCASFailureCode
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
 - IESLicenseRenewalResultEvent::GetCASFailureCode
 - tuner/IESLicenseRenewalResultEvent::GetCASFailureCode
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
 - IESLicenseRenewalResultEvent.GetCASFailureCode
---

# IESLicenseRenewalResultEvent::GetCASFailureCode


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

 Gets a code from a  <b>LicenseRenewalResult</b> event that indicates the reason for the failure in the conditional access system (CAS).

## -parameters

### -param pdwCASFailureCode [out, retval]

Receives the CAS failure code. This code is defined by the CAS that is used.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/previous-versions/windows/desktop/api/tuner/nn-tuner-ieslicenserenewalresultevent">IESLicenseRenewalResultEvent</a>