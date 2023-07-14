---
UID: NF:dvbsiparser.IDvbLogicalChannel2Descriptor.GetListRecordServiceId
title: IDvbLogicalChannel2Descriptor::GetListRecordServiceId (dvbsiparser.h)
description: Gets the service identifier from a Digital Video Broadcast (DVB) logical channel descriptor.
helpviewer_keywords: ["GetListRecordServiceId","GetListRecordServiceId method [Microsoft TV Technologies]","GetListRecordServiceId method [Microsoft TV Technologies]","IDvbLogicalChannel2Descriptor interface","IDvbLogicalChannel2Descriptor interface [Microsoft TV Technologies]","GetListRecordServiceId method","IDvbLogicalChannel2Descriptor.GetListRecordServiceId","IDvbLogicalChannel2Descriptor::GetListRecordServiceId","dvbsiparser/IDvbLogicalChannel2Descriptor::GetListRecordServiceId","mstv.idvblogicalchannel2descriptor_getlistrecordserviceid"]
old-location: mstv\idvblogicalchannel2descriptor_getlistrecordserviceid.htm
tech.root: mstv
ms.assetid: ebd81791-558d-4380-af4c-d8380f404771
ms.date: 12/05/2018
ms.keywords: GetListRecordServiceId, GetListRecordServiceId method [Microsoft TV Technologies], GetListRecordServiceId method [Microsoft TV Technologies],IDvbLogicalChannel2Descriptor interface, IDvbLogicalChannel2Descriptor interface [Microsoft TV Technologies],GetListRecordServiceId method, IDvbLogicalChannel2Descriptor.GetListRecordServiceId, IDvbLogicalChannel2Descriptor::GetListRecordServiceId, dvbsiparser/IDvbLogicalChannel2Descriptor::GetListRecordServiceId, mstv.idvblogicalchannel2descriptor_getlistrecordserviceid
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
 - IDvbLogicalChannel2Descriptor::GetListRecordServiceId
 - dvbsiparser/IDvbLogicalChannel2Descriptor::GetListRecordServiceId
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
 - IDvbLogicalChannel2Descriptor.GetListRecordServiceId
---

# IDvbLogicalChannel2Descriptor::GetListRecordServiceId


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

Gets the service identifier from a Digital Video Broadcast (DVB) logical channel descriptor.  getlistcountofrecords

## -parameters

### -param bListIndex [in]

Specifies the channel list record number,
  indexed from zero. Call the <a href="/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-idvblogicalchannel2descriptor-getcountoflists">IDvbLogicalChannel2Descriptor::GetCountOfLists</a> method to get the number of channel list records in the logical channel descriptor.

### -param bRecordIndex [in]

Specifies the service record number,
  indexed from zero. Call the <a href="/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-idvblogicalchannel2descriptor-getlistcountofrecords">IDvbLogicalChannel2Descriptor::GetListCountOfRecords</a> method to get the number of service records in the logical channel descriptor.

### -param pwVal [out]

Receives the service identifier.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/previous-versions/windows/desktop/api/dvbsiparser/nn-dvbsiparser-idvblogicalchannel2descriptor">IDvbLogicalChannel2Descriptor</a>