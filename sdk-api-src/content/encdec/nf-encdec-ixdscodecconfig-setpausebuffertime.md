---
UID: NF:encdec.IXDSCodecConfig.SetPauseBufferTime
title: IXDSCodecConfig::SetPauseBufferTime (encdec.h)
description: This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005.
helpviewer_keywords: ["IXDSCodecConfig interface [Microsoft TV Technologies]","SetPauseBufferTime method","IXDSCodecConfig.SetPauseBufferTime","IXDSCodecConfig::SetPauseBufferTime","IXDSCodecConfigSetPauseBufferTime","SetPauseBufferTime","SetPauseBufferTime method [Microsoft TV Technologies]","SetPauseBufferTime method [Microsoft TV Technologies]","IXDSCodecConfig interface","encdec/IXDSCodecConfig::SetPauseBufferTime","mstv.ixdscodecconfig_setpausebuffertime"]
old-location: mstv\ixdscodecconfig_setpausebuffertime.htm
tech.root: mstv
ms.assetid: 46e71958-86bc-4649-a401-b16131dd6bbd
ms.date: 12/05/2018
ms.keywords: IXDSCodecConfig interface [Microsoft TV Technologies],SetPauseBufferTime method, IXDSCodecConfig.SetPauseBufferTime, IXDSCodecConfig::SetPauseBufferTime, IXDSCodecConfigSetPauseBufferTime, SetPauseBufferTime, SetPauseBufferTime method [Microsoft TV Technologies], SetPauseBufferTime method [Microsoft TV Technologies],IXDSCodecConfig interface, encdec/IXDSCodecConfig::SetPauseBufferTime, mstv.ixdscodecconfig_setpausebuffertime
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
 - IXDSCodecConfig::SetPauseBufferTime
 - encdec/IXDSCodecConfig::SetPauseBufferTime
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
 - IXDSCodecConfig.SetPauseBufferTime
---

# IXDSCodecConfig::SetPauseBufferTime


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005.
        



The <b>SetPauseBufferTime</b> method specifies how often the XDS Codec filter attempts to generate a new license for protected video content.

## -parameters

### -param dwPauseBufferTime [in]

Specifies the license generation interval, in seconds.

## -returns

Returns an <b>HRESULT</b>.

## -see-also

<a href="/previous-versions/windows/desktop/api/encdec/nn-encdec-ixdscodecconfig">IXDSCodecConfig Interface</a>