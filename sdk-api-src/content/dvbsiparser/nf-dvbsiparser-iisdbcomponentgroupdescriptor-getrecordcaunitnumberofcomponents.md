---
UID: NF:dvbsiparser.IIsdbComponentGroupDescriptor.GetRecordCAUnitNumberOfComponents
title: IIsdbComponentGroupDescriptor::GetRecordCAUnitNumberOfComponents (dvbsiparser.h)
description: Gets the number of components corresponding to a conditional access unit from an Integrated Services Digital Broadcasting (ISDB) component group descriptor.
helpviewer_keywords: ["GetRecordCAUnitNumberOfComponents","GetRecordCAUnitNumberOfComponents method [Microsoft TV Technologies]","GetRecordCAUnitNumberOfComponents method [Microsoft TV Technologies]","IIsdbComponentGroupDescriptor interface","IIsdbComponentGroupDescriptor interface [Microsoft TV Technologies]","GetRecordCAUnitNumberOfComponents method","IIsdbComponentGroupDescriptor.GetRecordCAUnitNumberOfComponents","IIsdbComponentGroupDescriptor::GetRecordCAUnitNumberOfComponents","dvbsiparser/IIsdbComponentGroupDescriptor::GetRecordCAUnitNumberOfComponents","mstv.iisdbcomponentgroupdescriptor_getrecordcaunitnumberofcomponents"]
old-location: mstv\iisdbcomponentgroupdescriptor_getrecordcaunitnumberofcomponents.htm
tech.root: mstv
ms.assetid: 2656ecfd-84a1-43cb-8fa3-a188f9176c01
ms.date: 12/05/2018
ms.keywords: GetRecordCAUnitNumberOfComponents, GetRecordCAUnitNumberOfComponents method [Microsoft TV Technologies], GetRecordCAUnitNumberOfComponents method [Microsoft TV Technologies],IIsdbComponentGroupDescriptor interface, IIsdbComponentGroupDescriptor interface [Microsoft TV Technologies],GetRecordCAUnitNumberOfComponents method, IIsdbComponentGroupDescriptor.GetRecordCAUnitNumberOfComponents, IIsdbComponentGroupDescriptor::GetRecordCAUnitNumberOfComponents, dvbsiparser/IIsdbComponentGroupDescriptor::GetRecordCAUnitNumberOfComponents, mstv.iisdbcomponentgroupdescriptor_getrecordcaunitnumberofcomponents
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
 - IIsdbComponentGroupDescriptor::GetRecordCAUnitNumberOfComponents
 - dvbsiparser/IIsdbComponentGroupDescriptor::GetRecordCAUnitNumberOfComponents
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
 - IIsdbComponentGroupDescriptor.GetRecordCAUnitNumberOfComponents
---

# IIsdbComponentGroupDescriptor::GetRecordCAUnitNumberOfComponents


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

 Gets the number of components corresponding to a conditional access  unit from an Integrated Services Digital Broadcasting (ISDB) component group descriptor.

## -parameters

### -param bRecordIndex [in]

Specifies the component record number,
  indexed from zero. Call the <a href="/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-iisdbcomponentgroupdescriptor-getcountofrecords">IIsdbComponentGroupDescriptor::GetCountOfRecords</a> method to get the number of component records in the component group descriptor.

### -param bCAUnitIndex [in]

Specifies the conditional access unit record number,
  indexed from zero. Call the <a href="/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-iisdbcomponentgroupdescriptor-getrecordnumberofcaunit">IIsdbComponentGroupDescriptor::GetRecordNumberOfCAUnit</a> method to get the number of conditional access unit records in the component group descriptor.

### -param pbVal [out]

Receives the number of components.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/previous-versions/windows/desktop/api/dvbsiparser/nn-dvbsiparser-iisdbcomponentgroupdescriptor">IIsdbComponentGroupDescriptor</a>



<a href="/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-iisdbcomponentgroupdescriptor-getcountofrecords">IIsdbComponentGroupDescriptor::GetCountOfRecords</a>



<a href="/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-iisdbcomponentgroupdescriptor-getrecordnumberofcaunit">IIsdbComponentGroupDescriptor::GetRecordNumberOfCAUnit</a>