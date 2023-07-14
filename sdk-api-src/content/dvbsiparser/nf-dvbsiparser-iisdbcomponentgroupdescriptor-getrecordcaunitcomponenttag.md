---
UID: NF:dvbsiparser.IIsdbComponentGroupDescriptor.GetRecordCAUnitComponentTag
title: IIsdbComponentGroupDescriptor::GetRecordCAUnitComponentTag (dvbsiparser.h)
description: Gets the tag that identifies a component record in an Integrated Services Digital Broadcasting (ISDB) component group descriptor.
helpviewer_keywords: ["GetRecordCAUnitComponentTag","GetRecordCAUnitComponentTag method [Microsoft TV Technologies]","GetRecordCAUnitComponentTag method [Microsoft TV Technologies]","IIsdbComponentGroupDescriptor interface","IIsdbComponentGroupDescriptor interface [Microsoft TV Technologies]","GetRecordCAUnitComponentTag method","IIsdbComponentGroupDescriptor.GetRecordCAUnitComponentTag","IIsdbComponentGroupDescriptor::GetRecordCAUnitComponentTag","dvbsiparser/IIsdbComponentGroupDescriptor::GetRecordCAUnitComponentTag","mstv.iisdbcomponentgroupdescriptor_getrecordcaunitcomponenttag"]
old-location: mstv\iisdbcomponentgroupdescriptor_getrecordcaunitcomponenttag.htm
tech.root: mstv
ms.assetid: e6588a58-d6df-4f54-ab09-3e938d45f8c4
ms.date: 12/05/2018
ms.keywords: GetRecordCAUnitComponentTag, GetRecordCAUnitComponentTag method [Microsoft TV Technologies], GetRecordCAUnitComponentTag method [Microsoft TV Technologies],IIsdbComponentGroupDescriptor interface, IIsdbComponentGroupDescriptor interface [Microsoft TV Technologies],GetRecordCAUnitComponentTag method, IIsdbComponentGroupDescriptor.GetRecordCAUnitComponentTag, IIsdbComponentGroupDescriptor::GetRecordCAUnitComponentTag, dvbsiparser/IIsdbComponentGroupDescriptor::GetRecordCAUnitComponentTag, mstv.iisdbcomponentgroupdescriptor_getrecordcaunitcomponenttag
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
 - IIsdbComponentGroupDescriptor::GetRecordCAUnitComponentTag
 - dvbsiparser/IIsdbComponentGroupDescriptor::GetRecordCAUnitComponentTag
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
 - IIsdbComponentGroupDescriptor.GetRecordCAUnitComponentTag
---

# IIsdbComponentGroupDescriptor::GetRecordCAUnitComponentTag


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

Gets the tag that identifies a component record in an Integrated Services Digital Broadcasting (ISDB) component group descriptor.

## -parameters

### -param bRecordIndex [in]

Specifies the component record number,
  indexed from zero. Call the <a href="/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-iisdbcomponentgroupdescriptor-getcountofrecords">IIsdbComponentGroupDescriptor::GetCountOfRecords</a> method to get the number of records in the extended event descriptor.

### -param bCAUnitIndex [in]

Specifies the conditional access unit number within the component group,
  indexed from zero. Call the <a href="/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-iisdbcomponentgroupdescriptor-getrecordnumberofcaunit">IIsdbComponentGroupDescriptor::GetRecordNumberOfCAUnit</a> method to get the number of records in the extended event descriptor.

### -param bComponentIndex [in]

Specifies the component within the component group,
  indexed from zero. Call the <a href="/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-iisdbcomponentgroupdescriptor-getrecordcaunitnumberofcomponents">IIsdbComponentGroupDescriptor::GetRecordCAUnitNumberOfComponents</a> method to get the number of components for the conditional access unit given by the <i>bCAUnitIndex</i> parameter.

### -param pbVal [out]

Receives the component tag value.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/previous-versions/windows/desktop/api/dvbsiparser/nn-dvbsiparser-iisdbcomponentgroupdescriptor">IIsdbComponentGroupDescriptor</a>