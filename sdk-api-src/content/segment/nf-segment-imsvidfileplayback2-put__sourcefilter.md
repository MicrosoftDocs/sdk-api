---
UID: NF:segment.IMSVidFilePlayback2.put__SourceFilter
title: IMSVidFilePlayback2::put__SourceFilter (segment.h)
description: This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005 or later.
helpviewer_keywords: ["IMSVidFilePlayback2 interface [Microsoft TV Technologies]","put__SourceFilter method","IMSVidFilePlayback2.put__SourceFilter","IMSVidFilePlayback2::put__SourceFilter","IMSVidFilePlayback2put__SourceFilter","mstv.imsvidfileplayback2_put__sourcefilter","put__SourceFilter","put__SourceFilter method [Microsoft TV Technologies]","put__SourceFilter method [Microsoft TV Technologies]","IMSVidFilePlayback2 interface","segment/IMSVidFilePlayback2::put__SourceFilter"]
old-location: mstv\imsvidfileplayback2_put__sourcefilter.htm
tech.root: mstv
ms.assetid: ef536087-dd2b-417f-b139-916d930e3d25
ms.date: 12/05/2018
ms.keywords: IMSVidFilePlayback2 interface [Microsoft TV Technologies],put__SourceFilter method, IMSVidFilePlayback2.put__SourceFilter, IMSVidFilePlayback2::put__SourceFilter, IMSVidFilePlayback2put__SourceFilter, mstv.imsvidfileplayback2_put__sourcefilter, put__SourceFilter, put__SourceFilter method [Microsoft TV Technologies], put__SourceFilter method [Microsoft TV Technologies],IMSVidFilePlayback2 interface, segment/IMSVidFilePlayback2::put__SourceFilter
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
 - IMSVidFilePlayback2::put__SourceFilter
 - segment/IMSVidFilePlayback2::put__SourceFilter
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
 - IMSVidFilePlayback2.put__SourceFilter
---

# IMSVidFilePlayback2::put__SourceFilter


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005 or later.
        



The <b>put__SourceFilter</b> method sets the CLSID of a DirectShow source filter to use for this source. The CLSID is specified as a string.

## -parameters

### -param FileName [in]

<b>BSTR</b> that contains the CLSID of the source filter. The <b>BSTR</b> must use the following format: <code>{XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX}</code>.

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