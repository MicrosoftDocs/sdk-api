---
UID: NF:dvbsiparser.IIsdbComponentGroupDescriptor.GetCountOfRecords
title: IIsdbComponentGroupDescriptor::GetCountOfRecords (dvbsiparser.h)
description: Gets the number of component records in an Integrated Services Digital Broadcasting (ISDB) component group descriptor.
helpviewer_keywords: ["GetCountOfRecords","GetCountOfRecords method [Microsoft TV Technologies]","GetCountOfRecords method [Microsoft TV Technologies]","IIsdbComponentGroupDescriptor interface","IIsdbComponentGroupDescriptor interface [Microsoft TV Technologies]","GetCountOfRecords method","IIsdbComponentGroupDescriptor.GetCountOfRecords","IIsdbComponentGroupDescriptor::GetCountOfRecords","dvbsiparser/IIsdbComponentGroupDescriptor::GetCountOfRecords","mstv.iisdbcomponentgroupdescriptor_getcountofrecords"]
old-location: mstv\iisdbcomponentgroupdescriptor_getcountofrecords.htm
tech.root: mstv
ms.assetid: b5b8334c-a3f1-42f7-81c9-d0c461e17f25
ms.date: 12/05/2018
ms.keywords: GetCountOfRecords, GetCountOfRecords method [Microsoft TV Technologies], GetCountOfRecords method [Microsoft TV Technologies],IIsdbComponentGroupDescriptor interface, IIsdbComponentGroupDescriptor interface [Microsoft TV Technologies],GetCountOfRecords method, IIsdbComponentGroupDescriptor.GetCountOfRecords, IIsdbComponentGroupDescriptor::GetCountOfRecords, dvbsiparser/IIsdbComponentGroupDescriptor::GetCountOfRecords, mstv.iisdbcomponentgroupdescriptor_getcountofrecords
req.header: dvbsiparser.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: None supported
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Dvbsiparser.idl
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
 - IIsdbComponentGroupDescriptor::GetCountOfRecords
 - dvbsiparser/IIsdbComponentGroupDescriptor::GetCountOfRecords
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
 - IIsdbComponentGroupDescriptor.GetCountOfRecords
---

# IIsdbComponentGroupDescriptor::GetCountOfRecords


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

 Gets the number of component records in an Integrated Services Digital Broadcasting (ISDB) component group descriptor.

## -parameters

### -param pbVal [out]

Receives the number of records.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-iisdbcomponentgroupdescriptor-getcountofrecords">IIsdbComponentGroupDescriptor</a>