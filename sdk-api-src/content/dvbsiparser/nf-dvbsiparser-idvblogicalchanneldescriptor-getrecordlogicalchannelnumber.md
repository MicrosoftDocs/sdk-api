---
UID: NF:dvbsiparser.IDvbLogicalChannelDescriptor.GetRecordLogicalChannelNumber
title: IDvbLogicalChannelDescriptor::GetRecordLogicalChannelNumber (dvbsiparser.h)
description: Note  This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005 and later. .
helpviewer_keywords: ["GetRecordLogicalChannelNumber","GetRecordLogicalChannelNumber method [DirectShow]","GetRecordLogicalChannelNumber method [DirectShow]","IDvbLogicalChannelDescriptor interface","IDvbLogicalChannelDescriptor interface [DirectShow]","GetRecordLogicalChannelNumber method","IDvbLogicalChannelDescriptor.GetRecordLogicalChannelNumber","IDvbLogicalChannelDescriptor::GetRecordLogicalChannelNumber","IDvbLogicalChannelDescriptorGetRecordLogicalChannelNumber","dvbsiparser/IDvbLogicalChannelDescriptor::GetRecordLogicalChannelNumber","mstv.idvblogicalchanneldescriptor_getrecordlogicalchannelnumber"]
old-location: mstv\idvblogicalchanneldescriptor_getrecordlogicalchannelnumber.htm
tech.root: mstv
ms.assetid: fa74587a-ba11-449c-ba0d-bea371e7f019
ms.date: 12/05/2018
ms.keywords: GetRecordLogicalChannelNumber, GetRecordLogicalChannelNumber method [DirectShow], GetRecordLogicalChannelNumber method [DirectShow],IDvbLogicalChannelDescriptor interface, IDvbLogicalChannelDescriptor interface [DirectShow],GetRecordLogicalChannelNumber method, IDvbLogicalChannelDescriptor.GetRecordLogicalChannelNumber, IDvbLogicalChannelDescriptor::GetRecordLogicalChannelNumber, IDvbLogicalChannelDescriptorGetRecordLogicalChannelNumber, dvbsiparser/IDvbLogicalChannelDescriptor::GetRecordLogicalChannelNumber, mstv.idvblogicalchanneldescriptor_getrecordlogicalchannelnumber
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
 - IDvbLogicalChannelDescriptor::GetRecordLogicalChannelNumber
 - dvbsiparser/IDvbLogicalChannelDescriptor::GetRecordLogicalChannelNumber
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
 - IDvbLogicalChannelDescriptor.GetRecordLogicalChannelNumber
---

# IDvbLogicalChannelDescriptor::GetRecordLogicalChannelNumber


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

<div class="alert"><b>Note</b>  This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005 and later.</div>
<div> </div>




The <b>GetRecordLogicalChannelNumber</b> method returns the logical channel number at a specified index in the channel list.

## -parameters

### -param bRecordIndex [in]

Zero-based index of the logical channel number to return. To get the number of logical channel numbers in the descriptor, call <a href="/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-idvblogicalchanneldescriptor-getcountofrecords">IDvbLogicalChannelDescriptor::GetCountOfRecords</a>.

### -param pwVal [out]

Receives the logical_channel_number field.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/previous-versions/windows/desktop/api/dvbsiparser/nn-dvbsiparser-idvblogicalchanneldescriptor">IDvbLogicalChannelDescriptor</a>