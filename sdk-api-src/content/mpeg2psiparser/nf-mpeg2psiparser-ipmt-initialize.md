---
UID: NF:mpeg2psiparser.IPMT.Initialize
title: IPMT::Initialize (mpeg2psiparser.h)
description: The Initialize method initializes the object using captured table section data. This method is called internally by the IAtscPsipParser::GetPMT method, so applications typically should not call it.
helpviewer_keywords: ["IPMT interface [Microsoft TV Technologies]","Initialize method","IPMT.Initialize","IPMT::Initialize","IPMTInitialize","Initialize","Initialize method [Microsoft TV Technologies]","Initialize method [Microsoft TV Technologies]","IPMT interface","mpeg2psiparser/IPMT::Initialize","mstv.ipmt_initialize"]
old-location: mstv\ipmt_initialize.htm
tech.root: mstv
ms.assetid: d9f5e6b0-4317-40cd-9664-e2cc6d1a8833
ms.date: 12/05/2018
ms.keywords: IPMT interface [Microsoft TV Technologies],Initialize method, IPMT.Initialize, IPMT::Initialize, IPMTInitialize, Initialize, Initialize method [Microsoft TV Technologies], Initialize method [Microsoft TV Technologies],IPMT interface, mpeg2psiparser/IPMT::Initialize, mstv.ipmt_initialize
f1_keywords:
- mpeg2psiparser/IPMT.Initialize
dev_langs:
- c++
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
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- Mpeg2PsiParser.h
api_name:
- IPMT.Initialize
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IPMT::Initialize


## -description



The <b>Initialize</b> method initializes the object using captured table section data. This method is called internally by the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/atscpsipparser/nf-atscpsipparser-iatscpsipparser-getpmt">IAtscPsipParser::GetPMT</a> method, so applications typically should not call it.




## -parameters




### -param pSectionList [in]

Pointer to the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/mpeg2data/nn-mpeg2data-isectionlist">ISectionList</a> interface of the <b>SectionList</b> object that contains the section data.


### -param pMPEGData [in]

Pointer to the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/mpeg2data/nn-mpeg2data-impeg2data">IMpeg2Data</a> interface of the MPEG-2 Sections and Tables filter.


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
The object is already initialized.

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




<a href="https://docs.microsoft.com/windows/desktop/api/mpeg2psiparser/nn-mpeg2psiparser-ipmt">IPMT Interface</a>
 

 

