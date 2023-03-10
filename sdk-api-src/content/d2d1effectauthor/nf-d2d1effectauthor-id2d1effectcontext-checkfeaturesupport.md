---
UID: NF:d2d1effectauthor.ID2D1EffectContext.CheckFeatureSupport
title: ID2D1EffectContext::CheckFeatureSupport (d2d1effectauthor.h)
description: This indicates whether an optional capability is supported by the D3D device.
helpviewer_keywords: ["CheckFeatureSupport","CheckFeatureSupport method [Direct2D]","CheckFeatureSupport method [Direct2D]","ID2D1EffectContext interface","ID2D1EffectContext interface [Direct2D]","CheckFeatureSupport method","ID2D1EffectContext.CheckFeatureSupport","ID2D1EffectContext::CheckFeatureSupport","d2d1effectauthor/ID2D1EffectContext::CheckFeatureSupport","direct2d.id2d1effectcontext_checkfeaturesupport"]
old-location: direct2d\id2d1effectcontext_checkfeaturesupport.htm
tech.root: Direct2D
ms.assetid: 1A97B928-7715-4D4E-AD38-7D01EE243494
ms.date: 12/05/2018
ms.keywords: CheckFeatureSupport, CheckFeatureSupport method [Direct2D], CheckFeatureSupport method [Direct2D],ID2D1EffectContext interface, ID2D1EffectContext interface [Direct2D],CheckFeatureSupport method, ID2D1EffectContext.CheckFeatureSupport, ID2D1EffectContext::CheckFeatureSupport, d2d1effectauthor/ID2D1EffectContext::CheckFeatureSupport, direct2d.id2d1effectcontext_checkfeaturesupport
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
req.lib: D2d1.lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ID2D1EffectContext::CheckFeatureSupport
 - d2d1effectauthor/ID2D1EffectContext::CheckFeatureSupport
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - d2d1.lib
 - d2d1.dll
api_name:
 - ID2D1EffectContext.CheckFeatureSupport
---

# ID2D1EffectContext::CheckFeatureSupport


## -description

This indicates whether an optional capability is supported by the D3D device.

## -parameters

### -param feature

Type: <b><a href="/windows/desktop/api/d2d1effectauthor/ne-d2d1effectauthor-d2d1_feature">D2D1_FEATURE</a></b>

The feature to query support for.

### -param featureSupportData [out]

Type: <b>void*</b>

A structure indicating information about how or if the feature is supported.

### -param featureSupportDataSize [out]

Type: <b>UINT32</b>

The size of the <i>featureSupportData</i> parameter.

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
</table>

## -see-also

<a href="/windows/desktop/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1effectcontext">ID2D1EffectContext</a>