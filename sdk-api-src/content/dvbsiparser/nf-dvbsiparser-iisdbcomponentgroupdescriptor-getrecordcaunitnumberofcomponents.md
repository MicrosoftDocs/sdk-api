---
UID: NF:dvbsiparser.IIsdbComponentGroupDescriptor.GetRecordCAUnitNumberOfComponents
title: IIsdbComponentGroupDescriptor::GetRecordCAUnitNumberOfComponents method
author: windows-driver-content
description: Gets the number of components corresponding to a conditional access unit from an Integrated Services Digital Broadcasting (ISDB) component group descriptor.
old-location: mstv\iisdbcomponentgroupdescriptor_getrecordcaunitnumberofcomponents.htm
old-project: mstv
ms.assetid: 2656ecfd-84a1-43cb-8fa3-a188f9176c01
ms.author: windowsdriverdev
ms.date: 3/26/2018
ms.keywords: GetRecordCAUnitNumberOfComponents method [Microsoft TV Technologies], GetRecordCAUnitNumberOfComponents method [Microsoft TV Technologies], IIsdbComponentGroupDescriptor interface, GetRecordCAUnitNumberOfComponents,IIsdbComponentGroupDescriptor.GetRecordCAUnitNumberOfComponents, IIsdbComponentGroupDescriptor, IIsdbComponentGroupDescriptor interface [Microsoft TV Technologies], GetRecordCAUnitNumberOfComponents method, IIsdbComponentGroupDescriptor::GetRecordCAUnitNumberOfComponents, dvbsiparser/IIsdbComponentGroupDescriptor::GetRecordCAUnitNumberOfComponents, mstv.iisdbcomponentgroupdescriptor_getrecordcaunitnumberofcomponents
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
-	IIsdbComponentGroupDescriptor.GetRecordCAUnitNumberOfComponents
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Media Format 9 Series or later
---

# IIsdbComponentGroupDescriptor::GetRecordCAUnitNumberOfComponents method


## -description


 Gets the number of components corresponding to a conditional access  unit from an Integrated Services Digital Broadcasting (ISDB) component group descriptor.


## -parameters




### -param bRecordIndex [in]

Specifies the component record number,
  indexed from zero. Call the <a href="https://msdn.microsoft.com/b5b8334c-a3f1-42f7-81c9-d0c461e17f25">IIsdbComponentGroupDescriptor::GetCountOfRecords</a>
  method to get the number of component records in the component group descriptor.


### -param bCAUnitIndex [in]

Specifies the conditional access unit record number,
  indexed from zero. Call the <a href="https://msdn.microsoft.com/239d952f-908d-4aa9-86c0-f58f7616987f">IIsdbComponentGroupDescriptor::GetRecordNumberOfCAUnit</a>
  method to get the number of conditional access unit records in the component group descriptor.


### -param pbVal [out]

Receives the number of components.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/54ba8ca6-712f-46a1-9ed1-2b20ef8539ba">IIsdbComponentGroupDescriptor</a>



<a href="https://msdn.microsoft.com/b5b8334c-a3f1-42f7-81c9-d0c461e17f25">IIsdbComponentGroupDescriptor::GetCountOfRecords</a>



<a href="https://msdn.microsoft.com/239d952f-908d-4aa9-86c0-f58f7616987f">IIsdbComponentGroupDescriptor::GetRecordNumberOfCAUnit</a>
 

 

