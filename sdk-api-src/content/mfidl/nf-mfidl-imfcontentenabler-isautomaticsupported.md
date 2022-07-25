---
UID: NF:mfidl.IMFContentEnabler.IsAutomaticSupported
title: IMFContentEnabler::IsAutomaticSupported (mfidl.h)
description: Queries whether the content enabler can perform all of its actions automatically.
helpviewer_keywords: ["144470ce-2849-4464-8596-fac216529145","IMFContentEnabler interface [Media Foundation]","IsAutomaticSupported method","IMFContentEnabler.IsAutomaticSupported","IMFContentEnabler::IsAutomaticSupported","IsAutomaticSupported","IsAutomaticSupported method [Media Foundation]","IsAutomaticSupported method [Media Foundation]","IMFContentEnabler interface","mf.imfcontentenabler_isautomaticsupported","mfidl/IMFContentEnabler::IsAutomaticSupported"]
old-location: mf\imfcontentenabler_isautomaticsupported.htm
tech.root: mf
ms.assetid: 144470ce-2849-4464-8596-fac216529145
ms.date: 12/05/2018
ms.keywords: 144470ce-2849-4464-8596-fac216529145, IMFContentEnabler interface [Media Foundation],IsAutomaticSupported method, IMFContentEnabler.IsAutomaticSupported, IMFContentEnabler::IsAutomaticSupported, IsAutomaticSupported, IsAutomaticSupported method [Media Foundation], IsAutomaticSupported method [Media Foundation],IMFContentEnabler interface, mf.imfcontentenabler_isautomaticsupported, mfidl/IMFContentEnabler::IsAutomaticSupported
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
 - IMFContentEnabler::IsAutomaticSupported
 - mfidl/IMFContentEnabler::IsAutomaticSupported
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
 - IMFContentEnabler.IsAutomaticSupported
---

# IMFContentEnabler::IsAutomaticSupported


## -description

Queries whether the content enabler can perform all of its actions automatically.

## -parameters

### -param pfAutomatic [out]

Receives a Boolean value. If <b>TRUE</b>, the content enabler can perform the enabling action automatically.

## -returns

The method returns an HRESULT. Possible values include, but are not limited to, those in the following table.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The method succeeded.

</td>
</tr>
</table>

## -remarks

If this method returns <b>TRUE</b> in the <i>pfAutomatic</i> parameter, call the <a href="/windows/desktop/api/mfidl/nf-mfidl-imfcontentenabler-automaticenable">IMFContentEnabler::AutomaticEnable</a> method to perform the enabling action.

If this method returns <b>FALSE</b> in the <i>pfAutomatic</i> parameter, the application must use manual enabling. To do so, call <a href="/windows/desktop/api/mfidl/nf-mfidl-imfcontentenabler-getenableurl">IMFContentEnabler::GetEnableURL</a> and <a href="/windows/desktop/api/mfidl/nf-mfidl-imfcontentenabler-getenabledata">IMFContentEnabler::GetEnableData</a> to get the URL and data needed for manual enabling.

## -see-also

<a href="/windows/desktop/medfound/how-to-play-protected-media-files">How to Play Protected Media Files</a>



<a href="/windows/desktop/api/mfidl/nn-mfidl-imfcontentenabler">IMFContentEnabler</a>