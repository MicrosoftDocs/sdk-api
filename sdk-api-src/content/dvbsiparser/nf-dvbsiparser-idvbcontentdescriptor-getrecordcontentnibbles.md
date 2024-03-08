---
UID: NF:dvbsiparser.IDvbContentDescriptor.GetRecordContentNibbles
title: IDvbContentDescriptor::GetRecordContentNibbles (dvbsiparser.h)
description: Gets the two 4-bit fields that make up a DVB-defined identifier for a content descriptor.
helpviewer_keywords: ["GetRecordContentNibbles","GetRecordContentNibbles method [Microsoft TV Technologies]","GetRecordContentNibbles method [Microsoft TV Technologies]","IDvbContentDescriptor interface","IDvbContentDescriptor interface [Microsoft TV Technologies]","GetRecordContentNibbles method","IDvbContentDescriptor.GetRecordContentNibbles","IDvbContentDescriptor::GetRecordContentNibbles","dvbsiparser/IDvbContentDescriptor::GetRecordContentNibbles","mstv.idvbcontentdescriptor_getrecordcontentnibbles"]
old-location: mstv\idvbcontentdescriptor_getrecordcontentnibbles.htm
tech.root: mstv
ms.assetid: 2b05403a-cf9e-4f23-907f-ffb90b6fc5e3
ms.date: 12/05/2018
ms.keywords: GetRecordContentNibbles, GetRecordContentNibbles method [Microsoft TV Technologies], GetRecordContentNibbles method [Microsoft TV Technologies],IDvbContentDescriptor interface, IDvbContentDescriptor interface [Microsoft TV Technologies],GetRecordContentNibbles method, IDvbContentDescriptor.GetRecordContentNibbles, IDvbContentDescriptor::GetRecordContentNibbles, dvbsiparser/IDvbContentDescriptor::GetRecordContentNibbles, mstv.idvbcontentdescriptor_getrecordcontentnibbles
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
 - IDvbContentDescriptor::GetRecordContentNibbles
 - dvbsiparser/IDvbContentDescriptor::GetRecordContentNibbles
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
 - IDvbContentDescriptor.GetRecordContentNibbles
---

# IDvbContentDescriptor::GetRecordContentNibbles


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

Gets the two 4-bit fields that make up a DVB-defined identifier for a content descriptor.

## -parameters

### -param bRecordIndex [in]

Zero-based index of the descriptor to return. To get the number of descriptors, call <a href="/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-idvbcontentdescriptor-getcountofrecords">IDvbContentDescriptor::GetCountOfRecords</a>

### -param pbValLevel1 [out]

Gets the most-significant four bits of the content identifier.

### -param pbValLevel2 [out]

Gets the least-significant four bits of the content identifier.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

For a list of content descriptors associated with the values returned in the <i>dwVal1</i> and <i>dwVal2</i> parameters, see Table 28 in Section 6.2.9 of the DVB standard document titled  
      <i>Digital Video Broadcasting (DVB);
Specification for Service Information (SI) in DVB systems (DVB Document A038 Rev. 4)</i>. (This resource may not be available in some languages 

and countries.)

## -see-also

<a href="/previous-versions/windows/desktop/api/dvbsiparser/nn-dvbsiparser-idvbcontentdescriptor">IDvbContentDescriptor</a>