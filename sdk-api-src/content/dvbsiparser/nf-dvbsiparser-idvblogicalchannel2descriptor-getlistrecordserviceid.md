---
UID: NF:dvbsiparser.IDvbLogicalChannel2Descriptor.GetListRecordServiceId
title: IDvbLogicalChannel2Descriptor::GetListRecordServiceId
author: windows-sdk-content
description: Gets the service identifier from a Digital Video Broadcast (DVB) logical channel descriptor.
old-location: mstv\idvblogicalchannel2descriptor_getlistrecordserviceid.htm
tech.root: MSTV
ms.assetid: ebd81791-558d-4380-af4c-d8380f404771
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: GetListRecordServiceId, GetListRecordServiceId method [Microsoft TV Technologies], GetListRecordServiceId method [Microsoft TV Technologies],IDvbLogicalChannel2Descriptor interface, IDvbLogicalChannel2Descriptor interface [Microsoft TV Technologies],GetListRecordServiceId method, IDvbLogicalChannel2Descriptor.GetListRecordServiceId, IDvbLogicalChannel2Descriptor::GetListRecordServiceId, dvbsiparser/IDvbLogicalChannel2Descriptor::GetListRecordServiceId, mstv.idvblogicalchannel2descriptor_getlistrecordserviceid
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
 - IDvbLogicalChannel2Descriptor.GetListRecordServiceId
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- dvbsiparser.h
: 
- IDvbLogicalChannel2Descriptor.GetListRecordServiceId
: 
---

# IDvbLogicalChannel2Descriptor::GetListRecordServiceId


## -description


Gets the service identifier from a Digital Video Broadcast (DVB) logical channel descriptor.  getlistcountofrecords


## -parameters




### -param bListIndex [in]

Specifies the channel list record number,
  indexed from zero. Call the <a href="https://msdn.microsoft.com/13a439d1-c6b6-49ab-a41e-caa27e320f37">IDvbLogicalChannel2Descriptor::GetCountOfLists</a>method to get the number of channel list records in the logical channel descriptor.


### -param bRecordIndex [in]

Specifies the service record number,
  indexed from zero. Call the <a href="https://msdn.microsoft.com/ca9cac1c-1e4a-4ea2-b44f-d037e9e8197e">IDvbLogicalChannel2Descriptor::GetListCountOfRecords</a>method to get the number of service records in the logical channel descriptor.



### -param pwVal [out]

Receives the service identifier.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/dc60db7f-ae49-48dd-bd8a-62899e5ca7a3">IDvbLogicalChannel2Descriptor</a>
 

 

