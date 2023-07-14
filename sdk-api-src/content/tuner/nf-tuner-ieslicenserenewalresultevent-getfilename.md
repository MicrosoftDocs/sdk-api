---
UID: NF:tuner.IESLicenseRenewalResultEvent.GetFileName
title: IESLicenseRenewalResultEvent::GetFileName (tuner.h)
description: Gets the file name for the license to renew from a LicenseRenewalResult event.
helpviewer_keywords: ["GetFileName","GetFileName method [DirectShow]","GetFileName method [DirectShow]","IESLicenseRenewalResultEvent interface","IESLicenseRenewalResultEvent interface [DirectShow]","GetFileName method","IESLicenseRenewalResultEvent.GetFileName","IESLicenseRenewalResultEvent::GetFileName","mstv.ieslicenserenewalresultevent_getfilename","tuner/IESLicenseRenewalResultEvent::GetFileName"]
old-location: mstv\ieslicenserenewalresultevent_getfilename.htm
tech.root: mstv
ms.assetid: 6ef49a38-c005-4731-a1cb-d5a63ea94e71
ms.date: 12/05/2018
ms.keywords: GetFileName, GetFileName method [DirectShow], GetFileName method [DirectShow],IESLicenseRenewalResultEvent interface, IESLicenseRenewalResultEvent interface [DirectShow],GetFileName method, IESLicenseRenewalResultEvent.GetFileName, IESLicenseRenewalResultEvent::GetFileName, mstv.ieslicenserenewalresultevent_getfilename, tuner/IESLicenseRenewalResultEvent::GetFileName
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
 - IESLicenseRenewalResultEvent::GetFileName
 - tuner/IESLicenseRenewalResultEvent::GetFileName
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
 - IESLicenseRenewalResultEvent.GetFileName
---

# IESLicenseRenewalResultEvent::GetFileName


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

Gets the file name for the license to renew  from a <b>LicenseRenewalResult</b> event.

## -parameters

### -param pbstrFilename [out, retval]

Pointer to a buffer that receives the file name. The caller is responsible for freeing this memory.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/previous-versions/windows/desktop/api/tuner/nn-tuner-ieslicenserenewalresultevent">IESLicenseRenewalResultEvent</a>