---
UID: NF:dvbsiparser.IDVB_EIT2.GetSegmentInfo
title: IDVB_EIT2::GetSegmentInfo (dvbsiparser.h)
description: Gets the table identifier and segment number for the current EIT segment.
helpviewer_keywords: ["GetSegmentInfo","GetSegmentInfo method [Microsoft TV Technologies]","GetSegmentInfo method [Microsoft TV Technologies]","IDVB_EIT2 interface","IDVB_EIT2 interface [Microsoft TV Technologies]","GetSegmentInfo method","IDVB_EIT2.GetSegmentInfo","IDVB_EIT2::GetSegmentInfo","dvbsiparser/IDVB_EIT2::GetSegmentInfo","mstv.idvb_eit2_getsegmentinfo"]
old-location: mstv\idvb_eit2_getsegmentinfo.htm
tech.root: mstv
ms.assetid: acc83c4e-7ec5-43f3-8d29-5c974fea91b8
ms.date: 12/05/2018
ms.keywords: GetSegmentInfo, GetSegmentInfo method [Microsoft TV Technologies], GetSegmentInfo method [Microsoft TV Technologies],IDVB_EIT2 interface, IDVB_EIT2 interface [Microsoft TV Technologies],GetSegmentInfo method, IDVB_EIT2.GetSegmentInfo, IDVB_EIT2::GetSegmentInfo, dvbsiparser/IDVB_EIT2::GetSegmentInfo, mstv.idvb_eit2_getsegmentinfo
req.header: dvbsiparser.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: None supported
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Dvbsiparser.idl
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
 - IDVB_EIT2::GetSegmentInfo
 - dvbsiparser/IDVB_EIT2::GetSegmentInfo
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - dvbsiparser.h
api_name:
 - IDVB_EIT2.GetSegmentInfo
---

# IDVB_EIT2::GetSegmentInfo


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

Gets the table identifier and segment number for the current EIT segment.

## -parameters

### -param pbTid [out]

Receives the table identifier.

### -param pbSegment [out]

Receives the segment number.

## -returns

The method returns an <b>HRESULT</b>. Possible values include those in the following table.

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
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
NULL pointer argument.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MPEG2_E_UNINITIALIZED</b></dt>
</dl>
</td>
<td width="60%">
The <a href="/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-idvb_eit-initialize">Initialize</a> method was not called.

</td>
</tr>
</table>

## -see-also

<a href="/previous-versions/windows/desktop/api/dvbsiparser/nn-dvbsiparser-idvb_eit2">IDVB_EIT2</a>