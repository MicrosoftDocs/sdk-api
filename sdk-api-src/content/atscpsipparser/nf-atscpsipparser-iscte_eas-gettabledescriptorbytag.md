---
UID: NF:atscpsipparser.ISCTE_EAS.GetTableDescriptorByTag
title: ISCTE_EAS::GetTableDescriptorByTag (atscpsipparser.h)
description: The GetTableDescriptorByTag method searches the EAS table for a descriptor with the specified descriptor tag.
helpviewer_keywords: ["GetTableDescriptorByTag","GetTableDescriptorByTag method [Microsoft TV Technologies]","GetTableDescriptorByTag method [Microsoft TV Technologies]","ISCTE_EAS interface","ISCTE_EAS interface [Microsoft TV Technologies]","GetTableDescriptorByTag method","ISCTE_EAS.GetTableDescriptorByTag","ISCTE_EAS::GetTableDescriptorByTag","ISCTE_EASGetTableDescriptorByTag","atscpsipparser/ISCTE_EAS::GetTableDescriptorByTag","mstv.iscte_eas_gettabledescriptorbytag"]
old-location: mstv\iscte_eas_gettabledescriptorbytag.htm
tech.root: mstv
ms.assetid: 91e0aad8-31d9-44d1-9bda-7f0134f5457b
ms.date: 12/05/2018
ms.keywords: GetTableDescriptorByTag, GetTableDescriptorByTag method [Microsoft TV Technologies], GetTableDescriptorByTag method [Microsoft TV Technologies],ISCTE_EAS interface, ISCTE_EAS interface [Microsoft TV Technologies],GetTableDescriptorByTag method, ISCTE_EAS.GetTableDescriptorByTag, ISCTE_EAS::GetTableDescriptorByTag, ISCTE_EASGetTableDescriptorByTag, atscpsipparser/ISCTE_EAS::GetTableDescriptorByTag, mstv.iscte_eas_gettabledescriptorbytag
req.header: atscpsipparser.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: None supported
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
 - ISCTE_EAS::GetTableDescriptorByTag
 - atscpsipparser/ISCTE_EAS::GetTableDescriptorByTag
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - atscpsipparser.h
api_name:
 - ISCTE_EAS.GetTableDescriptorByTag
---

# ISCTE_EAS::GetTableDescriptorByTag


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

The <b>GetTableDescriptorByTag</b> method searches the EAS table for a descriptor with the specified descriptor tag.

## -parameters

### -param bTag [in]

The descriptor tag to search for.

### -param pdwCookie [in, out]

A pointer to a variable that specifies the start position in the descriptor list. This parameter can be <b>NULL</b>. If the value is <b>NULL</b>, the search starts from the first descriptor in the list. Otherwise, the search starts from the position given in *<i>pdwCookie</i>. When the method returns, the <i>pdwCookie</i> parameter contains the position of the next matching descriptor, if any. You can use this parameter to iterate through the descriptor list, looking for every instance of a particular descriptor tag.

### -param ppDescriptor [out]

Receives a pointer to the <a href="/windows/desktop/api/mpeg2psiparser/nn-mpeg2psiparser-igenericdescriptor">IGenericDescriptor</a> interface. Use this interface to retrieve the information in the descriptor. The caller must release the interface.

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
<dt><b>MPEG2_E_NOT_PRESENT</b></dt>
</dl>
</td>
<td width="60%">
The specified tag was not found.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MPEG2_E_OUT_OF_BOUNDS</b></dt>
</dl>
</td>
<td width="60%">
Index out of bounds.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MPEG2_E_UNINITIALIZED</b></dt>
</dl>
</td>
<td width="60%">
The <a href="/previous-versions/windows/desktop/api/atscpsipparser/nf-atscpsipparser-iscte_eas-initialize">ISCTE_EAS::Initialize</a> method was not called.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MPEG2_S_MORE_DATA_AVAILABLE</b></dt>
</dl>
</td>
<td width="60%">
The record contains at least one more descriptor with this tag.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MPEG2_S_NO_MORE_DATA_AVAILABLE</b></dt>
</dl>
</td>
<td width="60%">
The record does not contain any more descriptors with this tag.

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

<a href="/previous-versions/windows/desktop/api/atscpsipparser/nn-atscpsipparser-iscte_eas">ISCTE_EAS Interface</a>