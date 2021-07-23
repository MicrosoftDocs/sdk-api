---
UID: NF:mfidl.IMFTrustedOutput.GetOutputTrustAuthorityCount
title: IMFTrustedOutput::GetOutputTrustAuthorityCount (mfidl.h)
description: Gets the number of output trust authorities (OTAs) provided by this trusted output. Each OTA reports a single action.
helpviewer_keywords: ["3aae6859-0b32-4705-9045-b98d0bbf43a6","GetOutputTrustAuthorityCount","GetOutputTrustAuthorityCount method [Media Foundation]","GetOutputTrustAuthorityCount method [Media Foundation]","IMFTrustedOutput interface","IMFTrustedOutput interface [Media Foundation]","GetOutputTrustAuthorityCount method","IMFTrustedOutput.GetOutputTrustAuthorityCount","IMFTrustedOutput::GetOutputTrustAuthorityCount","mf.imftrustedoutput_getoutputtrustauthoritycount","mfidl/IMFTrustedOutput::GetOutputTrustAuthorityCount"]
old-location: mf\imftrustedoutput_getoutputtrustauthoritycount.htm
tech.root: mf
ms.assetid: 3aae6859-0b32-4705-9045-b98d0bbf43a6
ms.date: 12/05/2018
ms.keywords: 3aae6859-0b32-4705-9045-b98d0bbf43a6, GetOutputTrustAuthorityCount, GetOutputTrustAuthorityCount method [Media Foundation], GetOutputTrustAuthorityCount method [Media Foundation],IMFTrustedOutput interface, IMFTrustedOutput interface [Media Foundation],GetOutputTrustAuthorityCount method, IMFTrustedOutput.GetOutputTrustAuthorityCount, IMFTrustedOutput::GetOutputTrustAuthorityCount, mf.imftrustedoutput_getoutputtrustauthoritycount, mfidl/IMFTrustedOutput::GetOutputTrustAuthorityCount
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
 - IMFTrustedOutput::GetOutputTrustAuthorityCount
 - mfidl/IMFTrustedOutput::GetOutputTrustAuthorityCount
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
 - IMFTrustedOutput.GetOutputTrustAuthorityCount
---

# IMFTrustedOutput::GetOutputTrustAuthorityCount


## -description

Gets the number of output trust authorities (OTAs) provided by this trusted output. Each OTA reports a single action.

## -parameters

### -param pcOutputTrustAuthorities [out]

Receives the number of OTAs.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/mfidl/nn-mfidl-imftrustedoutput">IMFTrustedOutput</a>