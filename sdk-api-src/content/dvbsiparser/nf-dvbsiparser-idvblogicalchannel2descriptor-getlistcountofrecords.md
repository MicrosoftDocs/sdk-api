---
UID: NF:dvbsiparser.IDvbLogicalChannel2Descriptor.GetListCountOfRecords
title: IDvbLogicalChannel2Descriptor::GetListCountOfRecords (dvbsiparser.h)
description: Gets an indexed count of records for a channel list in a Digital Video Broadcast (DVB) logical channel descriptor.
helpviewer_keywords: ["GetListCountOfRecords","GetListCountOfRecords method [Microsoft TV Technologies]","GetListCountOfRecords method [Microsoft TV Technologies]","IDvbLogicalChannel2Descriptor interface","IDvbLogicalChannel2Descriptor interface [Microsoft TV Technologies]","GetListCountOfRecords method","IDvbLogicalChannel2Descriptor.GetListCountOfRecords","IDvbLogicalChannel2Descriptor::GetListCountOfRecords","dvbsiparser/IDvbLogicalChannel2Descriptor::GetListCountOfRecords","mstv.idvblogicalchannel2descriptor_getlistcountofrecords"]
old-location: mstv\idvblogicalchannel2descriptor_getlistcountofrecords.htm
tech.root: mstv
ms.assetid: ca9cac1c-1e4a-4ea2-b44f-d037e9e8197e
ms.date: 12/05/2018
ms.keywords: GetListCountOfRecords, GetListCountOfRecords method [Microsoft TV Technologies], GetListCountOfRecords method [Microsoft TV Technologies],IDvbLogicalChannel2Descriptor interface, IDvbLogicalChannel2Descriptor interface [Microsoft TV Technologies],GetListCountOfRecords method, IDvbLogicalChannel2Descriptor.GetListCountOfRecords, IDvbLogicalChannel2Descriptor::GetListCountOfRecords, dvbsiparser/IDvbLogicalChannel2Descriptor::GetListCountOfRecords, mstv.idvblogicalchannel2descriptor_getlistcountofrecords
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
 - IDvbLogicalChannel2Descriptor::GetListCountOfRecords
 - dvbsiparser/IDvbLogicalChannel2Descriptor::GetListCountOfRecords
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
 - IDvbLogicalChannel2Descriptor.GetListCountOfRecords
---

# IDvbLogicalChannel2Descriptor::GetListCountOfRecords


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

Gets an indexed count of records for a channel list in a Digital Video Broadcast (DVB) logical channel descriptor.

## -parameters

### -param bChannelListIndex [in]

Specifies the channel list number,
  indexed from zero. Call the <a href="/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-idvblogicalchanneldescriptor-getcountofrecords">IDvbLogicalChannel2Descriptor::GetCountOfLists</a> method to get the number of channel lists in the logical channel descriptor.

### -param pbVal [out]

Receives the number of channels in the list.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/previous-versions/windows/desktop/api/dvbsiparser/nn-dvbsiparser-idvblogicalchannel2descriptor">IDvbLogicalChannel2Descriptor</a>



<a href="/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-idvblogicalchanneldescriptor-getcountofrecords">IDvbLogicalChannel2Descriptor::GetCountOfLists</a>