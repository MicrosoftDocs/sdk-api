---
UID: NF:mfidl.MFCreateAggregateSource
title: MFCreateAggregateSource function (mfidl.h)
description: Creates a media source that aggregates a collection of media sources.
helpviewer_keywords: ["MFCreateAggregateSource","MFCreateAggregateSource function [Media Foundation]","mf.mfcreateaggregatesource","mfidl/MFCreateAggregateSource"]
old-location: mf\mfcreateaggregatesource.htm
tech.root: mf
ms.assetid: 7288bd4b-6a74-4528-854d-d82783630422
ms.date: 12/05/2018
ms.keywords: MFCreateAggregateSource, MFCreateAggregateSource function [Media Foundation], mf.mfcreateaggregatesource, mfidl/MFCreateAggregateSource
req.header: mfidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Mf.lib
req.dll: Mf.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - MFCreateAggregateSource
 - mfidl/MFCreateAggregateSource
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - mf.dll
api_name:
 - MFCreateAggregateSource
---

# MFCreateAggregateSource function


## -description

Creates a media source that aggregates a collection of media sources.

## -parameters

### -param pSourceCollection [in]

A pointer to the <a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfcollection">IMFCollection</a> interface of the collection object that contains a list of media sources.

### -param ppAggSource [out]

Receives a pointer to the <a href="/windows/desktop/api/mfidl/nn-mfidl-imfmediasource">IMFMediaSource</a> interface of the aggregated media source. The caller must release the interface.

## -returns

The function returns an <b>HRESULT</b>. Possible values include, but are not limited to, those in the following table.



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
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
The <i>pSourceCollection</i> collection does not contain any elements.

</td>
</tr>
</table>

## -remarks

The aggregated media source is useful for combining  streams from separate media sources. For example, you can use it to  combine a video capture source and an audio capture source. 


#### Examples


```cpp
HRESULT CreateAggregatedSource(
    IMFMediaSource *pSource1,
    IMFMediaSource *pSource2,
    IMFMediaSource **ppAggSource
    )
{
    *ppAggSource = NULL;

    IMFCollection *pCollection = NULL;

    HRESULT hr = MFCreateCollection(&pCollection);

    if (SUCCEEDED(hr))
    {
        hr = pCollection->AddElement(pSource1);
    }
    if (SUCCEEDED(hr))
    {
        hr = pCollection->AddElement(pSource2);
    }
    if (SUCCEEDED(hr))
    {
        hr = MFCreateAggregateSource(pCollection, ppAggSource);
    }
    SafeRelease(&pCollection);
    return hr;    
}

```

## -see-also

<a href="/windows/desktop/api/mfidl/nn-mfidl-imfmediasource">IMFMediaSource</a>



<a href="/windows/desktop/medfound/media-foundation-functions">Media Foundation Functions</a>