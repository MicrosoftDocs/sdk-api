---
UID: NF:dvbsiparser.IDvbMultilingualServiceNameDescriptor.GetRecordServiceNameW
title: IDvbMultilingualServiceNameDescriptor::GetRecordServiceNameW (dvbsiparser.h)
description: Gets the service name in string format from a Digital Video Broadcast (DVB) multilingual service name descriptor.
helpviewer_keywords: ["GetRecordServiceNameW","GetRecordServiceNameW method [Microsoft TV Technologies]","GetRecordServiceNameW method [Microsoft TV Technologies]","IDvbMultilingualServiceNameDescriptor interface","IDvbMultilingualServiceNameDescriptor interface [Microsoft TV Technologies]","GetRecordServiceNameW method","IDvbMultilingualServiceNameDescriptor.GetRecordServiceNameW","IDvbMultilingualServiceNameDescriptor::GetRecordServiceNameW","dvbsiparser/IDvbMultilingualServiceNameDescriptor::GetRecordServiceNameW","mstv.idvbmultilingualservicenamedescriptor_getrecordservicenamew"]
old-location: mstv\idvbmultilingualservicenamedescriptor_getrecordservicenamew.htm
tech.root: mstv
ms.assetid: dfe9040d-18f1-4a35-a4ed-bb3f84ad8dd7
ms.date: 12/05/2018
ms.keywords: GetRecordServiceNameW, GetRecordServiceNameW method [Microsoft TV Technologies], GetRecordServiceNameW method [Microsoft TV Technologies],IDvbMultilingualServiceNameDescriptor interface, IDvbMultilingualServiceNameDescriptor interface [Microsoft TV Technologies],GetRecordServiceNameW method, IDvbMultilingualServiceNameDescriptor.GetRecordServiceNameW, IDvbMultilingualServiceNameDescriptor::GetRecordServiceNameW, dvbsiparser/IDvbMultilingualServiceNameDescriptor::GetRecordServiceNameW, mstv.idvbmultilingualservicenamedescriptor_getrecordservicenamew
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
 - IDvbMultilingualServiceNameDescriptor::GetRecordServiceNameW
 - dvbsiparser/IDvbMultilingualServiceNameDescriptor::GetRecordServiceNameW
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
 - IDvbMultilingualServiceNameDescriptor.GetRecordServiceNameW
---

# IDvbMultilingualServiceNameDescriptor::GetRecordServiceNameW


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

Gets the service name in string format from a Digital Video Broadcast (DVB) multilingual service name descriptor.

## -parameters

### -param bRecordIndex [in]

Specifies the service record number,
  indexed from zero. Call the <a href="/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-idvbmultilingualservicenamedescriptor-getcountofrecords">IDvbMultilingualServiceNameDescriptor::GetCountOfRecords</a> method to get the number of records in the logical channel descriptor.

### -param convMode [in]

Specifies the string conversion mode to use. This parameter can have any of the following values.<ul>
<li><b>STRCONV_MODE_DVB</b></li>
<li><b>STRCONV_MODE_DVB_EMPHASIS</b></li>
<li><b>STRCONV_MODE_DVB_WITHOUT_EMPHASIS</b></li>
<li><b>STRCONV_MODE_ISDB</b></li>
</ul>

### -param pbstrName [out]

Pointer to a buffer that receives the service name string. The caller is responsible for freeing this memory.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/previous-versions/windows/desktop/api/dvbsiparser/nn-dvbsiparser-idvbmultilingualservicenamedescriptor">IDvbMultilingualServiceNameDescriptor</a>



<a href="/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-idvbmultilingualservicenamedescriptor-getcountofrecords">IDvbMultilingualServiceNameDescriptor::GetCountOfRecords</a>