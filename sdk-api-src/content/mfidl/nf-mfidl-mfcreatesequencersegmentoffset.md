---
UID: NF:mfidl.MFCreateSequencerSegmentOffset
title: MFCreateSequencerSegmentOffset function (mfidl.h)
description: Creates a PROPVARIANT that can be used to seek within a sequencer source presentation.
helpviewer_keywords: ["5999af23-03a6-4fd9-8a56-23179164ff32","MFCreateSequencerSegmentOffset","MFCreateSequencerSegmentOffset function [Media Foundation]","mf.mfcreatesequencersegmentoffset","mfidl/MFCreateSequencerSegmentOffset"]
old-location: mf\mfcreatesequencersegmentoffset.htm
tech.root: mf
ms.assetid: 5999af23-03a6-4fd9-8a56-23179164ff32
ms.date: 12/05/2018
ms.keywords: 5999af23-03a6-4fd9-8a56-23179164ff32, MFCreateSequencerSegmentOffset, MFCreateSequencerSegmentOffset function [Media Foundation], mf.mfcreatesequencersegmentoffset, mfidl/MFCreateSequencerSegmentOffset
req.header: mfidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
 - MFCreateSequencerSegmentOffset
 - mfidl/MFCreateSequencerSegmentOffset
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
 - MFCreateSequencerSegmentOffset
---

# MFCreateSequencerSegmentOffset function


## -description

Creates a <b>PROPVARIANT</b> that can be used to seek within a sequencer source presentation.

## -parameters

### -param dwId [in]

Sequencer element identifier. This value specifies the segment in which to begin playback. The element identifier is returned in the <a href="/windows/desktop/api/mfidl/nf-mfidl-imfsequencersource-appendtopology">IMFSequencerSource::AppendTopology</a> method.

### -param hnsOffset [in]

Starting position within the segment, in 100-nanosecond units.

### -param pvarSegmentOffset [out]

Pointer to a <b>PROPVARIANT</b>. The method fills in the <b>PROPVARIANT</b> with the information needed for performing a seek operation. The caller must free the <b>PROPVARIANT</b> by calling <b>PropVariantClear</b>.

## -returns

If this function succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

The <b>PROPVARIANT</b> returned in <i>pvarSegmentOffset</i> can be used for the <i>pvarStartPosition</i> parameter in the <a href="/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-start">IMFMediaSession::Start</a> method. Use the time format <b>GUID MF_TIME_FORMAT_SEGMENT_OFFSET</b>.
      


#### Examples


```cpp
// Skips to the specified segment in the sequencer source

HRESULT CPlaylist::SkipTo(DWORD index)
{
    if (index >= m_count)
    {
        return E_INVALIDARG;
    }

    MFSequencerElementId ID = m_segments[index].SegmentID;

    PROPVARIANT var;

    HRESULT hr = MFCreateSequencerSegmentOffset(ID, NULL, &var);
    
    if (SUCCEEDED(hr))
    {
        hr = m_pSession->Start(&MF_TIME_FORMAT_SEGMENT_OFFSET, &var);
        PropVariantClear(&var);
    }
    return hr;
}

```

## -see-also

<a href="/windows/desktop/medfound/mftime">MFTIME</a>



<a href="/windows/desktop/medfound/media-foundation-functions">Media Foundation Functions</a>



<a href="/windows/desktop/medfound/sequencer-source">Sequencer Source</a>



<a href="/windows/desktop/medfound/using-the-sequencer-source">Using the Sequencer Source</a>