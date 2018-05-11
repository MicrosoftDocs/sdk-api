---
UID: NF:dvbsiparser.IIsdbComponentGroupDescriptor.GetComponentGroupType
title: IIsdbComponentGroupDescriptor::GetComponentGroupType
author: windows-driver-content
description: Gets the value of the component_group_type field from an Integrated Services Digital Broadcasting (ISDB) component group descriptor. This three-bit field indicates the group type to which the components in the descriptor belong.
old-location: mstv\iisdbcomponentgroupdescriptor_getcomponentgrouptype.htm
old-project: mstv
ms.assetid: 6bf17c29-ee43-4de8-a536-bea44238aa53
ms.author: windowsdriverdev
ms.date: 5/8/2018
ms.keywords: GetComponentGroupType, GetComponentGroupType method [Microsoft TV Technologies], GetComponentGroupType method [Microsoft TV Technologies],IIsdbComponentGroupDescriptor interface, IIsdbComponentGroupDescriptor interface [Microsoft TV Technologies],GetComponentGroupType method, IIsdbComponentGroupDescriptor.GetComponentGroupType, IIsdbComponentGroupDescriptor::GetComponentGroupType, dvbsiparser/IIsdbComponentGroupDescriptor::GetComponentGroupType, mstv.iisdbcomponentgroupdescriptor_getcomponentgrouptype
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
req.typenames: DSROLE_UPGRADE_STATUS_INFO, *PDSROLE_UPGRADE_STATUS_INFO
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	dvbsiparser.h
api_name:
-	IIsdbComponentGroupDescriptor.GetComponentGroupType
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Media Format 9 Series or later
---

# IIsdbComponentGroupDescriptor::GetComponentGroupType


## -description


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



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/6bf17c29-ee43-4de8-a536-bea44238aa53">IIsdbComponentGroupDescriptor</a>
 

 

