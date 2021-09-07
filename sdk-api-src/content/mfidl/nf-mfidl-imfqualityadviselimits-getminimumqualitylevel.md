---
UID: NF:mfidl.IMFQualityAdviseLimits.GetMinimumQualityLevel
title: IMFQualityAdviseLimits::GetMinimumQualityLevel (mfidl.h)
description: Gets the minimum quality level that is supported by the component.
helpviewer_keywords: ["GetMinimumQualityLevel","GetMinimumQualityLevel method [Media Foundation]","GetMinimumQualityLevel method [Media Foundation]","IMFQualityAdviseLimits interface","IMFQualityAdviseLimits interface [Media Foundation]","GetMinimumQualityLevel method","IMFQualityAdviseLimits.GetMinimumQualityLevel","IMFQualityAdviseLimits::GetMinimumQualityLevel","mf.imfqualityadviselimits_getminimumqualitylevel","mfidl/IMFQualityAdviseLimits::GetMinimumQualityLevel"]
old-location: mf\imfqualityadviselimits_getminimumqualitylevel.htm
tech.root: mf
ms.assetid: aea08ae5-4252-4703-964b-afc6bbc01a51
ms.date: 12/05/2018
ms.keywords: GetMinimumQualityLevel, GetMinimumQualityLevel method [Media Foundation], GetMinimumQualityLevel method [Media Foundation],IMFQualityAdviseLimits interface, IMFQualityAdviseLimits interface [Media Foundation],GetMinimumQualityLevel method, IMFQualityAdviseLimits.GetMinimumQualityLevel, IMFQualityAdviseLimits::GetMinimumQualityLevel, mf.imfqualityadviselimits_getminimumqualitylevel, mfidl/IMFQualityAdviseLimits::GetMinimumQualityLevel
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
 - IMFQualityAdviseLimits::GetMinimumQualityLevel
 - mfidl/IMFQualityAdviseLimits::GetMinimumQualityLevel
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
 - IMFQualityAdviseLimits.GetMinimumQualityLevel
---

# IMFQualityAdviseLimits::GetMinimumQualityLevel


## -description

Gets the minimum quality level that is supported by the component.

## -parameters

### -param peQualityLevel [out]

Receives the minimum quality level, specified as a member of the <a href="/windows/desktop/api/mfidl/ne-mfidl-mf_quality_level">MF_QUALITY_LEVEL</a> enumeration.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

To get the current quality level, call the <a href="/windows/desktop/api/mfidl/nf-mfidl-imfqualityadvise-getqualitylevel">IMFQualityAdvise::GetQualityLevel</a> method. To set the quality level, call the <a href="/windows/desktop/api/mfidl/nf-mfidl-imfqualityadvise-setqualitylevel">IMFQualityAdvise::SetQualityLevel</a> method.

## -see-also

<a href="/windows/desktop/api/mfidl/nn-mfidl-imfqualityadviselimits">IMFQualityAdviseLimits</a>