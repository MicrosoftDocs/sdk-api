---
UID: NF:dvbsiparser.IIsdbEventGroupDescriptor.GetCountOfRecords
title: IIsdbEventGroupDescriptor::GetCountOfRecords (dvbsiparser.h)
description: Gets the number of event records from an Integrated Services Digital Broadcasting (ISDB) event group descriptor.
helpviewer_keywords: ["GetCountOfRecords","GetCountOfRecords method [Microsoft TV Technologies]","GetCountOfRecords method [Microsoft TV Technologies]","IIsdbEventGroupDescriptor interface","IIsdbEventGroupDescriptor interface [Microsoft TV Technologies]","GetCountOfRecords method","IIsdbEventGroupDescriptor.GetCountOfRecords","IIsdbEventGroupDescriptor::GetCountOfRecords","dvbsiparser/IIsdbEventGroupDescriptor::GetCountOfRecords","mstv.iisdbeventgroupdescriptor_getcountofrecords"]
old-location: mstv\iisdbeventgroupdescriptor_getcountofrecords.htm
tech.root: mstv
ms.assetid: a254840c-c6bd-4245-a0fc-b0b0b63e637a
ms.date: 12/05/2018
ms.keywords: GetCountOfRecords, GetCountOfRecords method [Microsoft TV Technologies], GetCountOfRecords method [Microsoft TV Technologies],IIsdbEventGroupDescriptor interface, IIsdbEventGroupDescriptor interface [Microsoft TV Technologies],GetCountOfRecords method, IIsdbEventGroupDescriptor.GetCountOfRecords, IIsdbEventGroupDescriptor::GetCountOfRecords, dvbsiparser/IIsdbEventGroupDescriptor::GetCountOfRecords, mstv.iisdbeventgroupdescriptor_getcountofrecords
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
 - IIsdbEventGroupDescriptor::GetCountOfRecords
 - dvbsiparser/IIsdbEventGroupDescriptor::GetCountOfRecords
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
 - IIsdbEventGroupDescriptor.GetCountOfRecords
---

# IIsdbEventGroupDescriptor::GetCountOfRecords


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

Gets the number of event records from an Integrated Services Digital Broadcasting (ISDB) event group descriptor.

## -parameters

### -param pbVal [out]

Receives the number of records.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/previous-versions/windows/desktop/api/dvbsiparser/nn-dvbsiparser-iisdbeventgroupdescriptor">IIsdbEventGroupDescriptor</a>