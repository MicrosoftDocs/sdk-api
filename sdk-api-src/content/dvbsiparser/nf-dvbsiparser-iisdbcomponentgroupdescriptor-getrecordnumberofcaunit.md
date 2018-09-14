---
UID: NF:dvbsiparser.IIsdbComponentGroupDescriptor.GetRecordNumberOfCAUnit
title: IIsdbComponentGroupDescriptor::GetRecordNumberOfCAUnit
author: windows-sdk-content
description: Gets the number of conditional access unit records in a component group from an Integrated Services Digital Broadcasting (ISDB) component group descriptor.
old-location: mstv\iisdbcomponentgroupdescriptor_getrecordnumberofcaunit.htm
tech.root: MSTV
ms.assetid: 239d952f-908d-4aa9-86c0-f58f7616987f
ms.author: windowssdkdev
ms.date: 08/30/2018
ms.keywords: GetRecordNumberOfCAUnit, GetRecordNumberOfCAUnit method [Microsoft TV Technologies], GetRecordNumberOfCAUnit method [Microsoft TV Technologies],IIsdbComponentGroupDescriptor interface, IIsdbComponentGroupDescriptor interface [Microsoft TV Technologies],GetRecordNumberOfCAUnit method, IIsdbComponentGroupDescriptor.GetRecordNumberOfCAUnit, IIsdbComponentGroupDescriptor::GetRecordNumberOfCAUnit, dvbsiparser/IIsdbComponentGroupDescriptor::GetRecordNumberOfCAUnit, mstv.iisdbcomponentgroupdescriptor_getrecordnumberofcaunit
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
 - IIsdbComponentGroupDescriptor.GetRecordNumberOfCAUnit
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IIsdbComponentGroupDescriptor::GetRecordNumberOfCAUnit


## -description


Gets the number of conditional access unit records in a component group from an Integrated Services Digital Broadcasting (ISDB) component group descriptor.


## -parameters




### -param bRecordIndex [in]

Specifies the component group record number,
  indexed from zero. Call the <a href="https://msdn.microsoft.com/b5b8334c-a3f1-42f7-81c9-d0c461e17f25">IIsdbComponentGroupDescriptor::GetCountOfRecords</a>method to get the number of records in the extended event descriptor.


### -param pbVal [out]

Receives the number of conditional access unit records.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/54ba8ca6-712f-46a1-9ed1-2b20ef8539ba">IIsdbComponentGroupDescriptor</a>
 

 

