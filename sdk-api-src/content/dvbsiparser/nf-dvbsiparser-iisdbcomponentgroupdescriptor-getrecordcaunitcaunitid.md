---
UID: NF:dvbsiparser.IIsdbComponentGroupDescriptor.GetRecordCAUnitCAUnitId
title: IIsdbComponentGroupDescriptor::GetRecordCAUnitCAUnitId (dvbsiparser.h)
description: Gets a conditional access unit identifier from a specified component group record in an Integrated Services Digital Broadcasting (ISDB) component group descriptor.
helpviewer_keywords: ["GetRecordCAUnitCAUnitId","GetRecordCAUnitCAUnitId method [Microsoft TV Technologies]","GetRecordCAUnitCAUnitId method [Microsoft TV Technologies]","IIsdbComponentGroupDescriptor interface","IIsdbComponentGroupDescriptor interface [Microsoft TV Technologies]","GetRecordCAUnitCAUnitId method","IIsdbComponentGroupDescriptor.GetRecordCAUnitCAUnitId","IIsdbComponentGroupDescriptor::GetRecordCAUnitCAUnitId","dvbsiparser/IIsdbComponentGroupDescriptor::GetRecordCAUnitCAUnitId","mstv.iisdbcomponentgroupdescriptor_getrecordcaunitcaunitid"]
old-location: mstv\iisdbcomponentgroupdescriptor_getrecordcaunitcaunitid.htm
tech.root: mstv
ms.assetid: 97aa98b7-d676-44ad-be93-e58d996a8a6a
ms.date: 12/05/2018
ms.keywords: GetRecordCAUnitCAUnitId, GetRecordCAUnitCAUnitId method [Microsoft TV Technologies], GetRecordCAUnitCAUnitId method [Microsoft TV Technologies],IIsdbComponentGroupDescriptor interface, IIsdbComponentGroupDescriptor interface [Microsoft TV Technologies],GetRecordCAUnitCAUnitId method, IIsdbComponentGroupDescriptor.GetRecordCAUnitCAUnitId, IIsdbComponentGroupDescriptor::GetRecordCAUnitCAUnitId, dvbsiparser/IIsdbComponentGroupDescriptor::GetRecordCAUnitCAUnitId, mstv.iisdbcomponentgroupdescriptor_getrecordcaunitcaunitid
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
 - IIsdbComponentGroupDescriptor::GetRecordCAUnitCAUnitId
 - dvbsiparser/IIsdbComponentGroupDescriptor::GetRecordCAUnitCAUnitId
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
 - IIsdbComponentGroupDescriptor.GetRecordCAUnitCAUnitId
---

# IIsdbComponentGroupDescriptor::GetRecordCAUnitCAUnitId


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

 Gets a conditional access unit identifier from a specified component group record in an Integrated Services Digital Broadcasting (ISDB) component group descriptor. This identifier specifies the type of conditional access unit group to which the component belongs.

## -parameters

### -param bRecordIndex [in]

Specifies the component group record number,
  indexed from zero. Call the <a href="/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-iisdbcomponentgroupdescriptor-getcountofrecords">IIsdbComponentGroupDescriptor::GetCountOfRecords</a> method to get the number of records in the descriptor.

### -param bCAUnitIndex [in]

Specifies the conditional access unit record number,
  indexed from zero. Call the <a href="/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-iisdbcomponentgroupdescriptor-getrecordcaunitnumberofcomponents">IIsdbComponentGroupDescriptor::GetRecordCAUnitNumberOfComponents</a> method to get the number of conditional access  records in the descriptor.

### -param pbVal [out]

Receives the conditional access unit identifier. This can be any of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt>0x0</dt>
</dl>
</td>
<td width="60%">
Non-conditional access unit group.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>0x1</dt>
</dl>
</td>
<td width="60%">
Conditional access unit group that includes the default elementary stream  group.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>0x2-0xF</dt>
</dl>
</td>
<td width="60%">
Conditional access unit group other than that including the default elementary stream group.

</td>
</tr>
</table>

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/previous-versions/windows/desktop/api/dvbsiparser/nn-dvbsiparser-iisdbcomponentgroupdescriptor">IIsdbComponentGroupDescriptor</a>



<a href="/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-iisdbcomponentgroupdescriptor-getcountofrecords">IIsdbComponentGroupDescriptor::GetCountOfRecords</a>



<a href="/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-iisdbcomponentgroupdescriptor-getrecordcaunitnumberofcomponents">IIsdbComponentGroupDescriptor::GetRecordCAUnitNumberOfComponents</a>