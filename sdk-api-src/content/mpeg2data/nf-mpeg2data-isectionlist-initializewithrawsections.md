---
UID: NF:mpeg2data.ISectionList.InitializeWithRawSections
title: ISectionList::InitializeWithRawSections (mpeg2data.h)
description: The InitializeWithRawSections method initializes the object with raw section data. This method allows for custom processing of section data.
helpviewer_keywords: ["ISectionList interface [Microsoft TV Technologies]","InitializeWithRawSections method","ISectionList.InitializeWithRawSections","ISectionList::InitializeWithRawSections","ISectionListInitializeWithRawSections","InitializeWithRawSections","InitializeWithRawSections method [Microsoft TV Technologies]","InitializeWithRawSections method [Microsoft TV Technologies]","ISectionList interface","mpeg2data/ISectionList::InitializeWithRawSections","mstv.isectionlist_initializewithrawsections"]
old-location: mstv\isectionlist_initializewithrawsections.htm
tech.root: mstv
ms.assetid: 61f1e99b-c375-4aa3-a11b-7e24c35f71ca
ms.date: 12/05/2018
ms.keywords: ISectionList interface [Microsoft TV Technologies],InitializeWithRawSections method, ISectionList.InitializeWithRawSections, ISectionList::InitializeWithRawSections, ISectionListInitializeWithRawSections, InitializeWithRawSections, InitializeWithRawSections method [Microsoft TV Technologies], InitializeWithRawSections method [Microsoft TV Technologies],ISectionList interface, mpeg2data/ISectionList::InitializeWithRawSections, mstv.isectionlist_initializewithrawsections
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
 - ISectionList::InitializeWithRawSections
 - mpeg2data/ISectionList::InitializeWithRawSections
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
 - ISectionList.InitializeWithRawSections
---

# ISectionList::InitializeWithRawSections


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

The <b>InitializeWithRawSections</b> method initializes the object with raw section data. This method allows for custom processing of section data.

## -parameters

### -param pmplSections [in]

Pointer to an <a href="/previous-versions/windows/desktop/api/mpeg2structs/ns-mpeg2structs-mpeg_packet_list">MPEG_PACKET_LIST</a> structure that contains a list of MPEG-2 sections.

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
<dt><b>MPEG2_E_ALREADY_INITIALIZED</b></dt>
</dl>
</td>
<td width="60%">
The object has already been initialized.

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

Use this method as follows:

<ol>
<li>Get the section data by calling the <a href="/previous-versions/windows/desktop/api/mpeg2data/nf-mpeg2data-impeg2data-getstreamofsections">IMpeg2Data::GetStreamOfSections</a> method.</li>
<li>Create a new <b>SectionList</b> object and call <b>InitializeWithRawSections</b> with the section data.</li>
</ol>

## -see-also

<a href="/previous-versions/windows/desktop/api/mpeg2data/nn-mpeg2data-isectionlist">ISectionList Interface</a>