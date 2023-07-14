---
UID: NF:dvbsiparser.IDvbMultilingualServiceNameDescriptor.GetRecordLangId
title: IDvbMultilingualServiceNameDescriptor::GetRecordLangId (dvbsiparser.h)
description: Gets the three-character ISO 639 language code from a Digital Video Broadcast (DVB) multilingual service name descriptor. The language code identifies the language used for text in the descriptor.
helpviewer_keywords: ["GetRecordLangId","GetRecordLangId method [Microsoft TV Technologies]","GetRecordLangId method [Microsoft TV Technologies]","IDvbMultilingualServiceNameDescriptor interface","IDvbMultilingualServiceNameDescriptor interface [Microsoft TV Technologies]","GetRecordLangId method","IDvbMultilingualServiceNameDescriptor.GetRecordLangId","IDvbMultilingualServiceNameDescriptor::GetRecordLangId","dvbsiparser/IDvbMultilingualServiceNameDescriptor::GetRecordLangId","mstv.idvbmultilingualservicenamedescriptor_getrecordlangid"]
old-location: mstv\idvbmultilingualservicenamedescriptor_getrecordlangid.htm
tech.root: mstv
ms.assetid: a8432acb-f59b-4995-8b5d-576acab0f6b1
ms.date: 12/05/2018
ms.keywords: GetRecordLangId, GetRecordLangId method [Microsoft TV Technologies], GetRecordLangId method [Microsoft TV Technologies],IDvbMultilingualServiceNameDescriptor interface, IDvbMultilingualServiceNameDescriptor interface [Microsoft TV Technologies],GetRecordLangId method, IDvbMultilingualServiceNameDescriptor.GetRecordLangId, IDvbMultilingualServiceNameDescriptor::GetRecordLangId, dvbsiparser/IDvbMultilingualServiceNameDescriptor::GetRecordLangId, mstv.idvbmultilingualservicenamedescriptor_getrecordlangid
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
 - IDvbMultilingualServiceNameDescriptor::GetRecordLangId
 - dvbsiparser/IDvbMultilingualServiceNameDescriptor::GetRecordLangId
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
 - IDvbMultilingualServiceNameDescriptor.GetRecordLangId
---

# IDvbMultilingualServiceNameDescriptor::GetRecordLangId


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

Gets the three-character ISO 639 language code from a Digital Video Broadcast (DVB) multilingual service name descriptor. The language code
identifies the language used for text in the descriptor.

## -parameters

### -param bRecordIndex [in]

Specifies the service record number,
  indexed from zero. Call the <a href="/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-idvbmultilingualservicenamedescriptor-getcountofrecords">IDvbMultilingualServiceNameDescriptor::GetCountOfRecords</a> method to get the number of records in the multilingual service name descriptor.

### -param ulVal [out]

Pointer to a buffer that receives the language code. For a list of language codes, refer to <a href="http://www.sil.org/ISO639-3/codes.asp">this document</a>.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/previous-versions/windows/desktop/api/dvbsiparser/nn-dvbsiparser-idvbmultilingualservicenamedescriptor">IDvbMultilingualServiceNameDescriptor</a>



<a href="/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-idvbmultilingualservicenamedescriptor-getcountofrecords">IDvbMultilingualServiceNameDescriptor::GetCountOfRecords</a>