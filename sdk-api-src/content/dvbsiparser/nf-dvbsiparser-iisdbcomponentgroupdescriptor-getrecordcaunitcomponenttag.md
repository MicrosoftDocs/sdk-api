---
UID: NF:dvbsiparser.IIsdbComponentGroupDescriptor.GetRecordCAUnitComponentTag
title: IIsdbComponentGroupDescriptor::GetRecordCAUnitComponentTag
author: windows-driver-content
description: Gets the tag that identifies a component record in an Integrated Services Digital Broadcasting (ISDB) component group descriptor.
old-location: mstv\iisdbcomponentgroupdescriptor_getrecordcaunitcomponenttag.htm
old-project: mstv
ms.assetid: e6588a58-d6df-4f54-ab09-3e938d45f8c4
ms.author: windowsdriverdev
ms.date: 5/8/2018
ms.keywords: GetRecordCAUnitComponentTag, GetRecordCAUnitComponentTag method [Microsoft TV Technologies], GetRecordCAUnitComponentTag method [Microsoft TV Technologies],IIsdbComponentGroupDescriptor interface, IIsdbComponentGroupDescriptor interface [Microsoft TV Technologies],GetRecordCAUnitComponentTag method, IIsdbComponentGroupDescriptor.GetRecordCAUnitComponentTag, IIsdbComponentGroupDescriptor::GetRecordCAUnitComponentTag, dvbsiparser/IIsdbComponentGroupDescriptor::GetRecordCAUnitComponentTag, mstv.iisdbcomponentgroupdescriptor_getrecordcaunitcomponenttag
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
-	IIsdbComponentGroupDescriptor.GetRecordCAUnitComponentTag
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Media Format 9 Series or later
---

# IIsdbComponentGroupDescriptor::GetRecordCAUnitComponentTag


## -description


Gets the tag that identifies a component record in an Integrated Services Digital Broadcasting (ISDB) component group descriptor.


## -parameters




### -param bRecordIndex [in]

Specifies the component record number,
  indexed from zero. Call the <a href="https://msdn.microsoft.com/b5b8334c-a3f1-42f7-81c9-d0c461e17f25">IIsdbComponentGroupDescriptor::GetCountOfRecords</a>
  method to get the number of records in the extended event descriptor.


### -param bCAUnitIndex [in]

Specifies the conditional access unit number within the component group,
  indexed from zero. Call the <a href="https://msdn.microsoft.com/239d952f-908d-4aa9-86c0-f58f7616987f">IIsdbComponentGroupDescriptor::GetRecordNumberOfCAUnit</a>
  method to get the number of records in the extended event descriptor.


### -param bComponentIndex [in]

Specifies the component within the component group,
  indexed from zero. Call the <a href="https://msdn.microsoft.com/2656ecfd-84a1-43cb-8fa3-a188f9176c01">IIsdbComponentGroupDescriptor::GetRecordCAUnitNumberOfComponents</a>
  method to get the number of components for the conditional access unit given by the <i>bCAUnitIndex</i> parameter.


### -param pbVal [out]

Receives the component tag value.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/54ba8ca6-712f-46a1-9ed1-2b20ef8539ba">IIsdbComponentGroupDescriptor</a>
 

 

