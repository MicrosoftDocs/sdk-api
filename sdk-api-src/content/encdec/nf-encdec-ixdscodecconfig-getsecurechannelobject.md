---
UID: NF:encdec.IXDSCodecConfig.GetSecureChannelObject
title: IXDSCodecConfig::GetSecureChannelObject (encdec.h)
description: This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005.
helpviewer_keywords: ["GetSecureChannelObject","GetSecureChannelObject method [Microsoft TV Technologies]","GetSecureChannelObject method [Microsoft TV Technologies]","IXDSCodecConfig interface","IXDSCodecConfig interface [Microsoft TV Technologies]","GetSecureChannelObject method","IXDSCodecConfig.GetSecureChannelObject","IXDSCodecConfig::GetSecureChannelObject","IXDSCodecConfigGetSecureChannelObject","encdec/IXDSCodecConfig::GetSecureChannelObject","mstv.ixdscodecconfig_getsecurechannelobject"]
old-location: mstv\ixdscodecconfig_getsecurechannelobject.htm
tech.root: mstv
ms.assetid: c7bf4efe-110a-4bcc-927c-f5e4798211df
ms.date: 12/05/2018
ms.keywords: GetSecureChannelObject, GetSecureChannelObject method [Microsoft TV Technologies], GetSecureChannelObject method [Microsoft TV Technologies],IXDSCodecConfig interface, IXDSCodecConfig interface [Microsoft TV Technologies],GetSecureChannelObject method, IXDSCodecConfig.GetSecureChannelObject, IXDSCodecConfig::GetSecureChannelObject, IXDSCodecConfigGetSecureChannelObject, encdec/IXDSCodecConfig::GetSecureChannelObject, mstv.ixdscodecconfig_getsecurechannelobject
req.header: encdec.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
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
 - IXDSCodecConfig::GetSecureChannelObject
 - encdec/IXDSCodecConfig::GetSecureChannelObject
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - EncDec.h
api_name:
 - IXDSCodecConfig.GetSecureChannelObject
---

# IXDSCodecConfig::GetSecureChannelObject


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005.
        



The <b>GetSecureChannelObject</b> method retrieves the secure channel object used to decrypt the stream.

## -parameters

### -param ppUnkDRMSecureChannel [out]

Receives a pointer to the secure channel object's <b>IUnknown</b> interface.

## -returns

Returns an <b>HRESULT</b>.

## -remarks

If the method succeeds, the caller must release the <b>IUnknown</b> interface.

## -see-also

<a href="/previous-versions/windows/desktop/api/encdec/nn-encdec-ixdscodecconfig">IXDSCodecConfig Interface</a>