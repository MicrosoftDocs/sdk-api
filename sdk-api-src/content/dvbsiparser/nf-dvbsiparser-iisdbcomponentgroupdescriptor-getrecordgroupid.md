---
UID: NF:dvbsiparser.IIsdbComponentGroupDescriptor.GetRecordGroupId
title: IIsdbComponentGroupDescriptor::GetRecordGroupId
author: windows-driver-content
description: Gets the component group identifier from an Integrated Services Digital Broadcasting (ISDB) component group descriptor.
old-location: mstv\iisdbcomponentgroupdescriptor_getrecordgroupid.htm
old-project: mstv
ms.assetid: 159c496c-675e-458a-b9f9-5c9622fd1848
ms.author: windowsdriverdev
ms.date: 5/8/2018
ms.keywords: GetRecordGroupId, GetRecordGroupId method [Microsoft TV Technologies], GetRecordGroupId method [Microsoft TV Technologies],IIsdbComponentGroupDescriptor interface, IIsdbComponentGroupDescriptor interface [Microsoft TV Technologies],GetRecordGroupId method, IIsdbComponentGroupDescriptor.GetRecordGroupId, IIsdbComponentGroupDescriptor::GetRecordGroupId, dvbsiparser/IIsdbComponentGroupDescriptor::GetRecordGroupId, mstv.iisdbcomponentgroupdescriptor_getrecordgroupid
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
req.typenames: DSROLE_UPGRADE_STATUS_INFO, *PDSROLE_UPGRADE_STATUS_INFO
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	dvbsiparser.h
api_name:
-	IIsdbComponentGroupDescriptor.GetRecordGroupId
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Media Format 9 Series or later
---

# IIsdbComponentGroupDescriptor::GetRecordGroupId


## -description


Gets the component group identifier from an Integrated Services Digital Broadcasting (ISDB) component group descriptor.


## -parameters




### -param bRecordIndex [in]

Specifies the component group record number,
  indexed from zero. Call the <a href="https://msdn.microsoft.com/b5b8334c-a3f1-42f7-81c9-d0c461e17f25">IIsdbComponentGroupDescriptor::GetCountOfRecords</a>
  method to get the number of records in the extended event descriptor.


### -param pbVal [out]

Receives the component group record number.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/54ba8ca6-712f-46a1-9ed1-2b20ef8539ba">IIsdbComponentGroupDescriptor</a>
 

 

