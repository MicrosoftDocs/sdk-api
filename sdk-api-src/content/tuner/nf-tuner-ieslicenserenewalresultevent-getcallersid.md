---
UID: NF:tuner.IESLicenseRenewalResultEvent.GetCallersId
title: IESLicenseRenewalResultEvent::GetCallersId (tuner.h)
description: Gets a unique identifier from a LicenseRenewalResult event that identifies the caller.
helpviewer_keywords: ["GetCallersId","GetCallersId method [DirectShow]","GetCallersId method [DirectShow]","IESLicenseRenewalResultEvent interface","IESLicenseRenewalResultEvent interface [DirectShow]","GetCallersId method","IESLicenseRenewalResultEvent.GetCallersId","IESLicenseRenewalResultEvent::GetCallersId","mstv.ieslicenserenewalresultevent_getcallersid","tuner/IESLicenseRenewalResultEvent::GetCallersId"]
old-location: mstv\ieslicenserenewalresultevent_getcallersid.htm
tech.root: mstv
ms.assetid: c1dfbd63-c165-4872-b992-3f536be9cad1
ms.date: 12/05/2018
ms.keywords: GetCallersId, GetCallersId method [DirectShow], GetCallersId method [DirectShow],IESLicenseRenewalResultEvent interface, IESLicenseRenewalResultEvent interface [DirectShow],GetCallersId method, IESLicenseRenewalResultEvent.GetCallersId, IESLicenseRenewalResultEvent::GetCallersId, mstv.ieslicenserenewalresultevent_getcallersid, tuner/IESLicenseRenewalResultEvent::GetCallersId
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
 - IESLicenseRenewalResultEvent::GetCallersId
 - tuner/IESLicenseRenewalResultEvent::GetCallersId
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
 - IESLicenseRenewalResultEvent.GetCallersId
---

# IESLicenseRenewalResultEvent::GetCallersId


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

 Gets a unique identifier from a <b>LicenseRenewalResult</b> event that identifies the caller. Each client that attempts to renew a license must specify this identifier to identify the client that is requesting the license renewal. When the renewal completes, this result is sent out and received by all the clients that are listening for this event. Clients can use this identifier value to match whether the result belongs to them or is intended for some other client.

## -parameters

### -param pdwCallersId [out, retval]

Receives the caller identifier.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/previous-versions/windows/desktop/api/tuner/nn-tuner-ieslicenserenewalresultevent">IESLicenseRenewalResultEvent</a>