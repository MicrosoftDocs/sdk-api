---
UID: NF:segment.IMSVidGenericSink2.AddFilter
title: IMSVidGenericSink2::AddFilter (segment.h)
description: Note  This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005 or later. .
helpviewer_keywords: ["AddFilter","AddFilter method [Microsoft TV Technologies]","AddFilter method [Microsoft TV Technologies]","IMSVidGenericSink2 interface","IMSVidGenericSink2 interface [Microsoft TV Technologies]","AddFilter method","IMSVidGenericSink2.AddFilter","IMSVidGenericSink2::AddFilter","IMSVidGenericSink2AddFilter","mstv.imsvidgenericsink2_addfilter","segment/IMSVidGenericSink2::AddFilter"]
old-location: mstv\imsvidgenericsink2_addfilter.htm
tech.root: mstv
ms.assetid: b0044995-5bca-4f49-a22b-00df8f73b47f
ms.date: 12/05/2018
ms.keywords: AddFilter, AddFilter method [Microsoft TV Technologies], AddFilter method [Microsoft TV Technologies],IMSVidGenericSink2 interface, IMSVidGenericSink2 interface [Microsoft TV Technologies],AddFilter method, IMSVidGenericSink2.AddFilter, IMSVidGenericSink2::AddFilter, IMSVidGenericSink2AddFilter, mstv.imsvidgenericsink2_addfilter, segment/IMSVidGenericSink2::AddFilter
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
 - IMSVidGenericSink2::AddFilter
 - segment/IMSVidGenericSink2::AddFilter
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
 - IMSVidGenericSink2.AddFilter
---

# IMSVidGenericSink2::AddFilter


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

<div class="alert"><b>Note</b>  This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005 or later.</div>
<div> </div>




The <b>AddFilter</b> method specifies a DirectShow filter that is added to the graph when this segment is built.

## -parameters

### -param bstrName

<b>BSTR</b> that contains the CLSID of the filter. The <b>BSTR</b> must use the following format: <code>{XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX}</code>

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

Use this method to insert additional filters to the graph other than the sink filter. To specify the sink filter, call <a href="/windows/desktop/api/segment/nf-segment-imsvidgenericsink-setsinkfilter">IMSVidGenericSink::SetSinkFilter</a>.

## -see-also

<a href="/windows/desktop/api/segment/nn-segment-imsvidgenericsink2">IMSVidGenericSink2 Interface</a>