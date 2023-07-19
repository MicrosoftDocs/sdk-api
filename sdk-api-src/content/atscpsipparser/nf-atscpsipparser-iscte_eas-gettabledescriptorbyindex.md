---
UID: NF:atscpsipparser.ISCTE_EAS.GetTableDescriptorByIndex
title: ISCTE_EAS::GetTableDescriptorByIndex (atscpsipparser.h)
description: The GetTableDescriptorByIndex method returns a descriptor for the EAS table.
helpviewer_keywords: ["GetTableDescriptorByIndex","GetTableDescriptorByIndex method [Microsoft TV Technologies]","GetTableDescriptorByIndex method [Microsoft TV Technologies]","ISCTE_EAS interface","ISCTE_EAS interface [Microsoft TV Technologies]","GetTableDescriptorByIndex method","ISCTE_EAS.GetTableDescriptorByIndex","ISCTE_EAS::GetTableDescriptorByIndex","ISCTE_EASGetTableDescriptorByIndex","atscpsipparser/ISCTE_EAS::GetTableDescriptorByIndex","mstv.iscte_eas_gettabledescriptorbyindex"]
old-location: mstv\iscte_eas_gettabledescriptorbyindex.htm
tech.root: mstv
ms.assetid: 24e02875-32ab-4844-bec3-8044b03b9843
ms.date: 12/05/2018
ms.keywords: GetTableDescriptorByIndex, GetTableDescriptorByIndex method [Microsoft TV Technologies], GetTableDescriptorByIndex method [Microsoft TV Technologies],ISCTE_EAS interface, ISCTE_EAS interface [Microsoft TV Technologies],GetTableDescriptorByIndex method, ISCTE_EAS.GetTableDescriptorByIndex, ISCTE_EAS::GetTableDescriptorByIndex, ISCTE_EASGetTableDescriptorByIndex, atscpsipparser/ISCTE_EAS::GetTableDescriptorByIndex, mstv.iscte_eas_gettabledescriptorbyindex
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
 - ISCTE_EAS::GetTableDescriptorByIndex
 - atscpsipparser/ISCTE_EAS::GetTableDescriptorByIndex
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
 - ISCTE_EAS.GetTableDescriptorByIndex
---

# ISCTE_EAS::GetTableDescriptorByIndex


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

The <b>GetTableDescriptorByIndex</b> method returns a descriptor for the EAS table.

## -parameters

### -param dwIndex [in]

The zero-based index of the descriptor to retrieve. Call the <a href="/previous-versions/windows/desktop/api/atscpsipparser/nf-atscpsipparser-iscte_eas-getcountoftabledescriptors">ISCTE_EAS::GetCountOfTableDescriptors</a> method to get the number of table descriptors.

### -param ppDescriptor [out]

Receives a pointer to the <a href="/windows/desktop/api/mpeg2psiparser/nn-mpeg2psiparser-igenericdescriptor">IGenericDescriptor</a> interface. The caller must release the interface.

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