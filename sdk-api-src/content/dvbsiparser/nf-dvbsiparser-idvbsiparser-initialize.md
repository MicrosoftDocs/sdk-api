---
UID: NF:dvbsiparser.IDvbSiParser.Initialize
title: IDvbSiParser::Initialize (dvbsiparser.h)
description: This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005 and later.
helpviewer_keywords: ["IDvbSiParser interface [Microsoft TV Technologies]","Initialize method","IDvbSiParser.Initialize","IDvbSiParser::Initialize","IDvbSiParserInitialize","Initialize","Initialize method [Microsoft TV Technologies]","Initialize method [Microsoft TV Technologies]","IDvbSiParser interface","dvbsiparser/IDvbSiParser::Initialize","mstv.idvbsiparser_initialize"]
old-location: mstv\idvbsiparser_initialize.htm
tech.root: mstv
ms.assetid: 2724f8b4-99bc-477d-bf9e-cc18f56a465b
ms.date: 12/05/2018
ms.keywords: IDvbSiParser interface [Microsoft TV Technologies],Initialize method, IDvbSiParser.Initialize, IDvbSiParser::Initialize, IDvbSiParserInitialize, Initialize, Initialize method [Microsoft TV Technologies], Initialize method [Microsoft TV Technologies],IDvbSiParser interface, dvbsiparser/IDvbSiParser::Initialize, mstv.idvbsiparser_initialize
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IDvbSiParser::Initialize
 - dvbsiparser/IDvbSiParser::Initialize
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - dvbsiparser.h
api_name:
 - IDvbSiParser.Initialize
---

# IDvbSiParser::Initialize


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005 and later.
        



The <b>Initialize</b> method initializes this object.

## -parameters

### -param punkMpeg2Data [in]

Pointer to the <b>IUnknown</b> interface of the <a href="/previous-versions/windows/desktop/mstv/mpeg-2-sections-and-tables-filter">MPEG-2 Sections and Tables Filter</a> or another object that implements the <a href="/previous-versions/windows/desktop/api/mpeg2data/nn-mpeg2data-impeg2data">IMpeg2Data</a> interface.

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
<dt><b>E_NOINTERFACE</b></dt>
</dl>
</td>
<td width="60%">
The <i>punkMpeg2Data</i> pointer does not expose the <b>IMpeg2Data</b> interface.

</td>
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
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The method succeeded.

</td>
</tr>
</table>

## -remarks

Until this method is called, all other methods on this interface fail.

## -see-also

<a href="/previous-versions/windows/desktop/api/dvbsiparser/nn-dvbsiparser-idvbsiparser">IDvbSiParser Interface</a>