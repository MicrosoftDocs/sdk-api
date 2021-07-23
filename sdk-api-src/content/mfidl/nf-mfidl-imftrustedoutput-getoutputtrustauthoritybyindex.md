---
UID: NF:mfidl.IMFTrustedOutput.GetOutputTrustAuthorityByIndex
title: IMFTrustedOutput::GetOutputTrustAuthorityByIndex (mfidl.h)
description: Gets an output trust authority (OTA), specified by index.
helpviewer_keywords: ["4dd570e7-c6fb-4ffb-8ef5-b88a6638dbbf","GetOutputTrustAuthorityByIndex","GetOutputTrustAuthorityByIndex method [Media Foundation]","GetOutputTrustAuthorityByIndex method [Media Foundation]","IMFTrustedOutput interface","IMFTrustedOutput interface [Media Foundation]","GetOutputTrustAuthorityByIndex method","IMFTrustedOutput.GetOutputTrustAuthorityByIndex","IMFTrustedOutput::GetOutputTrustAuthorityByIndex","mf.imftrustedoutput_getoutputtrustauthoritybyindex","mfidl/IMFTrustedOutput::GetOutputTrustAuthorityByIndex"]
old-location: mf\imftrustedoutput_getoutputtrustauthoritybyindex.htm
tech.root: medfound
ms.assetid: 4dd570e7-c6fb-4ffb-8ef5-b88a6638dbbf
ms.date: 12/05/2018
ms.keywords: 4dd570e7-c6fb-4ffb-8ef5-b88a6638dbbf, GetOutputTrustAuthorityByIndex, GetOutputTrustAuthorityByIndex method [Media Foundation], GetOutputTrustAuthorityByIndex method [Media Foundation],IMFTrustedOutput interface, IMFTrustedOutput interface [Media Foundation],GetOutputTrustAuthorityByIndex method, IMFTrustedOutput.GetOutputTrustAuthorityByIndex, IMFTrustedOutput::GetOutputTrustAuthorityByIndex, mf.imftrustedoutput_getoutputtrustauthoritybyindex, mfidl/IMFTrustedOutput::GetOutputTrustAuthorityByIndex
req.header: mfidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Mfuuid.lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IMFTrustedOutput::GetOutputTrustAuthorityByIndex
 - mfidl/IMFTrustedOutput::GetOutputTrustAuthorityByIndex
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mfuuid.lib
 - mfuuid.dll
api_name:
 - IMFTrustedOutput.GetOutputTrustAuthorityByIndex
---

# IMFTrustedOutput::GetOutputTrustAuthorityByIndex


## -description

Gets an output trust authority (OTA), specified by index.

## -parameters

### -param dwIndex [in]

Zero-based index of the OTA to retrieve. To get the number of OTAs provided by this object, call <a href="/windows/desktop/api/mfidl/nf-mfidl-imftrustedoutput-getoutputtrustauthoritycount">IMFTrustedOutput::GetOutputTrustAuthorityCount</a>.

### -param ppauthority [out]

Receives a pointer to the <a href="/windows/desktop/api/mfidl/nn-mfidl-imfoutputtrustauthority">IMFOutputTrustAuthority</a> interface of the OTA. The caller must release the interface.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/mfidl/nn-mfidl-imftrustedoutput">IMFTrustedOutput</a>