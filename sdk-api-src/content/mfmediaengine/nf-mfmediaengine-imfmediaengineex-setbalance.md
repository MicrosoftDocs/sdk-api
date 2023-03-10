---
UID: NF:mfmediaengine.IMFMediaEngineEx.SetBalance
title: IMFMediaEngineEx::SetBalance (mfmediaengine.h)
description: Sets the audio balance. (IMFMediaEngineEx.SetBalance)
helpviewer_keywords: ["IMFMediaEngineEx interface [Media Foundation]","SetBalance method","IMFMediaEngineEx.SetBalance","IMFMediaEngineEx::SetBalance","SetBalance","SetBalance method [Media Foundation]","SetBalance method [Media Foundation]","IMFMediaEngineEx interface","mf.imfmediaengineex_setbalance","mfmediaengine/IMFMediaEngineEx::SetBalance"]
old-location: mf\imfmediaengineex_setbalance.htm
tech.root: mf
ms.assetid: 11187826-B873-4182-A77B-FD9CCECFBAE5
ms.date: 12/05/2018
ms.keywords: IMFMediaEngineEx interface [Media Foundation],SetBalance method, IMFMediaEngineEx.SetBalance, IMFMediaEngineEx::SetBalance, SetBalance, SetBalance method [Media Foundation], SetBalance method [Media Foundation],IMFMediaEngineEx interface, mf.imfmediaengineex_setbalance, mfmediaengine/IMFMediaEngineEx::SetBalance
req.header: mfmediaengine.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2012 [desktop apps \| UWP apps]
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
 - IMFMediaEngineEx::SetBalance
 - mfmediaengine/IMFMediaEngineEx::SetBalance
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mfmediaengine.h
api_name:
 - IMFMediaEngineEx.SetBalance
---

# IMFMediaEngineEx::SetBalance


## -description

Sets the audio balance.

## -parameters

### -param balance [in]

The audio balance. The value can be any number in the following range (inclusive).



<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt>-1</dt>
</dl>
</td>
<td width="60%">
The left channel is at full volume; the right channel is silent.


</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>1</dt>
</dl>
</td>
<td width="60%">
The right channel is at full volume; the left channel is silent.


</td>
</tr>
</table>
 

If the value is zero, the left and right channels are at equal volumes. The default value is zero.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

When the audio balance changes, the Media Engine sends an <b>MF_MEDIA_ENGINE_EVENT_BALANCECHANGE</b> event. See <a href="/windows/desktop/api/mfmediaengine/nf-mfmediaengine-imfmediaenginenotify-eventnotify">IMFMediaEventNotify::EventNotify</a>.

## -see-also

<a href="/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfmediaengineex">IMFMediaEngineEx</a>
