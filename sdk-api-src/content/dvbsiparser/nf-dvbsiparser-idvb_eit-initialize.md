---
UID: NF:dvbsiparser.IDVB_EIT.Initialize
title: IDVB_EIT::Initialize (dvbsiparser.h)
description: This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005 and later.helpviewer_keywords: ["IDVB_EIT interface [Microsoft TV Technologies]","Initialize method","IDVB_EIT.Initialize","IDVB_EIT::Initialize","IDVB_EITInitialize","Initialize","Initialize method [Microsoft TV Technologies]","Initialize method [Microsoft TV Technologies]","IDVB_EIT interface","dvbsiparser/IDVB_EIT::Initialize","mstv.idvb_eit_initialize"]
old-location: mstv\idvb_eit_initialize.htm
tech.root: mstv
ms.assetid: a0ffa39a-9e91-4229-8dee-b31f3973f384
ms.date: 12/05/2018
ms.keywords: IDVB_EIT interface [Microsoft TV Technologies],Initialize method, IDVB_EIT.Initialize, IDVB_EIT::Initialize, IDVB_EITInitialize, Initialize, Initialize method [Microsoft TV Technologies], Initialize method [Microsoft TV Technologies],IDVB_EIT interface, dvbsiparser/IDVB_EIT::Initialize, mstv.idvb_eit_initialize
f1_keywords:
- dvbsiparser/IDVB_EIT.Initialize
dev_langs:
- c++
req.header: dvbsiparser.h
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
- dvbsiparser.h
api_name:
- IDVB_EIT.Initialize
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IDVB_EIT::Initialize


## -description



This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005 and later.
        



The <b>Initialize</b> method initializes the object using captured table section data. This method is called internally by the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-idvbsiparser-geteit">IDvbSiParser::GetEIT</a> method, so applications typically should not call it.


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




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/dvbsiparser/nn-dvbsiparser-idvb_eit">IDVB_EIT Interface</a>
 

 

