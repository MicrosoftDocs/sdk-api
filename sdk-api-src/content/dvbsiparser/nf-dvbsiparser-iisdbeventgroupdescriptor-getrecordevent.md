---
UID: NF:dvbsiparser.IIsdbEventGroupDescriptor.GetRecordEvent
title: IIsdbEventGroupDescriptor::GetRecordEvent (dvbsiparser.h)
description: Gets data from an event record in an Integrated Services Digital Broadcasting (ISDB) event group descriptor.
old-location: mstv\iisdbeventgroupdescriptor_getrecordevent.htm
tech.root: mstv
ms.assetid: 899c8c7f-9e85-4b0d-b7ea-24fb0b5daa88
ms.date: 12/05/2018
ms.keywords: GetRecordEvent, GetRecordEvent method [Microsoft TV Technologies], GetRecordEvent method [Microsoft TV Technologies],IIsdbEventGroupDescriptor interface, IIsdbEventGroupDescriptor interface [Microsoft TV Technologies],GetRecordEvent method, IIsdbEventGroupDescriptor.GetRecordEvent, IIsdbEventGroupDescriptor::GetRecordEvent, dvbsiparser/IIsdbEventGroupDescriptor::GetRecordEvent, mstv.iisdbeventgroupdescriptor_getrecordevent
ms.topic: method
f1_keywords:
- dvbsiparser/IIsdbEventGroupDescriptor.GetRecordEvent
dev_langs:
- c++
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
- IIsdbEventGroupDescriptor.GetRecordEvent
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IIsdbEventGroupDescriptor::GetRecordEvent


## -description


 Gets data from an event record in an Integrated Services Digital Broadcasting (ISDB) event group descriptor.


## -parameters




### -param bRecordIndex [in]

Zero-based index of the event record containing the data. To get the number of components, call <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-iisdbtsinformationdescriptor-getcountofrecords">IIsdbEventGrouptDescriptor::GetCountOfRecords</a>.


### -param pwServiceId [out]

Receives the value of the sevice_id field from the event record. This value identifies the information service and appears in the program_number field of the corresponding program map section. 


### -param pwEventId [out]

Receives the value of  the event_id field from the related event record. This value identifies the event.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/dvbsiparser/nn-dvbsiparser-iisdbeventgroupdescriptor">IIsdbEventGroupDescriptor</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-iisdbtsinformationdescriptor-getcountofrecords">IIsdbEventGrouptDescriptor::GetCountOfRecords</a>
 

 

