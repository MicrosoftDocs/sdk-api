---
UID: NF:atscpsipparser.ISCTE_EAS.Initialize
title: ISCTE_EAS::Initialize (atscpsipparser.h)
description: The Initialize method initializes the object using captured table section data. This method is called internally by the IAtscPsipParser::GetEAS method, so applications typically should not call it.
helpviewer_keywords: ["ISCTE_EAS interface [Microsoft TV Technologies]","Initialize method","ISCTE_EAS.Initialize","ISCTE_EAS::Initialize","ISCTE_EASInitialize","Initialize","Initialize method [Microsoft TV Technologies]","Initialize method [Microsoft TV Technologies]","ISCTE_EAS interface","atscpsipparser/ISCTE_EAS::Initialize","mstv.iscte_eas_initialize"]
old-location: mstv\iscte_eas_initialize.htm
tech.root: mstv
ms.assetid: f40e89f4-6a33-44a9-933c-bf38978f1cb2
ms.date: 12/05/2018
ms.keywords: ISCTE_EAS interface [Microsoft TV Technologies],Initialize method, ISCTE_EAS.Initialize, ISCTE_EAS::Initialize, ISCTE_EASInitialize, Initialize, Initialize method [Microsoft TV Technologies], Initialize method [Microsoft TV Technologies],ISCTE_EAS interface, atscpsipparser/ISCTE_EAS::Initialize, mstv.iscte_eas_initialize
f1_keywords:
- atscpsipparser/ISCTE_EAS.Initialize
dev_langs:
- c++
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
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- atscpsipparser.h
api_name:
- ISCTE_EAS.Initialize
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ISCTE_EAS::Initialize


## -description


The <b>Initialize</b> method initializes the object using captured table section data. This method is called internally by the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/atscpsipparser/nf-atscpsipparser-iatscpsipparser-geteas">IAtscPsipParser::GetEAS</a> method, so applications typically should not call it.


## -parameters




### -param pSectionList [in]

Pointer to the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/mpeg2data/nn-mpeg2data-isectionlist">ISectionList</a> interface.


### -param pMPEGData [in]

Pointer to the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/mpeg2data/nn-mpeg2data-impeg2data">IMpeg2Data</a> interface of the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/mstv/mpeg-2-sections-and-tables-filter">MPEG-2 Sections and Tables</a> filter.


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
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
Insufficient memory.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MPEG2_E_MALFORMED_TABLE</b></dt>
</dl>
</td>
<td width="60%">
The EAS table is not well formed.

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




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/atscpsipparser/nn-atscpsipparser-iscte_eas">ISCTE_EAS Interface</a>
 

 

