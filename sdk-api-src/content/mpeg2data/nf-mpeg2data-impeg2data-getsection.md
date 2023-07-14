---
UID: NF:mpeg2data.IMpeg2Data.GetSection
title: IMpeg2Data::GetSection (mpeg2data.h)
description: GetSection is no longer available for use as of Windows 7.
helpviewer_keywords: ["GetSection","GetSection method [Microsoft TV Technologies]","GetSection method [Microsoft TV Technologies]","IMpeg2Data interface","IMpeg2Data interface [Microsoft TV Technologies]","GetSection method","IMpeg2Data.GetSection","IMpeg2Data::GetSection","IMpeg2DataGetSection","mpeg2data/IMpeg2Data::GetSection","mstv.impeg2data_getsection"]
old-location: mstv\impeg2data_getsection.htm
tech.root: mstv
ms.assetid: 9fb0d10f-7f9a-452d-9725-546d372430bd
ms.date: 12/05/2018
ms.keywords: GetSection, GetSection method [Microsoft TV Technologies], GetSection method [Microsoft TV Technologies],IMpeg2Data interface, IMpeg2Data interface [Microsoft TV Technologies],GetSection method, IMpeg2Data.GetSection, IMpeg2Data::GetSection, IMpeg2DataGetSection, mpeg2data/IMpeg2Data::GetSection, mstv.impeg2data_getsection
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
 - IMpeg2Data::GetSection
 - mpeg2data/IMpeg2Data::GetSection
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
 - IMpeg2Data.GetSection
---

# IMpeg2Data::GetSection


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

<p class="CCE_Message">[<b>GetSection</b> is no longer available for use as of Windows 7. Instead, use the <a href="/windows/desktop/api/mpeg2psiparser/nn-mpeg2psiparser-ipsitables">IPSITables</a> interface to get program specific information (PSI) tables from an MPEG-2 transport stream.]

The <b>GetSection</b> method retrieves an MPEG-2 table section. This method blocks until the filter receives a matching table section, or until the specified time out elapses.

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

Pointer to a variable that receives an <a href="/previous-versions/windows/desktop/api/mpeg2data/nn-mpeg2data-isectionlist">ISectionList</a> interface pointer. Use this interface to retrieve the section data. The caller must release the interface.

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
<dt><b>MPEG2_E_SECTION_NOT_FOUND</b></dt>
</dl>
</td>
<td width="60%">
The filter did not receive a matching table section.

</td>
</tr>
</table>

## -see-also

<a href="/previous-versions/windows/desktop/api/mpeg2data/nn-mpeg2data-impeg2data">IMpeg2Data Interface</a>