---
UID: NF:mfidl.MFCreateSequencerSegmentOffset
title: MFCreateSequencerSegmentOffset function
author: windows-sdk-content
description: Creates a PROPVARIANT that can be used to seek within a sequencer source presentation.
old-location: mf\mfcreatesequencersegmentoffset.htm
tech.root: medfound
ms.assetid: 5999af23-03a6-4fd9-8a56-23179164ff32
ms.author: windowssdkdev
ms.date: 11/09/2018
ms.keywords: 5999af23-03a6-4fd9-8a56-23179164ff32, MFCreateSequencerSegmentOffset, MFCreateSequencerSegmentOffset function [Media Foundation], mf.mfcreatesequencersegmentoffset, mfidl/MFCreateSequencerSegmentOffset
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - mf.dll
api_name:
 - MFCreateSequencerSegmentOffset
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- 
: 
- MFCreateSequencerSegmentOffset
: 
---

# MFCreateSequencerSegmentOffset function


## -description


Creates a <b>PROPVARIANT</b> that can be used to seek within a sequencer source presentation.
        


## -parameters




### -param dwId [in]

Sequencer element identifier. This value specifies the segment in which to begin playback. The element identifier is returned in the <a href="https://msdn.microsoft.com/4ff20d56-6095-495d-89ee-9086c61da8ac">IMFSequencerSource::AppendTopology</a> method.
          


### -param hnsOffset [in]

Starting position within the segment, in 100-nanosecond units.
          


### -param pvarSegmentOffset [out]

Pointer to a <b>PROPVARIANT</b>. The method fills in the <b>PROPVARIANT</b> with the information needed for performing a seek operation. The caller must free the <b>PROPVARIANT</b> by calling <b>PropVariantClear</b>.
          


## -returns



If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



The <b>PROPVARIANT</b> returned in <i>pvarSegmentOffset</i> can be used for the <i>pvarStartPosition</i> parameter in the <a href="https://msdn.microsoft.com/1bdec0c0-b042-4e5e-a72b-b15942750ced">IMFMediaSession::Start</a> method. Use the time format <b>GUID MF_TIME_FORMAT_SEGMENT_OFFSET</b>.
      


#### Examples

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>// Skips to the specified segment in the sequencer source

HRESULT CPlaylist::SkipTo(DWORD index)
{
    if (index &gt;= m_count)
    {
        return E_INVALIDARG;
    }

    MFSequencerElementId ID = m_segments[index].SegmentID;

    PROPVARIANT var;

    HRESULT hr = MFCreateSequencerSegmentOffset(ID, NULL, &amp;var);
    
    if (SUCCEEDED(hr))
    {
        hr = m_pSession-&gt;Start(&amp;MF_TIME_FORMAT_SEGMENT_OFFSET, &amp;var);
        PropVariantClear(&amp;var);
    }
    return hr;
}
</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/9273ff1f-382e-4c58-b571-4852545915b3">MFTIME</a>



<a href="https://msdn.microsoft.com/3018ffa7-e709-45b0-8b2b-7640d5633378">Media Foundation Functions</a>



<a href="https://msdn.microsoft.com/788ede68-2fd7-45f6-90cb-2426c40f7d4c">Sequencer Source</a>



<a href="https://msdn.microsoft.com/7ce8dc67-02b1-4fd4-9e4d-6614fdb40620">Using the Sequencer Source</a>
 

 

