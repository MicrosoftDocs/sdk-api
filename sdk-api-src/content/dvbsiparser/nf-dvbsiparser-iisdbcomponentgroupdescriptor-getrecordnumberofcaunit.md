---
UID: NF:dvbsiparser.IIsdbComponentGroupDescriptor.GetRecordNumberOfCAUnit
title: IIsdbComponentGroupDescriptor::GetRecordNumberOfCAUnit (dvbsiparser.h)
description: Gets the number of conditional access unit records in a component group from an Integrated Services Digital Broadcasting (ISDB) component group descriptor.
helpviewer_keywords: ["GetRecordNumberOfCAUnit","GetRecordNumberOfCAUnit method [Microsoft TV Technologies]","GetRecordNumberOfCAUnit method [Microsoft TV Technologies]","IIsdbComponentGroupDescriptor interface","IIsdbComponentGroupDescriptor interface [Microsoft TV Technologies]","GetRecordNumberOfCAUnit method","IIsdbComponentGroupDescriptor.GetRecordNumberOfCAUnit","IIsdbComponentGroupDescriptor::GetRecordNumberOfCAUnit","dvbsiparser/IIsdbComponentGroupDescriptor::GetRecordNumberOfCAUnit","mstv.iisdbcomponentgroupdescriptor_getrecordnumberofcaunit"]
old-location: mstv\iisdbcomponentgroupdescriptor_getrecordnumberofcaunit.htm
tech.root: mstv
ms.assetid: 239d952f-908d-4aa9-86c0-f58f7616987f
ms.date: 12/05/2018
ms.keywords: GetRecordNumberOfCAUnit, GetRecordNumberOfCAUnit method [Microsoft TV Technologies], GetRecordNumberOfCAUnit method [Microsoft TV Technologies],IIsdbComponentGroupDescriptor interface, IIsdbComponentGroupDescriptor interface [Microsoft TV Technologies],GetRecordNumberOfCAUnit method, IIsdbComponentGroupDescriptor.GetRecordNumberOfCAUnit, IIsdbComponentGroupDescriptor::GetRecordNumberOfCAUnit, dvbsiparser/IIsdbComponentGroupDescriptor::GetRecordNumberOfCAUnit, mstv.iisdbcomponentgroupdescriptor_getrecordnumberofcaunit
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
 - IIsdbComponentGroupDescriptor::GetRecordNumberOfCAUnit
 - dvbsiparser/IIsdbComponentGroupDescriptor::GetRecordNumberOfCAUnit
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
 - IIsdbComponentGroupDescriptor.GetRecordNumberOfCAUnit
---

# IIsdbComponentGroupDescriptor::GetRecordNumberOfCAUnit


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

Gets the number of conditional access unit records in a component group from an Integrated Services Digital Broadcasting (ISDB) component group descriptor.

## -parameters

### -param bRecordIndex [in]

Specifies the component group record number,
  indexed from zero. Call the <a href="/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-iisdbcomponentgroupdescriptor-getcountofrecords">IIsdbComponentGroupDescriptor::GetCountOfRecords</a> method to get the number of records in the extended event descriptor.

### -param pbVal [out]

Receives the number of conditional access unit records.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/previous-versions/windows/desktop/api/dvbsiparser/nn-dvbsiparser-iisdbcomponentgroupdescriptor">IIsdbComponentGroupDescriptor</a>