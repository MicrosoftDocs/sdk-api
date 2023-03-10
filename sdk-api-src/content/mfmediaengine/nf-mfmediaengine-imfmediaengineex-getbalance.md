---
UID: NF:mfmediaengine.IMFMediaEngineEx.GetBalance
title: IMFMediaEngineEx::GetBalance (mfmediaengine.h)
description: Gets the audio balance.
helpviewer_keywords: ["GetBalance","GetBalance method [Media Foundation]","GetBalance method [Media Foundation]","IMFMediaEngineEx interface","IMFMediaEngineEx interface [Media Foundation]","GetBalance method","IMFMediaEngineEx.GetBalance","IMFMediaEngineEx::GetBalance","mf.imfmediaengineex_getbalance","mfmediaengine/IMFMediaEngineEx::GetBalance"]
old-location: mf\imfmediaengineex_getbalance.htm
tech.root: mf
ms.assetid: 57935B52-27BE-47AF-8702-9DF91E1B515D
ms.date: 12/05/2018
ms.keywords: GetBalance, GetBalance method [Media Foundation], GetBalance method [Media Foundation],IMFMediaEngineEx interface, IMFMediaEngineEx interface [Media Foundation],GetBalance method, IMFMediaEngineEx.GetBalance, IMFMediaEngineEx::GetBalance, mf.imfmediaengineex_getbalance, mfmediaengine/IMFMediaEngineEx::GetBalance
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
 - IMFMediaEngineEx::GetBalance
 - mfmediaengine/IMFMediaEngineEx::GetBalance
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
 - IMFMediaEngineEx.GetBalance
---

# IMFMediaEngineEx::GetBalance


## -description

Gets the audio balance.



## -returns

Returns the balance. The value can be any number in the following range (inclusive).



<table>
<tr>
<th>Return value</th>
<th>Description</th>
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

## -see-also

<a href="/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfmediaengineex">IMFMediaEngineEx</a>
