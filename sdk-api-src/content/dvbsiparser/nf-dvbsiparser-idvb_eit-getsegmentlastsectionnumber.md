---
UID: NF:dvbsiparser.IDVB_EIT.GetSegmentLastSectionNumber
title: IDVB_EIT::GetSegmentLastSectionNumber (dvbsiparser.h)
description: This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005 and later.
helpviewer_keywords: ["GetSegmentLastSectionNumber","GetSegmentLastSectionNumber method [Microsoft TV Technologies]","GetSegmentLastSectionNumber method [Microsoft TV Technologies]","IDVB_EIT interface","IDVB_EIT interface [Microsoft TV Technologies]","GetSegmentLastSectionNumber method","IDVB_EIT.GetSegmentLastSectionNumber","IDVB_EIT::GetSegmentLastSectionNumber","IDVB_EITGetSegmentLastSectionNumber","dvbsiparser/IDVB_EIT::GetSegmentLastSectionNumber","mstv.idvb_eit_getsegmentlastsectionnumber"]
old-location: mstv\idvb_eit_getsegmentlastsectionnumber.htm
tech.root: mstv
ms.assetid: 01edaee4-1968-4e6c-8d4f-e1b518f54aaa
ms.date: 12/05/2018
ms.keywords: GetSegmentLastSectionNumber, GetSegmentLastSectionNumber method [Microsoft TV Technologies], GetSegmentLastSectionNumber method [Microsoft TV Technologies],IDVB_EIT interface, IDVB_EIT interface [Microsoft TV Technologies],GetSegmentLastSectionNumber method, IDVB_EIT.GetSegmentLastSectionNumber, IDVB_EIT::GetSegmentLastSectionNumber, IDVB_EITGetSegmentLastSectionNumber, dvbsiparser/IDVB_EIT::GetSegmentLastSectionNumber, mstv.idvb_eit_getsegmentlastsectionnumber
req.header: dvbsiparser.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
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
 - IDVB_EIT::GetSegmentLastSectionNumber
 - dvbsiparser/IDVB_EIT::GetSegmentLastSectionNumber
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
 - IDVB_EIT.GetSegmentLastSectionNumber
---

# IDVB_EIT::GetSegmentLastSectionNumber


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005 and later.
        



The <b>GetSegmentLastSectionNumber</b> method returns the section number of the last section in the subtable that contains this section.

## -parameters

### -param pbVal [out]

Pointer to a variable that receives the last_section_number field

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
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The method succeeded.

</td>
</tr>
</table>

## -see-also

<a href="/previous-versions/windows/desktop/api/dvbsiparser/nn-dvbsiparser-idvb_eit">IDVB_EIT Interface</a>