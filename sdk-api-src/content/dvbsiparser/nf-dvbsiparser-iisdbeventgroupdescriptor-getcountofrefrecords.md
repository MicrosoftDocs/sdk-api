---
UID: NF:dvbsiparser.IIsdbEventGroupDescriptor.GetCountOfRefRecords
title: IIsdbEventGroupDescriptor::GetCountOfRefRecords (dvbsiparser.h)
description: Gets the number of related event records from an Integrated Services Digital Broadcasting (ISDB) event group descriptor.
helpviewer_keywords: ["GetCountOfRefRecords","GetCountOfRefRecords method [Microsoft TV Technologies]","GetCountOfRefRecords method [Microsoft TV Technologies]","IIsdbEventGroupDescriptor interface","IIsdbEventGroupDescriptor interface [Microsoft TV Technologies]","GetCountOfRefRecords method","IIsdbEventGroupDescriptor.GetCountOfRefRecords","IIsdbEventGroupDescriptor::GetCountOfRefRecords","dvbsiparser/IIsdbEventGroupDescriptor::GetCountOfRefRecords","mstv.iisdbeventgroupdescriptor_getcountofrefrecords"]
old-location: mstv\iisdbeventgroupdescriptor_getcountofrefrecords.htm
tech.root: mstv
ms.assetid: cdc3c99d-516d-4001-a261-2d909b17a1f1
ms.date: 12/05/2018
ms.keywords: GetCountOfRefRecords, GetCountOfRefRecords method [Microsoft TV Technologies], GetCountOfRefRecords method [Microsoft TV Technologies],IIsdbEventGroupDescriptor interface, IIsdbEventGroupDescriptor interface [Microsoft TV Technologies],GetCountOfRefRecords method, IIsdbEventGroupDescriptor.GetCountOfRefRecords, IIsdbEventGroupDescriptor::GetCountOfRefRecords, dvbsiparser/IIsdbEventGroupDescriptor::GetCountOfRefRecords, mstv.iisdbeventgroupdescriptor_getcountofrefrecords
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
 - IIsdbEventGroupDescriptor::GetCountOfRefRecords
 - dvbsiparser/IIsdbEventGroupDescriptor::GetCountOfRefRecords
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
 - IIsdbEventGroupDescriptor.GetCountOfRefRecords
---

# IIsdbEventGroupDescriptor::GetCountOfRefRecords


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

 Gets the number of related event records from an Integrated Services Digital Broadcasting (ISDB) event group descriptor.

## -parameters

### -param pbVal [out]

Receives the number of related event records.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/previous-versions/windows/desktop/api/dvbsiparser/nn-dvbsiparser-iisdbeventgroupdescriptor">IIsdbEventGroupDescriptor</a>