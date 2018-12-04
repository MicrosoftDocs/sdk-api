---
UID: NF:dvbsiparser.IIsdbComponentGroupDescriptor.GetRecordCAUnitCAUnitId
title: IIsdbComponentGroupDescriptor::GetRecordCAUnitCAUnitId
author: windows-sdk-content
description: Gets a conditional access unit identifier from a specified component group record in an Integrated Services Digital Broadcasting (ISDB) component group descriptor.
old-location: mstv\iisdbcomponentgroupdescriptor_getrecordcaunitcaunitid.htm
tech.root: mstv
ms.assetid: 97aa98b7-d676-44ad-be93-e58d996a8a6a
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: GetRecordCAUnitCAUnitId, GetRecordCAUnitCAUnitId method [Microsoft TV Technologies], GetRecordCAUnitCAUnitId method [Microsoft TV Technologies],IIsdbComponentGroupDescriptor interface, IIsdbComponentGroupDescriptor interface [Microsoft TV Technologies],GetRecordCAUnitCAUnitId method, IIsdbComponentGroupDescriptor.GetRecordCAUnitCAUnitId, IIsdbComponentGroupDescriptor::GetRecordCAUnitCAUnitId, dvbsiparser/IIsdbComponentGroupDescriptor::GetRecordCAUnitCAUnitId, mstv.iisdbcomponentgroupdescriptor_getrecordcaunitcaunitid
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
 - IIsdbComponentGroupDescriptor.GetRecordCAUnitCAUnitId
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IIsdbComponentGroupDescriptor::GetRecordCAUnitCAUnitId


## -description


 Gets a conditional access unit identifier from a specified component group record in an Integrated Services Digital Broadcasting (ISDB) component group descriptor. This identifier specifies the type of conditional access unit group to which the component belongs.


## -parameters




### -param bRecordIndex [in]

Specifies the component group record number,
  indexed from zero. Call the <a href="https://msdn.microsoft.com/b5b8334c-a3f1-42f7-81c9-d0c461e17f25">IIsdbComponentGroupDescriptor::GetCountOfRecords</a>method to get the number of records in the descriptor.


### -param bCAUnitIndex [in]

Specifies the conditional access unit record number,
  indexed from zero. Call the <a href="https://msdn.microsoft.com/2656ecfd-84a1-43cb-8fa3-a188f9176c01">IIsdbComponentGroupDescriptor::GetRecordCAUnitNumberOfComponents</a>method to get the number of conditional access  records in the descriptor.


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



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/54ba8ca6-712f-46a1-9ed1-2b20ef8539ba">IIsdbComponentGroupDescriptor</a>



<a href="https://msdn.microsoft.com/b5b8334c-a3f1-42f7-81c9-d0c461e17f25">IIsdbComponentGroupDescriptor::GetCountOfRecords</a>



<a href="https://msdn.microsoft.com/2656ecfd-84a1-43cb-8fa3-a188f9176c01">IIsdbComponentGroupDescriptor::GetRecordCAUnitNumberOfComponents</a>
 

 

