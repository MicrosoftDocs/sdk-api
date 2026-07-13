---
UID: NF:segment.IMSVidFilePlayback2.put___SourceFilter
title: IMSVidFilePlayback2::put___SourceFilter (segment.h)
description: This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005 or later.
helpviewer_keywords: ["IMSVidFilePlayback2 interface [Microsoft TV Technologies]","put___SourceFilter method","IMSVidFilePlayback2.put___SourceFilter","IMSVidFilePlayback2::put___SourceFilter","IMSVidFilePlayback2put___SourceFilter","mstv.imsvidfileplayback2_put___sourcefilter","put___SourceFilter","put___SourceFilter method [Microsoft TV Technologies]","put___SourceFilter method [Microsoft TV Technologies]","IMSVidFilePlayback2 interface","segment/IMSVidFilePlayback2::put___SourceFilter"]
old-location: mstv\imsvidfileplayback2_put___sourcefilter.htm
tech.root: mstv
ms.assetid: 257e93ec-fb26-45fb-b07b-4491dbf2528a
ms.date: 12/05/2018
ms.keywords: IMSVidFilePlayback2 interface [Microsoft TV Technologies],put___SourceFilter method, IMSVidFilePlayback2.put___SourceFilter, IMSVidFilePlayback2::put___SourceFilter, IMSVidFilePlayback2put___SourceFilter, mstv.imsvidfileplayback2_put___sourcefilter, put___SourceFilter, put___SourceFilter method [Microsoft TV Technologies], put___SourceFilter method [Microsoft TV Technologies],IMSVidFilePlayback2 interface, segment/IMSVidFilePlayback2::put___SourceFilter
req.header: segment.h
req.include-header: Msvidctl.h
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Segment.idl
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
 - IMSVidFilePlayback2::put___SourceFilter
 - segment/IMSVidFilePlayback2::put___SourceFilter
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - segment.h
api_name:
 - IMSVidFilePlayback2.put___SourceFilter
---

# IMSVidFilePlayback2::put___SourceFilter


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005 or later.
        



The <b>put___SourceFilter</b> method sets the CLSID of a DirectShow source filter to use for this source.

## -parameters

### -param FileName [in]

Specifies the CLSID of the source filter.

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

## -remarks

If the CLSID is GUID_NULL, the <a href="/previous-versions/windows/desktop/mstv/msvidfileplaybackdevice">MSVidFilePlaybackDevice</a> object uses the default source filter for the file name given in <a href="/windows/desktop/api/segment/nf-segment-imsvidfileplayback-put_filename">IMSVidFilePlayback::put_FileName</a>.

## -see-also

<a href="/windows/desktop/api/segment/nn-segment-imsvidfileplayback2">IMSVidFilePlayback2 Interface</a>