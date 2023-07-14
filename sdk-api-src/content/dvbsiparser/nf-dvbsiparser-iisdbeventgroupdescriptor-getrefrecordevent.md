---
UID: NF:dvbsiparser.IIsdbEventGroupDescriptor.GetRefRecordEvent
title: IIsdbEventGroupDescriptor::GetRefRecordEvent (dvbsiparser.h)
description: Gets data from a related event record in an Integrated Services Digital Broadcasting (ISDB) event group descriptor.
helpviewer_keywords: ["GetRefRecordEvent","GetRefRecordEvent method [Microsoft TV Technologies]","GetRefRecordEvent method [Microsoft TV Technologies]","IIsdbEventGroupDescriptor interface","IIsdbEventGroupDescriptor interface [Microsoft TV Technologies]","GetRefRecordEvent method","IIsdbEventGroupDescriptor.GetRefRecordEvent","IIsdbEventGroupDescriptor::GetRefRecordEvent","dvbsiparser/IIsdbEventGroupDescriptor::GetRefRecordEvent","mstv.iisdbeventgroupdescriptor_getrefrecordevent"]
old-location: mstv\iisdbeventgroupdescriptor_getrefrecordevent.htm
tech.root: mstv
ms.assetid: fede6a0e-5ac1-472e-aaa8-9d31737a8a1d
ms.date: 12/05/2018
ms.keywords: GetRefRecordEvent, GetRefRecordEvent method [Microsoft TV Technologies], GetRefRecordEvent method [Microsoft TV Technologies],IIsdbEventGroupDescriptor interface, IIsdbEventGroupDescriptor interface [Microsoft TV Technologies],GetRefRecordEvent method, IIsdbEventGroupDescriptor.GetRefRecordEvent, IIsdbEventGroupDescriptor::GetRefRecordEvent, dvbsiparser/IIsdbEventGroupDescriptor::GetRefRecordEvent, mstv.iisdbeventgroupdescriptor_getrefrecordevent
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
 - IIsdbEventGroupDescriptor::GetRefRecordEvent
 - dvbsiparser/IIsdbEventGroupDescriptor::GetRefRecordEvent
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
 - IIsdbEventGroupDescriptor.GetRefRecordEvent
---

# IIsdbEventGroupDescriptor::GetRefRecordEvent


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

Gets data from a related event record in an Integrated Services Digital Broadcasting (ISDB) event group descriptor. The descriptor contains records for related events if the group_type field of the descriptor has a value of 4 or 5. If this  field has a value of 4, it indicates an event relay to other networks. If this field has a value of 5, it indicates an event movement from other networks.

## -parameters

### -param bRecordIndex [in]

Zero-based index of the related event record containing the data. To get the number of components, call <a href="/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-iisdbtsinformationdescriptor-getcountofrecords">IIsdbEventGrouptDescriptor::GetCountOfRecords</a>.

### -param pwOriginalNetworkId [out]

Receives the value of the original_network_id field from the related
event record. This value is transmitted at the time of event relay or event move across networks.

### -param pwTransportStreamId [out]

Receives the value of the transport_stream_id field from the related
event record. This value that is transmitted at the time of event relay or event move across networks.

### -param pwServiceId [out]

Receives the value of the sevice_id field from the related event record. This value identifies the related information service and appears in the program_number field of the corresponding program map section.

### -param pwEventId [out]

Receives the value of  the event_id field from the related event record. This value identifies the related event.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/previous-versions/windows/desktop/api/dvbsiparser/nn-dvbsiparser-iisdbeventgroupdescriptor">IIsdbEventGroupDescriptor</a>



<a href="/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-iisdbtsinformationdescriptor-getcountofrecords">IIsdbEventGrouptDescriptor::GetCountOfRecords</a>