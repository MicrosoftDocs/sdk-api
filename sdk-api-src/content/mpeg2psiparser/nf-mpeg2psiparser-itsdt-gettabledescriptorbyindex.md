---
UID: NF:mpeg2psiparser.ITSDT.GetTableDescriptorByIndex
title: ITSDT::GetTableDescriptorByIndex (mpeg2psiparser.h)
description: This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005.
helpviewer_keywords: ["GetTableDescriptorByIndex","GetTableDescriptorByIndex method [Microsoft TV Technologies]","GetTableDescriptorByIndex method [Microsoft TV Technologies]","ITSDT interface","ITSDT interface [Microsoft TV Technologies]","GetTableDescriptorByIndex method","ITSDT.GetTableDescriptorByIndex","ITSDT::GetTableDescriptorByIndex","ITSDTGetTableDescriptorByIndex","mpeg2psiparser/ITSDT::GetTableDescriptorByIndex","mstv.itsdt_gettabledescriptorbyindex"]
old-location: mstv\itsdt_gettabledescriptorbyindex.htm
tech.root: mstv
ms.assetid: 9adcc8f6-44a7-41c6-b42a-e45c33cd5d6a
ms.date: 12/05/2018
ms.keywords: GetTableDescriptorByIndex, GetTableDescriptorByIndex method [Microsoft TV Technologies], GetTableDescriptorByIndex method [Microsoft TV Technologies],ITSDT interface, ITSDT interface [Microsoft TV Technologies],GetTableDescriptorByIndex method, ITSDT.GetTableDescriptorByIndex, ITSDT::GetTableDescriptorByIndex, ITSDTGetTableDescriptorByIndex, mpeg2psiparser/ITSDT::GetTableDescriptorByIndex, mstv.itsdt_gettabledescriptorbyindex
req.header: mpeg2psiparser.h
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
 - ITSDT::GetTableDescriptorByIndex
 - mpeg2psiparser/ITSDT::GetTableDescriptorByIndex
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Mpeg2PsiParser.h
api_name:
 - ITSDT.GetTableDescriptorByIndex
---

# ITSDT::GetTableDescriptorByIndex


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005.
        



The <b>GetTableDescriptorByIndex</b> method retrieves a table descriptor for the TSDT.

## -parameters

### -param dwIndex [in]

Specifies which descriptor to retrieve, indexed from zero. Call the <a href="/windows/desktop/api/mpeg2psiparser/nf-mpeg2psiparser-itsdt-getcountoftabledescriptors">ITSDT::GetCountOfTableDescriptors</a> method to get the number of table descriptors in the TSDT.

### -param ppDescriptor [out]

Address of a variable that receives an <a href="/windows/desktop/api/mpeg2psiparser/nn-mpeg2psiparser-igenericdescriptor">IGenericDescriptor</a> interface pointer. Use this interface to retrieve the information in the descriptor. The caller must release the interface.

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

<a href="/windows/desktop/api/mpeg2psiparser/nn-mpeg2psiparser-itsdt">ITSDT Interface</a>