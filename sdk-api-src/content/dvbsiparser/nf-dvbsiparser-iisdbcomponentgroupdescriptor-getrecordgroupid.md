---
UID: NF:dvbsiparser.IIsdbComponentGroupDescriptor.GetRecordGroupId
title: IIsdbComponentGroupDescriptor::GetRecordGroupId (dvbsiparser.h)
description: Gets the component group identifier from an Integrated Services Digital Broadcasting (ISDB) component group descriptor.
helpviewer_keywords: ["GetRecordGroupId","GetRecordGroupId method [Microsoft TV Technologies]","GetRecordGroupId method [Microsoft TV Technologies]","IIsdbComponentGroupDescriptor interface","IIsdbComponentGroupDescriptor interface [Microsoft TV Technologies]","GetRecordGroupId method","IIsdbComponentGroupDescriptor.GetRecordGroupId","IIsdbComponentGroupDescriptor::GetRecordGroupId","dvbsiparser/IIsdbComponentGroupDescriptor::GetRecordGroupId","mstv.iisdbcomponentgroupdescriptor_getrecordgroupid"]
old-location: mstv\iisdbcomponentgroupdescriptor_getrecordgroupid.htm
tech.root: mstv
ms.assetid: 159c496c-675e-458a-b9f9-5c9622fd1848
ms.date: 12/05/2018
ms.keywords: GetRecordGroupId, GetRecordGroupId method [Microsoft TV Technologies], GetRecordGroupId method [Microsoft TV Technologies],IIsdbComponentGroupDescriptor interface, IIsdbComponentGroupDescriptor interface [Microsoft TV Technologies],GetRecordGroupId method, IIsdbComponentGroupDescriptor.GetRecordGroupId, IIsdbComponentGroupDescriptor::GetRecordGroupId, dvbsiparser/IIsdbComponentGroupDescriptor::GetRecordGroupId, mstv.iisdbcomponentgroupdescriptor_getrecordgroupid
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
 - IIsdbComponentGroupDescriptor::GetRecordGroupId
 - dvbsiparser/IIsdbComponentGroupDescriptor::GetRecordGroupId
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
 - IIsdbComponentGroupDescriptor.GetRecordGroupId
---

# IIsdbComponentGroupDescriptor::GetRecordGroupId


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

Gets the component group identifier from an Integrated Services Digital Broadcasting (ISDB) component group descriptor.

## -parameters

### -param bRecordIndex [in]

Specifies the component group record number,
  indexed from zero. Call the <a href="/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-iisdbcomponentgroupdescriptor-getcountofrecords">IIsdbComponentGroupDescriptor::GetCountOfRecords</a> method to get the number of records in the extended event descriptor.

### -param pbVal [out]

Receives the component group record number.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/previous-versions/windows/desktop/api/dvbsiparser/nn-dvbsiparser-iisdbcomponentgroupdescriptor">IIsdbComponentGroupDescriptor</a>