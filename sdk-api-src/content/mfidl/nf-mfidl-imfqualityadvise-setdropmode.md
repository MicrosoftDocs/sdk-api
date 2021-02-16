---
UID: NF:mfidl.IMFQualityAdvise.SetDropMode
title: IMFQualityAdvise::SetDropMode (mfidl.h)
description: Sets the drop mode. In drop mode, a component drops samples, more or less aggressively depending on the level of the drop mode.
helpviewer_keywords: ["190de66a-6c47-49d5-a8f6-c2fb57a7aee2","IMFQualityAdvise interface [Media Foundation]","SetDropMode method","IMFQualityAdvise.SetDropMode","IMFQualityAdvise::SetDropMode","SetDropMode","SetDropMode method [Media Foundation]","SetDropMode method [Media Foundation]","IMFQualityAdvise interface","mf.imfqualityadvise_setdropmode","mfidl/IMFQualityAdvise::SetDropMode"]
old-location: mf\imfqualityadvise_setdropmode.htm
tech.root: mf
ms.assetid: 190de66a-6c47-49d5-a8f6-c2fb57a7aee2
ms.date: 12/05/2018
ms.keywords: 190de66a-6c47-49d5-a8f6-c2fb57a7aee2, IMFQualityAdvise interface [Media Foundation],SetDropMode method, IMFQualityAdvise.SetDropMode, IMFQualityAdvise::SetDropMode, SetDropMode, SetDropMode method [Media Foundation], SetDropMode method [Media Foundation],IMFQualityAdvise interface, mf.imfqualityadvise_setdropmode, mfidl/IMFQualityAdvise::SetDropMode
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
 - IMFQualityAdvise::SetDropMode
 - mfidl/IMFQualityAdvise::SetDropMode
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
 - IMFQualityAdvise.SetDropMode
---

# IMFQualityAdvise::SetDropMode


## -description

Sets the drop mode. In drop mode, a component drops samples, more or less aggressively depending on the level of the drop mode.

## -parameters

### -param eDropMode [in]

Requested drop mode, specified as a member of the <a href="/windows/desktop/api/mfidl/ne-mfidl-mf_quality_drop_mode">MF_QUALITY_DROP_MODE</a> enumeration.

## -returns

The method returns an <b>HRESULT</b>. Possible values include, but are not limited to, those in the following table.

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
<tr>
<td width="40%">
<dl>
<dt><b>MF_E_NO_MORE_DROP_MODES</b></dt>
</dl>
</td>
<td width="60%">
The component does not support the specified mode or any higher modes.

</td>
</tr>
</table>

## -remarks

If this method is called on a media source, the media source might switch between thinned and non-thinned output. If that occurs, the affected streams will send an <a href="/windows/desktop/medfound/mestreamthinmode">MEStreamThinMode</a> event to indicate the transition. The operation is asynchronous; after <b>SetDropMode</b> returns, you might receive samples that were queued before the transition. The MEStreamThinMode event marks the exact point in the stream where the transition occurs.

## -see-also

<a href="/windows/desktop/api/mfidl/nn-mfidl-imfqualityadvise">IMFQualityAdvise</a>