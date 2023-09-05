---
UID: NF:dvbsiparser.IIsdbComponentGroupDescriptor.GetComponentGroupType
title: IIsdbComponentGroupDescriptor::GetComponentGroupType (dvbsiparser.h)
description: Gets the value of the component_group_type field from an Integrated Services Digital Broadcasting (ISDB) component group descriptor. This three-bit field indicates the group type to which the components in the descriptor belong.
helpviewer_keywords: ["GetComponentGroupType","GetComponentGroupType method [Microsoft TV Technologies]","GetComponentGroupType method [Microsoft TV Technologies]","IIsdbComponentGroupDescriptor interface","IIsdbComponentGroupDescriptor interface [Microsoft TV Technologies]","GetComponentGroupType method","IIsdbComponentGroupDescriptor.GetComponentGroupType","IIsdbComponentGroupDescriptor::GetComponentGroupType","dvbsiparser/IIsdbComponentGroupDescriptor::GetComponentGroupType","mstv.iisdbcomponentgroupdescriptor_getcomponentgrouptype"]
old-location: mstv\iisdbcomponentgroupdescriptor_getcomponentgrouptype.htm
tech.root: mstv
ms.assetid: 6bf17c29-ee43-4de8-a536-bea44238aa53
ms.date: 12/05/2018
ms.keywords: GetComponentGroupType, GetComponentGroupType method [Microsoft TV Technologies], GetComponentGroupType method [Microsoft TV Technologies],IIsdbComponentGroupDescriptor interface, IIsdbComponentGroupDescriptor interface [Microsoft TV Technologies],GetComponentGroupType method, IIsdbComponentGroupDescriptor.GetComponentGroupType, IIsdbComponentGroupDescriptor::GetComponentGroupType, dvbsiparser/IIsdbComponentGroupDescriptor::GetComponentGroupType, mstv.iisdbcomponentgroupdescriptor_getcomponentgrouptype
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
 - IIsdbComponentGroupDescriptor::GetComponentGroupType
 - dvbsiparser/IIsdbComponentGroupDescriptor::GetComponentGroupType
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
 - IIsdbComponentGroupDescriptor.GetComponentGroupType
---

# IIsdbComponentGroupDescriptor::GetComponentGroupType


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

Gets the value of the component_group_type field from   an Integrated Services Digital Broadcasting (ISDB) component group descriptor. This three-bit field indicates the group type to which the components in the descriptor belong.

## -parameters

### -param pbVal [out]

Receives the group type. This can have any of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt>000</dt>
</dl>
</td>
<td width="60%">
Multiview television service.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>001-111</dt>
</dl>
</td>
<td width="60%">
Undefined.

</td>
</tr>
</table>

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-iisdbcomponentgroupdescriptor-getcomponentgrouptype">IIsdbComponentGroupDescriptor</a>