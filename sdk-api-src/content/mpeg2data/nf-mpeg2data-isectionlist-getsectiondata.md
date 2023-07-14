---
UID: NF:mpeg2data.ISectionList.GetSectionData
title: ISectionList::GetSectionData (mpeg2data.h)
description: The GetSectionData method retrieves a section.
helpviewer_keywords: ["GetSectionData","GetSectionData method [Microsoft TV Technologies]","GetSectionData method [Microsoft TV Technologies]","ISectionList interface","ISectionList interface [Microsoft TV Technologies]","GetSectionData method","ISectionList.GetSectionData","ISectionList::GetSectionData","ISectionListGetSectionData","mpeg2data/ISectionList::GetSectionData","mstv.isectionlist_getsectiondata"]
old-location: mstv\isectionlist_getsectiondata.htm
tech.root: mstv
ms.assetid: b03d1727-9ebd-4e78-b7d0-c6d0959aab8a
ms.date: 12/05/2018
ms.keywords: GetSectionData, GetSectionData method [Microsoft TV Technologies], GetSectionData method [Microsoft TV Technologies],ISectionList interface, ISectionList interface [Microsoft TV Technologies],GetSectionData method, ISectionList.GetSectionData, ISectionList::GetSectionData, ISectionListGetSectionData, mpeg2data/ISectionList::GetSectionData, mstv.isectionlist_getsectiondata
req.header: mpeg2data.h
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
 - ISectionList::GetSectionData
 - mpeg2data/ISectionList::GetSectionData
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Mpeg2data.h
api_name:
 - ISectionList.GetSectionData
---

# ISectionList::GetSectionData


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

The <b>GetSectionData</b> method retrieves a section.

## -parameters

### -param sectionNumber [in]

Specifies the section number to retrieve, indexed from zero. Call the <b>GetNumberOfSections</b> method to get the number of sections.

### -param pdwRawPacketLength [out]

Receives the size of the section data, in bytes.

### -param ppSection [out]

Address of a variable that receives a pointer to a <b>SECTION</b> structure, containing the section data. Do not free the memory for the structure; the object frees the memory when the interface is released.

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
<dt><b>E_ACCESSDENIED</b></dt>
</dl>
</td>
<td width="60%">
The request has not completed yet.

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
<dt><b>MPEG2_E_OUT_OF_BOUNDS</b></dt>
</dl>
</td>
<td width="60%">
The section number is out of range.

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

## -remarks

The section header is converted from network byte order to native byte order. The number of header bytes that are converted depends on the header type. The header types are <i>short header</i> (<a href="/previous-versions/windows/desktop/api/mpeg2structs/ns-mpeg2structs-section">SECTION</a> structure), <i>long header</i> (<a href="/previous-versions/windows/desktop/api/mpeg2structs/ns-mpeg2structs-long_section">LONG_SECTION</a> structure), or <i>DSM-CC header</i> (<a href="/previous-versions/windows/desktop/api/mpeg2structs/ns-mpeg2structs-dsmcc_section">DSMCC_SECTION</a> structure). If the section has a short header, the first three bytes are converted; for a long header, the first eight bytes are converted; and for a DSM-CC header, the first 20 bytes are converted.

The body of the section data, after the header, is left unparsed and unconverted.

## -see-also

<a href="/previous-versions/windows/desktop/api/mpeg2data/nn-mpeg2data-isectionlist">ISectionList Interface</a>