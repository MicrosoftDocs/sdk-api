---
UID: NF:dvbsiparser.IIsdbDataContentDescriptor.GetCountOfRecords
title: IIsdbDataContentDescriptor::GetCountOfRecords (dvbsiparser.h)
description: Gets the number of records in an Integrated Services Digital Broadcasting (ISDB) data content descriptor.
helpviewer_keywords: ["GetCountOfRecords","GetCountOfRecords method [Microsoft TV Technologies]","GetCountOfRecords method [Microsoft TV Technologies]","IIsdbDataContentDescriptor interface","IIsdbDataContentDescriptor interface [Microsoft TV Technologies]","GetCountOfRecords method","IIsdbDataContentDescriptor.GetCountOfRecords","IIsdbDataContentDescriptor::GetCountOfRecords","dvbsiparser/IIsdbDataContentDescriptor::GetCountOfRecords","mstv.iisdbdatacontentdescriptor_getcountofrecords"]
old-location: mstv\iisdbdatacontentdescriptor_getcountofrecords.htm
tech.root: mstv
ms.assetid: 4198ec3c-f2a3-4517-8efb-81dfb9f8c01d
ms.date: 12/05/2018
ms.keywords: GetCountOfRecords, GetCountOfRecords method [Microsoft TV Technologies], GetCountOfRecords method [Microsoft TV Technologies],IIsdbDataContentDescriptor interface, IIsdbDataContentDescriptor interface [Microsoft TV Technologies],GetCountOfRecords method, IIsdbDataContentDescriptor.GetCountOfRecords, IIsdbDataContentDescriptor::GetCountOfRecords, dvbsiparser/IIsdbDataContentDescriptor::GetCountOfRecords, mstv.iisdbdatacontentdescriptor_getcountofrecords
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
 - IIsdbDataContentDescriptor::GetCountOfRecords
 - dvbsiparser/IIsdbDataContentDescriptor::GetCountOfRecords
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
 - IIsdbDataContentDescriptor.GetCountOfRecords
---

# IIsdbDataContentDescriptor::GetCountOfRecords


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

Gets the number of records in an Integrated Services Digital Broadcasting (ISDB) data content descriptor.

## -parameters

### -param pbVal [out]

Receives the number of records.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/previous-versions/windows/desktop/api/dvbsiparser/nn-dvbsiparser-iisdbdatacontentdescriptor">IIsdbDataContentDescriptor</a>