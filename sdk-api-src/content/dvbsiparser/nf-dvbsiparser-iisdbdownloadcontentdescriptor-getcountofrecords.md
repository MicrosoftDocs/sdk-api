---
UID: NF:dvbsiparser.IIsdbDownloadContentDescriptor.GetCountOfRecords
title: IIsdbDownloadContentDescriptor::GetCountOfRecords (dvbsiparser.h)
description: Gets the body length of an Integrated Services Digital Broadcasting (ISDB) download content descriptor, in bytes.
helpviewer_keywords: ["GetCountOfRecords","GetCountOfRecords method [Microsoft TV Technologies]","GetCountOfRecords method [Microsoft TV Technologies]","IIsdbDownloadContentDescriptor interface","IIsdbDownloadContentDescriptor interface [Microsoft TV Technologies]","GetCountOfRecords method","IIsdbDownloadContentDescriptor.GetCountOfRecords","IIsdbDownloadContentDescriptor::GetCountOfRecords","dvbsiparser/IIsdbDownloadContentDescriptor::GetCountOfRecords","mstv.iisdbdownloadcontentdescriptor_getcountofrecords"]
old-location: mstv\iisdbdownloadcontentdescriptor_getcountofrecords.htm
tech.root: mstv
ms.assetid: d5a0b8e1-bb88-4ef6-ab25-b35b3d39fef0
ms.date: 12/05/2018
ms.keywords: GetCountOfRecords, GetCountOfRecords method [Microsoft TV Technologies], GetCountOfRecords method [Microsoft TV Technologies],IIsdbDownloadContentDescriptor interface, IIsdbDownloadContentDescriptor interface [Microsoft TV Technologies],GetCountOfRecords method, IIsdbDownloadContentDescriptor.GetCountOfRecords, IIsdbDownloadContentDescriptor::GetCountOfRecords, dvbsiparser/IIsdbDownloadContentDescriptor::GetCountOfRecords, mstv.iisdbdownloadcontentdescriptor_getcountofrecords
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
 - IIsdbDownloadContentDescriptor::GetCountOfRecords
 - dvbsiparser/IIsdbDownloadContentDescriptor::GetCountOfRecords
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
 - IIsdbDownloadContentDescriptor.GetCountOfRecords
---

# IIsdbDownloadContentDescriptor::GetCountOfRecords


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

Gets the body length of an Integrated Services Digital Broadcasting (ISDB) download content descriptor, in bytes.

## -parameters

### -param pwVal [out]

Receives the number of records.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/previous-versions/windows/desktop/api/dvbsiparser/nn-dvbsiparser-iisdbdownloadcontentdescriptor">IIsdbDownloadContentDescriptor</a>