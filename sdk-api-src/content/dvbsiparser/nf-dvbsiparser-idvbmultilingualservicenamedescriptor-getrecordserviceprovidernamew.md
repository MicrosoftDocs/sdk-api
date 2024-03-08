---
UID: NF:dvbsiparser.IDvbMultilingualServiceNameDescriptor.GetRecordServiceProviderNameW
title: IDvbMultilingualServiceNameDescriptor::GetRecordServiceProviderNameW (dvbsiparser.h)
description: Gets the service provider name in string format from a Digital Video Broadcast (DVB) multilingual service name descriptor.
helpviewer_keywords: ["GetRecordServiceProviderNameW","GetRecordServiceProviderNameW method [Microsoft TV Technologies]","GetRecordServiceProviderNameW method [Microsoft TV Technologies]","IDvbMultilingualServiceNameDescriptor interface","IDvbMultilingualServiceNameDescriptor interface [Microsoft TV Technologies]","GetRecordServiceProviderNameW method","IDvbMultilingualServiceNameDescriptor.GetRecordServiceProviderNameW","IDvbMultilingualServiceNameDescriptor::GetRecordServiceProviderNameW","dvbsiparser/IDvbMultilingualServiceNameDescriptor::GetRecordServiceProviderNameW","mstv.idvbmultilingualservicenamedescriptor_getrecordserviceprovidernamew"]
old-location: mstv\idvbmultilingualservicenamedescriptor_getrecordserviceprovidernamew.htm
tech.root: mstv
ms.assetid: e07ebe5c-b5b3-4604-91c3-3e75042ad074
ms.date: 12/05/2018
ms.keywords: GetRecordServiceProviderNameW, GetRecordServiceProviderNameW method [Microsoft TV Technologies], GetRecordServiceProviderNameW method [Microsoft TV Technologies],IDvbMultilingualServiceNameDescriptor interface, IDvbMultilingualServiceNameDescriptor interface [Microsoft TV Technologies],GetRecordServiceProviderNameW method, IDvbMultilingualServiceNameDescriptor.GetRecordServiceProviderNameW, IDvbMultilingualServiceNameDescriptor::GetRecordServiceProviderNameW, dvbsiparser/IDvbMultilingualServiceNameDescriptor::GetRecordServiceProviderNameW, mstv.idvbmultilingualservicenamedescriptor_getrecordserviceprovidernamew
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
 - IDvbMultilingualServiceNameDescriptor::GetRecordServiceProviderNameW
 - dvbsiparser/IDvbMultilingualServiceNameDescriptor::GetRecordServiceProviderNameW
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
 - IDvbMultilingualServiceNameDescriptor.GetRecordServiceProviderNameW
---

# IDvbMultilingualServiceNameDescriptor::GetRecordServiceProviderNameW


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

Gets the service provider name in string format from a Digital Video Broadcast (DVB) multilingual service name descriptor.

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

Pointer to a memory block that receives the service provider name string. The caller is responsible for freeing this memory.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/previous-versions/windows/desktop/api/dvbsiparser/nn-dvbsiparser-idvbmultilingualservicenamedescriptor">IDvbMultilingualServiceNameDescriptor</a>



<a href="/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-idvbmultilingualservicenamedescriptor-getcountofrecords">IDvbMultilingualServiceNameDescriptor::GetCountOfRecords</a>