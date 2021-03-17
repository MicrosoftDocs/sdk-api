---
UID: NF:mfidl.IMFMediaSource.GetCharacteristics
title: IMFMediaSource::GetCharacteristics (mfidl.h)
description: Retrieves the characteristics of the media source.
helpviewer_keywords: ["GetCharacteristics","GetCharacteristics method [Media Foundation]","GetCharacteristics method [Media Foundation]","IMFMediaSource interface","IMFMediaSource interface [Media Foundation]","GetCharacteristics method","IMFMediaSource.GetCharacteristics","IMFMediaSource::GetCharacteristics","cb5d54cd-58a3-4903-b22e-8207f90dbbc0","mf.imfmediasource_getcharacteristics","mfidl/IMFMediaSource::GetCharacteristics"]
old-location: mf\imfmediasource_getcharacteristics.htm
tech.root: mf
ms.assetid: cb5d54cd-58a3-4903-b22e-8207f90dbbc0
ms.date: 12/05/2018
ms.keywords: GetCharacteristics, GetCharacteristics method [Media Foundation], GetCharacteristics method [Media Foundation],IMFMediaSource interface, IMFMediaSource interface [Media Foundation],GetCharacteristics method, IMFMediaSource.GetCharacteristics, IMFMediaSource::GetCharacteristics, cb5d54cd-58a3-4903-b22e-8207f90dbbc0, mf.imfmediasource_getcharacteristics, mfidl/IMFMediaSource::GetCharacteristics
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
 - IMFMediaSource::GetCharacteristics
 - mfidl/IMFMediaSource::GetCharacteristics
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
 - IMFMediaSource.GetCharacteristics
---

# IMFMediaSource::GetCharacteristics


## -description

Retrieves the characteristics of the media source.

## -parameters

### -param pdwCharacteristics [out]

Receives a bitwise <b>OR</b> of zero or more flags from the <a href="/windows/desktop/api/mfidl/ne-mfidl-mfmediasource_characteristics">MFMEDIASOURCE_CHARACTERISTICS</a> enumeration.

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
<dt><b>MF_E_SHUTDOWN</b></dt>
</dl>
</td>
<td width="60%">
The media source's <a href="/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-shutdown">Shutdown</a> method has been called.

</td>
</tr>
</table>

## -remarks

The characteristics of a media source can change at any time. If this happens, the source sends an <a href="/windows/desktop/medfound/mesourcecharacteristicschanged">MESourceCharacteristicsChanged</a> event.

## -see-also

<a href="/windows/desktop/api/mfidl/nn-mfidl-imfmediasource">IMFMediaSource</a>