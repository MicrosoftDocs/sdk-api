---
UID: NF:dvbsiparser.IIsdbDownloadContentDescriptor.GetRecordModuleId
title: IIsdbDownloadContentDescriptor::GetRecordModuleId (dvbsiparser.h)
description: Gets the identifier from an Integrated Services Digital Broadcasting (ISDB) download content descriptor that specifies the carousel used for downloading.
helpviewer_keywords: ["GetRecordModuleId","GetRecordModuleId method [Microsoft TV Technologies]","GetRecordModuleId method [Microsoft TV Technologies]","IIsdbDownloadContentDescriptor interface","IIsdbDownloadContentDescriptor interface [Microsoft TV Technologies]","GetRecordModuleId method","IIsdbDownloadContentDescriptor.GetRecordModuleId","IIsdbDownloadContentDescriptor::GetRecordModuleId","dvbsiparser/IIsdbDownloadContentDescriptor::GetRecordModuleId","mstv.iisdbdownloadcontentdescriptor_getrecordmoduleid"]
old-location: mstv\iisdbdownloadcontentdescriptor_getrecordmoduleid.htm
tech.root: mstv
ms.assetid: c714b2f2-e787-40cc-b57b-d56b54dc8966
ms.date: 12/05/2018
ms.keywords: GetRecordModuleId, GetRecordModuleId method [Microsoft TV Technologies], GetRecordModuleId method [Microsoft TV Technologies],IIsdbDownloadContentDescriptor interface, IIsdbDownloadContentDescriptor interface [Microsoft TV Technologies],GetRecordModuleId method, IIsdbDownloadContentDescriptor.GetRecordModuleId, IIsdbDownloadContentDescriptor::GetRecordModuleId, dvbsiparser/IIsdbDownloadContentDescriptor::GetRecordModuleId, mstv.iisdbdownloadcontentdescriptor_getrecordmoduleid
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
 - IIsdbDownloadContentDescriptor::GetRecordModuleId
 - dvbsiparser/IIsdbDownloadContentDescriptor::GetRecordModuleId
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
 - IIsdbDownloadContentDescriptor.GetRecordModuleId
---

# IIsdbDownloadContentDescriptor::GetRecordModuleId


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

 Gets the identifier from an Integrated Services Digital Broadcasting (ISDB) download content descriptor that specifies the carousel used for downloading.

## -parameters

### -param wRecordIndex [in]

Specifies the module record number,
  indexed from zero. Call the <a href="/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-iisdbdownloadcontentdescriptor-getcountofrecords">IIsdbDownloadContentDescriptor::GetCountOfRecords</a> method to get the number of records in the extended event descriptor.

### -param pwVal [out]

Receives the module ID.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/previous-versions/windows/desktop/api/dvbsiparser/nn-dvbsiparser-iisdbdownloadcontentdescriptor">IIsdbDownloadContentDescriptor</a>



<a href="/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-iisdbdownloadcontentdescriptor-getcountofrecords">IIsdbDownloadContentDescriptor::GetCountOfRecords</a>