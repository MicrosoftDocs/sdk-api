---
UID: NF:mpeg2data.IMpeg2Data.GetTable
title: IMpeg2Data::GetTable (mpeg2data.h)
description: GetTable is no longer available for use as of Windows 7.
helpviewer_keywords: ["GetTable","GetTable method [Microsoft TV Technologies]","GetTable method [Microsoft TV Technologies]","IMpeg2Data interface","IMpeg2Data interface [Microsoft TV Technologies]","GetTable method","IMpeg2Data.GetTable","IMpeg2Data::GetTable","IMpeg2DataGetTable","mpeg2data/IMpeg2Data::GetTable","mstv.impeg2data_gettable"]
old-location: mstv\impeg2data_gettable.htm
tech.root: mstv
ms.assetid: c76a9117-5dd7-46fc-8390-3f1ec80f6499
ms.date: 12/05/2018
ms.keywords: GetTable, GetTable method [Microsoft TV Technologies], GetTable method [Microsoft TV Technologies],IMpeg2Data interface, IMpeg2Data interface [Microsoft TV Technologies],GetTable method, IMpeg2Data.GetTable, IMpeg2Data::GetTable, IMpeg2DataGetTable, mpeg2data/IMpeg2Data::GetTable, mstv.impeg2data_gettable
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
 - IMpeg2Data::GetTable
 - mpeg2data/IMpeg2Data::GetTable
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
 - IMpeg2Data.GetTable
---

# IMpeg2Data::GetTable


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

<p class="CCE_Message">[<b>GetTable</b> is no longer available for use as of Windows 7. Instead, use the <a href="/windows/desktop/api/mpeg2psiparser/nn-mpeg2psiparser-ipsitables">IPSITables</a> interface to get program specific information (PSI) tables from an MPEG-2 transport stream.]

Retrieves a complete MPEG-2 PSI table. This method blocks until the filter receives all of the sections that make up the requested table, or until the specified time out elapses.

## -parameters

### -param pid [in]

Specifies the packet identifier (PID) of the transport stream packets to examine.

### -param tid [in]

Specifies the table identifier (TID) of the section to retrieve.

### -param pFilter [in]

Optional pointer to an <a href="/previous-versions/windows/desktop/api/mpeg2structs/ns-mpeg2structs-mpeg2_filter">MPEG2_FILTER</a> structure. The caller can use this parameter to exclude packets based on additional MPEG-2 header fields. This parameter can be <b>NULL</b>.

### -param dwTimeout [in]

Specifies a time-out value, in milliseconds. If the filter does not receive a matching section within the time-out period, the method fails.

### -param ppSectionList [out]

Receives an <a href="/previous-versions/windows/desktop/api/mpeg2data/nn-mpeg2data-isectionlist">ISectionList</a> interface pointer. Use this interface to retrieve the section data. The caller must release the interface.

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
<dt><b>MPEG2_E_SECTION_NOT_FOUND</b></dt>
</dl>
</td>
<td width="60%">
The filter did not receive a matching table section.

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

You can use the <i>pFilter</i> parameter to specify the Table_ID_extension field or the version number field. Otherwise, the filter caches these values from the first section that matches the search criteria. It uses those values to match subsequent sections.

## -see-also

<a href="/previous-versions/windows/desktop/api/mpeg2data/nn-mpeg2data-impeg2data">IMpeg2Data Interface</a>