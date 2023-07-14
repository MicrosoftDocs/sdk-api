---
UID: NF:mpeg2data.IMpeg2Data.GetStreamOfSections
title: IMpeg2Data::GetStreamOfSections (mpeg2data.h)
description: GetStreamOfSections is no longer available for use as of Windows 7.
helpviewer_keywords: ["GetStreamOfSections","GetStreamOfSections method [Microsoft TV Technologies]","GetStreamOfSections method [Microsoft TV Technologies]","IMpeg2Data interface","IMpeg2Data interface [Microsoft TV Technologies]","GetStreamOfSections method","IMpeg2Data.GetStreamOfSections","IMpeg2Data::GetStreamOfSections","IMpeg2DataGetStreamOfSections","mpeg2data/IMpeg2Data::GetStreamOfSections","mstv.impeg2data_getstreamofsections"]
old-location: mstv\impeg2data_getstreamofsections.htm
tech.root: mstv
ms.assetid: 896080ff-cdf0-40b1-ba4e-d94de527d86e
ms.date: 12/05/2018
ms.keywords: GetStreamOfSections, GetStreamOfSections method [Microsoft TV Technologies], GetStreamOfSections method [Microsoft TV Technologies],IMpeg2Data interface, IMpeg2Data interface [Microsoft TV Technologies],GetStreamOfSections method, IMpeg2Data.GetStreamOfSections, IMpeg2Data::GetStreamOfSections, IMpeg2DataGetStreamOfSections, mpeg2data/IMpeg2Data::GetStreamOfSections, mstv.impeg2data_getstreamofsections
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
 - IMpeg2Data::GetStreamOfSections
 - mpeg2data/IMpeg2Data::GetStreamOfSections
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
 - IMpeg2Data.GetStreamOfSections
---

# IMpeg2Data::GetStreamOfSections


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

<p class="CCE_Message">[<b>GetStreamOfSections</b> is no longer available for use as of Windows 7. Instead, use the <a href="/windows/desktop/api/mpeg2psiparser/nn-mpeg2psiparser-ipsitables">IPSITables</a> interface to get program specific information (PSI) tables from an MPEG-2 transport stream.]

The <b>GetStreamOfSections</b> method starts an ongoing request for specific MPEG-2 table sections.

## -parameters

### -param pid [in]

Specifies the packet identifier (PID) of the transport stream packets to examine.

### -param tid [in]

Specifies the table identifier (TID) of the section to retrieve.

### -param pFilter [in]

Optional pointer to an <a href="/previous-versions/windows/desktop/api/mpeg2structs/ns-mpeg2structs-mpeg2_filter">MPEG2_FILTER</a> structure. The caller can use this parameter to exclude packets based on additional MPEG-2 header fields. This parameter can be <b>NULL</b>.

### -param hDataReadyEvent [in]

Handle to an event created by the caller. The filter signals this event whenever it receives new data.

### -param ppMpegStream [out]

Pointer to a variable that receives an <a href="/previous-versions/windows/desktop/api/mpeg2data/nn-mpeg2data-impeg2stream">IMpeg2Stream</a> interface pointer. The caller must release the interface. Use this interface to retrieve the data when it arrives.

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
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
Invalid argument.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
<b>NULL</b> pointer argument.

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

<a href="/previous-versions/windows/desktop/api/mpeg2data/nn-mpeg2data-impeg2data">IMpeg2Data Interface</a>