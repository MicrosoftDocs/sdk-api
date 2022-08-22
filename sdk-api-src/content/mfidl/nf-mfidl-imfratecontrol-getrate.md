---
UID: NF:mfidl.IMFRateControl.GetRate
title: IMFRateControl::GetRate (mfidl.h)
description: Gets the current playback rate. (IMFRateControl.GetRate)
helpviewer_keywords: ["GetRate","GetRate method [Media Foundation]","GetRate method [Media Foundation]","IMFRateControl interface","IMFRateControl interface [Media Foundation]","GetRate method","IMFRateControl.GetRate","IMFRateControl::GetRate","fb970d06-0f82-4e35-8e03-68044c7f12cd","mf.imfratecontrol_getrate","mfidl/IMFRateControl::GetRate"]
old-location: mf\imfratecontrol_getrate.htm
tech.root: mf
ms.assetid: fb970d06-0f82-4e35-8e03-68044c7f12cd
ms.date: 12/05/2018
ms.keywords: GetRate, GetRate method [Media Foundation], GetRate method [Media Foundation],IMFRateControl interface, IMFRateControl interface [Media Foundation],GetRate method, IMFRateControl.GetRate, IMFRateControl::GetRate, fb970d06-0f82-4e35-8e03-68044c7f12cd, mf.imfratecontrol_getrate, mfidl/IMFRateControl::GetRate
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
 - IMFRateControl::GetRate
 - mfidl/IMFRateControl::GetRate
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
 - IMFRateControl.GetRate
---

# IMFRateControl::GetRate


## -description

Gets the current playback rate.

## -parameters

### -param pfThin [in, out]

Receives the value <b>TRUE</b> if the stream is currently being thinned. If the object does not support thinning, this parameter always receives the value <b>FALSE</b>. This parameter can be <b>NULL</b>. For more information, see <a href="/windows/desktop/medfound/about-rate-control">About Rate Control</a>.

### -param pflRate [in, out]

Receives the current playback rate.

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
</table>

## -see-also

<a href="/windows/desktop/medfound/how-to-determine-supported-rates">How to Determine Supported Rates</a>



<a href="/windows/desktop/api/mfidl/nn-mfidl-imfratecontrol">IMFRateControl</a>
