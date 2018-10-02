---
UID: NF:dvbsiparser.IIsdbDataContentDescriptor.GetRecordComponentRef
title: IIsdbDataContentDescriptor::GetRecordComponentRef
author: windows-sdk-content
description: Gets the value of the component_ref field from a specified component record in an Integrated Services Digital Broadcasting (ISDB) data content descriptor. This field contains the broadcaster-defined component tag that identifies a component stream.
old-location: mstv\iisdbdatacontentdescriptor_getrecordcomponentref.htm
tech.root: MSTV
ms.assetid: 3668c323-6808-4bc4-b372-37647ef3fdd8
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: GetRecordComponentRef, GetRecordComponentRef method [Microsoft TV Technologies], GetRecordComponentRef method [Microsoft TV Technologies],IIsdbDataContentDescriptor interface, IIsdbDataContentDescriptor interface [Microsoft TV Technologies],GetRecordComponentRef method, IIsdbDataContentDescriptor.GetRecordComponentRef, IIsdbDataContentDescriptor::GetRecordComponentRef, dvbsiparser/IIsdbDataContentDescriptor::GetRecordComponentRef, mstv.iisdbdatacontentdescriptor_getrecordcomponentref
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
 - IIsdbDataContentDescriptor.GetRecordComponentRef
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IIsdbDataContentDescriptor::GetRecordComponentRef


## -description


 Gets the value of the component_ref field from a specified component record in an Integrated Services Digital Broadcasting (ISDB) data content descriptor. This field contains the broadcaster-defined component tag that identifies a component stream. 


## -parameters




### -param bRecordIndex [in]

Zero-based index of the component record containing the tag. To get the number of components, call <a href="https://msdn.microsoft.com/97e0d307-f41d-44e3-8f42-d00fecbcd61e">IIsdbDataContentDescriptor::GetCountOfRecords</a>.


### -param pbVal [out]

Receives the component tag. 


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/91d55991-5994-4104-9a8f-01cfc347a96f">IIsdbDataContentDescriptor</a>
 

 

