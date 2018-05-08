---
UID: NF:dvbsiparser.IIsdbSIParameterDescriptor.GetTableId
title: IIsdbSIParameterDescriptor::GetTableId
author: windows-driver-content
description: Gets an identifier for a table descriptor in a service information (SI) parameter descriptor.
old-location: mstv\iisdbsiparameterdescriptor_gettableid.htm
old-project: mstv
ms.assetid: 43b19e3d-20b0-4356-9c84-f47006635e2c
ms.author: windowsdriverdev
ms.date: 4/26/2018
ms.keywords: GetTableId, GetTableId method [Microsoft TV Technologies], GetTableId method [Microsoft TV Technologies],IIsdbSIParameterDescriptor interface, IIsdbSIParameterDescriptor interface [Microsoft TV Technologies],GetTableId method, IIsdbSIParameterDescriptor.GetTableId, IIsdbSIParameterDescriptor::GetTableId, dvbsiparser/IIsdbSIParameterDescriptor::GetTableId, mstv.iisdbsiparameterdescriptor_gettableid
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
-	IIsdbSIParameterDescriptor.GetTableId
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Media Format 9 Series or later
---

# IIsdbSIParameterDescriptor::GetTableId


## -description


Gets an identifier for a table descriptor in a service information (SI) parameter descriptor. 


## -parameters




### -param bRecordIndex [in]

Zero-based index of the SI table descriptor. To get the number of table descriptors, call the <a href="https://msdn.microsoft.com/12f7af61-494e-4597-8672-47ea9552be62">IIsdbSIParameterDescriptor::GetRecordNumberOfTable</a> method.


### -param pbVal [out]

Receives the table descriptor identifier.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/264ae78d-cd72-49ff-b99b-2af637cc2917">IIsdbSIParameterDescriptor</a>



<a href="https://msdn.microsoft.com/12f7af61-494e-4597-8672-47ea9552be62">IIsdbSIParameterDescriptor::GetRecordNumberOfTable</a>
 

 

