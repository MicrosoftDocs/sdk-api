---
UID: NF:atscpsipparser.IATSC_VCT.GetTableDescriptorByIndex
title: IATSC_VCT::GetTableDescriptorByIndex (atscpsipparser.h)
description: This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005 and later.
helpviewer_keywords: ["GetTableDescriptorByIndex","GetTableDescriptorByIndex method [Microsoft TV Technologies]","GetTableDescriptorByIndex method [Microsoft TV Technologies]","IATSC_VCT interface","IATSC_VCT interface [Microsoft TV Technologies]","GetTableDescriptorByIndex method","IATSC_VCT.GetTableDescriptorByIndex","IATSC_VCT::GetTableDescriptorByIndex","IATSC_VCTGetTableDescriptorByIndex","atscpsipparser/IATSC_VCT::GetTableDescriptorByIndex","mstv.iatsc_vct_gettabledescriptorbyindex"]
old-location: mstv\iatsc_vct_gettabledescriptorbyindex.htm
tech.root: mstv
ms.assetid: 964ae371-e7a5-4278-8408-b39ae4371135
ms.date: 12/05/2018
ms.keywords: GetTableDescriptorByIndex, GetTableDescriptorByIndex method [Microsoft TV Technologies], GetTableDescriptorByIndex method [Microsoft TV Technologies],IATSC_VCT interface, IATSC_VCT interface [Microsoft TV Technologies],GetTableDescriptorByIndex method, IATSC_VCT.GetTableDescriptorByIndex, IATSC_VCT::GetTableDescriptorByIndex, IATSC_VCTGetTableDescriptorByIndex, atscpsipparser/IATSC_VCT::GetTableDescriptorByIndex, mstv.iatsc_vct_gettabledescriptorbyindex
req.header: atscpsipparser.h
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
 - IATSC_VCT::GetTableDescriptorByIndex
 - atscpsipparser/IATSC_VCT::GetTableDescriptorByIndex
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
 - IATSC_VCT.GetTableDescriptorByIndex
---

# IATSC_VCT::GetTableDescriptorByIndex


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005 and later.
        



The <b>GetTableDescriptorByIndex</b> method returns a table-wide descriptor for the VCT.

## -parameters

### -param dwIndex [in]

Specifies which descriptor to retrieve, indexed from zero. Call the <a href="/previous-versions/windows/desktop/api/atscpsipparser/nf-atscpsipparser-iatsc_vct-getcountoftabledescriptors">IATSC_VCT::GetCountOfTableDescriptors</a> method to get the number of table descriptors in the VCT.

### -param ppDescriptor [out]

Receives a pointer to the <a href="/windows/desktop/api/mpeg2psiparser/nn-mpeg2psiparser-igenericdescriptor">IGenericDescriptor</a> interface. Use this interface to retrieve the information in the descriptor. The caller must release the interface.

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
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The method succeeded.

</td>
</tr>
</table>

## -see-also

<a href="/previous-versions/windows/desktop/api/atscpsipparser/nn-atscpsipparser-iatsc_vct">IATSC_VCT Interface</a>