---
UID: NF:mfidl.IMFRateSupport.IsRateSupported
title: IMFRateSupport::IsRateSupported (mfidl.h)
description: Queries whether the object supports a specified playback rate.
helpviewer_keywords: ["3ac04683-17d3-4d87-b260-39b04eab9e59","IMFRateSupport interface [Media Foundation]","IsRateSupported method","IMFRateSupport.IsRateSupported","IMFRateSupport::IsRateSupported","IsRateSupported","IsRateSupported method [Media Foundation]","IsRateSupported method [Media Foundation]","IMFRateSupport interface","mf.imfratesupport_isratesupported","mfidl/IMFRateSupport::IsRateSupported"]
old-location: mf\imfratesupport_isratesupported.htm
tech.root: medfound
ms.assetid: 3ac04683-17d3-4d87-b260-39b04eab9e59
ms.date: 12/05/2018
ms.keywords: 3ac04683-17d3-4d87-b260-39b04eab9e59, IMFRateSupport interface [Media Foundation],IsRateSupported method, IMFRateSupport.IsRateSupported, IMFRateSupport::IsRateSupported, IsRateSupported, IsRateSupported method [Media Foundation], IsRateSupported method [Media Foundation],IMFRateSupport interface, mf.imfratesupport_isratesupported, mfidl/IMFRateSupport::IsRateSupported
f1_keywords:
- mfidl/IMFRateSupport.IsRateSupported
dev_langs:
- c++
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
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- mfuuid.lib
- mfuuid.dll
api_name:
- IMFRateSupport.IsRateSupported
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IMFRateSupport::IsRateSupported


## -description



Queries whether the object supports a specified playback rate.




## -parameters




### -param fThin [in]

If <b>TRUE</b>, the method queries whether the object supports the playback rate with thinning. Otherwise, the method queries whether the object supports the playback rate without thinning. For information about thinning, see <a href="https://docs.microsoft.com/windows/desktop/medfound/about-rate-control">About Rate Control</a>.


### -param flRate [in]

The playback rate to query.


### -param pflNearestSupportedRate [in, out]

If the object does not support the playback rate given in <i>flRate</i>, this parameter receives the closest supported playback rate. If the method returns S_OK, this parameter receives the value given in <i>flRate</i>. This parameter can be <b>NULL</b>.


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
The object supports the specified rate.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MF_E_REVERSE_UNSUPPORTED</b></dt>
</dl>
</td>
<td width="60%">
The object does not support reverse playback.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MF_E_THINNING_UNSUPPORTED</b></dt>
</dl>
</td>
<td width="60%">
The object does not support thinning.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MF_E_UNSUPPORTED_RATE</b></dt>
</dl>
</td>
<td width="60%">
The object does not support the specified rate.

</td>
</tr>
</table>
 




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/medfound/how-to-determine-supported-rates">How to Determine Supported Rates</a>



<a href="https://docs.microsoft.com/windows/desktop/api/mfidl/nn-mfidl-imfratesupport">IMFRateSupport</a>
 

 

