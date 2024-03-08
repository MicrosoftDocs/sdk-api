---
UID: NF:dvbsiparser.IDvbExtendedEventDescriptor.GetRecordItemW
title: IDvbExtendedEventDescriptor::GetRecordItemW (dvbsiparser.h)
description: Gets the item and descriptor from a Digital Videl Broadcast (DVB) extended event descriptor, in Unicode string format.
helpviewer_keywords: ["GetRecordItemW","GetRecordItemW method [Microsoft TV Technologies]","GetRecordItemW method [Microsoft TV Technologies]","IDvbExtendedEventDescriptor interface","IDvbExtendedEventDescriptor interface [Microsoft TV Technologies]","GetRecordItemW method","IDvbExtendedEventDescriptor.GetRecordItemW","IDvbExtendedEventDescriptor::GetRecordItemW","dvbsiparser/IDvbExtendedEventDescriptor::GetRecordItemW","mstv.idvbextendedeventdescriptor_getrecorditemw"]
old-location: mstv\idvbextendedeventdescriptor_getrecorditemw.htm
tech.root: mstv
ms.assetid: 39c046b0-d357-44c5-9abe-2fb3998b7677
ms.date: 12/05/2018
ms.keywords: GetRecordItemW, GetRecordItemW method [Microsoft TV Technologies], GetRecordItemW method [Microsoft TV Technologies],IDvbExtendedEventDescriptor interface, IDvbExtendedEventDescriptor interface [Microsoft TV Technologies],GetRecordItemW method, IDvbExtendedEventDescriptor.GetRecordItemW, IDvbExtendedEventDescriptor::GetRecordItemW, dvbsiparser/IDvbExtendedEventDescriptor::GetRecordItemW, mstv.idvbextendedeventdescriptor_getrecorditemw
req.header: dvbsiparser.h
req.include-header: Dvbsiparser.idl
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
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
 - IDvbExtendedEventDescriptor::GetRecordItemW
 - dvbsiparser/IDvbExtendedEventDescriptor::GetRecordItemW
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
 - IDvbExtendedEventDescriptor.GetRecordItemW
---

# IDvbExtendedEventDescriptor::GetRecordItemW


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

Gets the item and descriptor from a  Digital Videl Broadcast (DVB) extended event descriptor, in Unicode string format.

## -parameters

### -param bRecordIndex [in]

Specifies the item record number,
  indexed from zero. Call the <a href="/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-idvbextendedeventdescriptor-getcountofrecords">IDvbExtendedEventDescriptor::GetCountOfRecords</a> method to get the number of records in the extended event descriptor.

### -param convMode [in]

Specifies the string conversion mode to use. This parameter can have any of the following values.<ul>
<li><b>STRCONV_MODE_DVB</b></li>
<li><b>STRCONV_MODE_DVB_EMPHASIS</b></li>
<li><b>STRCONV_MODE_DVB_WITHOUT_EMPHASIS</b></li>
<li><b>STRCONV_MODE_ISDB</b></li>
</ul>

### -param pbstrDesc [out]

Pointer to a buffer that receives the item description. The caller is responsible for freeing this memory.

### -param pbstrItem [out]

Pointer to a buffer that receives the item text. The caller is responsible for freeing this memory.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/previous-versions/windows/desktop/api/dvbsiparser/nn-dvbsiparser-idvbextendedeventdescriptor">IDvbExtendedEventDescriptor</a>



<a href="/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-idvbextendedeventdescriptor-getcountofrecords">IDvbExtendedEventDescriptor::GetCountOfRecords</a>