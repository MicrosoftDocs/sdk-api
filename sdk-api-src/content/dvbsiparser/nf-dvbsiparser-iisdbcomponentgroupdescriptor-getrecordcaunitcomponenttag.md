---
UID: NF:dvbsiparser.IIsdbComponentGroupDescriptor.GetRecordCAUnitComponentTag
title: IIsdbComponentGroupDescriptor::GetRecordCAUnitComponentTag (dvbsiparser.h)
description: Gets the tag that identifies a component record in an Integrated Services Digital Broadcasting (ISDB) component group descriptor.
old-location: mstv\iisdbcomponentgroupdescriptor_getrecordcaunitcomponenttag.htm
tech.root: mstv
ms.assetid: e6588a58-d6df-4f54-ab09-3e938d45f8c4
ms.date: 12/05/2018
ms.keywords: GetRecordCAUnitComponentTag, GetRecordCAUnitComponentTag method [Microsoft TV Technologies], GetRecordCAUnitComponentTag method [Microsoft TV Technologies],IIsdbComponentGroupDescriptor interface, IIsdbComponentGroupDescriptor interface [Microsoft TV Technologies],GetRecordCAUnitComponentTag method, IIsdbComponentGroupDescriptor.GetRecordCAUnitComponentTag, IIsdbComponentGroupDescriptor::GetRecordCAUnitComponentTag, dvbsiparser/IIsdbComponentGroupDescriptor::GetRecordCAUnitComponentTag, mstv.iisdbcomponentgroupdescriptor_getrecordcaunitcomponenttag
f1_keywords:
- dvbsiparser/IIsdbComponentGroupDescriptor.GetRecordCAUnitComponentTag
dev_langs:
- c++
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
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- dvbsiparser.h
api_name:
- IIsdbComponentGroupDescriptor.GetRecordCAUnitComponentTag
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IIsdbComponentGroupDescriptor::GetRecordCAUnitComponentTag


## -description


Gets the tag that identifies a component record in an Integrated Services Digital Broadcasting (ISDB) component group descriptor.


## -parameters




### -param bRecordIndex [in]

Specifies the component record number,
  indexed from zero. Call the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-iisdbcomponentgroupdescriptor-getcountofrecords">IIsdbComponentGroupDescriptor::GetCountOfRecords</a>method to get the number of records in the extended event descriptor.


### -param bCAUnitIndex [in]

Specifies the conditional access unit number within the component group,
  indexed from zero. Call the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-iisdbcomponentgroupdescriptor-getrecordnumberofcaunit">IIsdbComponentGroupDescriptor::GetRecordNumberOfCAUnit</a>method to get the number of records in the extended event descriptor.


### -param bComponentIndex [in]

Specifies the component within the component group,
  indexed from zero. Call the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-iisdbcomponentgroupdescriptor-getrecordcaunitnumberofcomponents">IIsdbComponentGroupDescriptor::GetRecordCAUnitNumberOfComponents</a>method to get the number of components for the conditional access unit given by the <i>bCAUnitIndex</i> parameter.


### -param pbVal [out]

Receives the component tag value.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/dvbsiparser/nn-dvbsiparser-iisdbcomponentgroupdescriptor">IIsdbComponentGroupDescriptor</a>
 

 

