---
UID: NF:mfidl.IMFQualityAdvise.DropTime
title: IMFQualityAdvise::DropTime (mfidl.h)
description: Drops samples over a specified interval of time.
helpviewer_keywords: ["60d27190-7bed-427c-9018-2926c85815fe","DropTime","DropTime method [Media Foundation]","DropTime method [Media Foundation]","IMFQualityAdvise interface","IMFQualityAdvise interface [Media Foundation]","DropTime method","IMFQualityAdvise.DropTime","IMFQualityAdvise::DropTime","mf.imfqualityadvise_droptime","mfidl/IMFQualityAdvise::DropTime"]
old-location: mf\imfqualityadvise_droptime.htm
tech.root: mf
ms.assetid: 60d27190-7bed-427c-9018-2926c85815fe
ms.date: 12/05/2018
ms.keywords: 60d27190-7bed-427c-9018-2926c85815fe, DropTime, DropTime method [Media Foundation], DropTime method [Media Foundation],IMFQualityAdvise interface, IMFQualityAdvise interface [Media Foundation],DropTime method, IMFQualityAdvise.DropTime, IMFQualityAdvise::DropTime, mf.imfqualityadvise_droptime, mfidl/IMFQualityAdvise::DropTime
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
 - IMFQualityAdvise::DropTime
 - mfidl/IMFQualityAdvise::DropTime
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
 - IMFQualityAdvise.DropTime
---

# IMFQualityAdvise::DropTime


## -description

Drops samples over a specified interval of time.

## -parameters

### -param hnsAmountToDrop [in]

Amount of time to drop, in 100-nanosecond units. This value is always absolute. If the method is called multiple times, do not add the times from previous calls.

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
<dt><b>MF_E_DROPTIME_NOT_SUPPORTED</b></dt>
</dl>
</td>
<td width="60%">
The object does not support this method.

</td>
</tr>
</table>

## -remarks

Ideally the quality manager can prevent a renderer from falling behind. But if this does occur, then simply lowering quality does not guarantee the renderer will ever catch up. As a result, audio and video might fall out of sync. To correct this problem, the quality manager can call <b>DropTime</b> to request that the renderer drop samples quickly over a specified time interval. After that period, the renderer stops dropping samples.

This method is primarily intended for the video renderer. Dropped audio samples cause audio glitching, which is not desirable.

If a component does not support this method, it should return MF_E_DROPTIME_NOT_SUPPORTED.

## -see-also

<a href="/windows/desktop/api/mfidl/nn-mfidl-imfqualityadvise">IMFQualityAdvise</a>