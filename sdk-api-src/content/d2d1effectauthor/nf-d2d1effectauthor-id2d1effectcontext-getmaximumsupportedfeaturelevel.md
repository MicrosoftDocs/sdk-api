---
UID: NF:d2d1effectauthor.ID2D1EffectContext.GetMaximumSupportedFeatureLevel
title: ID2D1EffectContext::GetMaximumSupportedFeatureLevel (d2d1effectauthor.h)
description: This indicates the maximum feature level from the provided list which is supported by the device.
helpviewer_keywords: ["GetMaximumSupportedFeatureLevel","GetMaximumSupportedFeatureLevel method [Direct2D]","GetMaximumSupportedFeatureLevel method [Direct2D]","ID2D1EffectContext interface","ID2D1EffectContext interface [Direct2D]","GetMaximumSupportedFeatureLevel method","ID2D1EffectContext.GetMaximumSupportedFeatureLevel","ID2D1EffectContext::GetMaximumSupportedFeatureLevel","d2d1effectauthor/ID2D1EffectContext::GetMaximumSupportedFeatureLevel","direct2d.id2d1contextinternal_getfeaturelevel"]
old-location: direct2d\id2d1contextinternal_getfeaturelevel.htm
tech.root: Direct2D
ms.assetid: BDB553F8-C19D-46FC-A3CF-7E525DA81CE2
ms.date: 12/05/2018
ms.keywords: GetMaximumSupportedFeatureLevel, GetMaximumSupportedFeatureLevel method [Direct2D], GetMaximumSupportedFeatureLevel method [Direct2D],ID2D1EffectContext interface, ID2D1EffectContext interface [Direct2D],GetMaximumSupportedFeatureLevel method, ID2D1EffectContext.GetMaximumSupportedFeatureLevel, ID2D1EffectContext::GetMaximumSupportedFeatureLevel, d2d1effectauthor/ID2D1EffectContext::GetMaximumSupportedFeatureLevel, direct2d.id2d1contextinternal_getfeaturelevel
req.header: d2d1effectauthor.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 and Platform Update for Windows 7 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2012 and Platform Update for Windows Server 2008 R2 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: D2D1.lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ID2D1EffectContext::GetMaximumSupportedFeatureLevel
 - d2d1effectauthor/ID2D1EffectContext::GetMaximumSupportedFeatureLevel
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - D2D1.lib
 - D2D1.dll
api_name:
 - ID2D1EffectContext.GetMaximumSupportedFeatureLevel
---

# ID2D1EffectContext::GetMaximumSupportedFeatureLevel


## -description

This indicates the maximum feature level from the provided list which is supported by the device. If none of the provided levels are supported, then this API fails with D2DERR_INSUFFICIENT_DEVICE_CAPABILITIES.

## -parameters

### -param featureLevels [in]

Type: <b>const <a href="/windows/desktop/api/d3dcommon/ne-d3dcommon-d3d_feature_level">D3D_FEATURE_LEVEL</a>*</b>

The feature levels provided by the application.

### -param featureLevelsCount

Type: <b>UINT32</b>

The count of feature levels provided by the application

### -param maximumSupportedFeatureLevel [out]

Type: <b><a href="/windows/desktop/api/d3dcommon/ne-d3dcommon-d3d_feature_level">D3D_FEATURE_LEVEL</a>*</b>

The maximum feature level from the <i>featureLevels</i> list which is supported by the D2D device.

## -returns

Type: <b>HRESULT</b>

The method returns an <b>HRESULT</b>. Possible values include, but are not limited to, those in the following table.

<table>
<tr>
<th>HRESULT</th>
<th>Description</th>
</tr>
<tr>
<td>S_OK</td>
<td>No error occurred.</td>
</tr>
<tr>
<td>E_OUTOFMEMORY</td>
<td>Direct2D could not allocate sufficient memory to complete the call.</td>
</tr>
<tr>
<td>E_INVALIDARG</td>
<td>An invalid parameter was passed to the returning function.</td>
</tr>
<tr>
<td>D2DERR_INSUFFICIENT_DEVICE_CAPABILITIES</td>
<td>None of the provided levels are supported.</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1effectcontext">ID2D1EffectContext</a>