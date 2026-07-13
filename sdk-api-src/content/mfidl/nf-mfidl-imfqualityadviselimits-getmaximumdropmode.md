---
UID: NF:mfidl.IMFQualityAdviseLimits.GetMaximumDropMode
title: IMFQualityAdviseLimits::GetMaximumDropMode (mfidl.h)
description: Gets the maximum drop mode.
helpviewer_keywords: ["GetMaximumDropMode","GetMaximumDropMode method [Media Foundation]","GetMaximumDropMode method [Media Foundation]","IMFQualityAdviseLimits interface","IMFQualityAdviseLimits interface [Media Foundation]","GetMaximumDropMode method","IMFQualityAdviseLimits.GetMaximumDropMode","IMFQualityAdviseLimits::GetMaximumDropMode","mf.imfqualityadviselimits_getmaximumdropmode","mfidl/IMFQualityAdviseLimits::GetMaximumDropMode"]
old-location: mf\imfqualityadviselimits_getmaximumdropmode.htm
tech.root: mf
ms.assetid: af3d968b-7baf-41d8-afd9-dbf673c1bb71
ms.date: 12/05/2018
ms.keywords: GetMaximumDropMode, GetMaximumDropMode method [Media Foundation], GetMaximumDropMode method [Media Foundation],IMFQualityAdviseLimits interface, IMFQualityAdviseLimits interface [Media Foundation],GetMaximumDropMode method, IMFQualityAdviseLimits.GetMaximumDropMode, IMFQualityAdviseLimits::GetMaximumDropMode, mf.imfqualityadviselimits_getmaximumdropmode, mfidl/IMFQualityAdviseLimits::GetMaximumDropMode
req.header: mfidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps \| UWP apps]
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
 - IMFQualityAdviseLimits::GetMaximumDropMode
 - mfidl/IMFQualityAdviseLimits::GetMaximumDropMode
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mfidl.h
api_name:
 - IMFQualityAdviseLimits.GetMaximumDropMode
---

# IMFQualityAdviseLimits::GetMaximumDropMode


## -description

Gets the maximum <i>drop mode</i>. A higher drop mode means that the object will, if needed, drop samples more aggressively to match the presentation clock.

## -parameters

### -param peDropMode [out]

Receives the maximum drop mode, specified as a member of the <a href="/windows/desktop/api/mfidl/ne-mfidl-mf_quality_drop_mode">MF_QUALITY_DROP_MODE</a> enumeration.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

To get the current drop mode, call the <a href="/windows/desktop/api/mfidl/nf-mfidl-imfqualityadvise-getdropmode">IMFQualityAdvise::GetDropMode</a> method. To set the drop mode, call the <a href="/windows/desktop/api/mfidl/nf-mfidl-imfqualityadvise-setdropmode">IMFQualityAdvise::SetDropMode</a> method.

## -see-also

<a href="/windows/desktop/api/mfidl/nn-mfidl-imfqualityadviselimits">IMFQualityAdviseLimits</a>