---
UID: NF:dvbsiparser.IDvbDataBroadcastIDDescriptor.GetTag
title: IDvbDataBroadcastIDDescriptor::GetTag (dvbsiparser.h)
description: Gets the tag that identifies a Digital Video Broadcast (DVB) data broadcast ID descriptor.
helpviewer_keywords: ["GetTag","GetTag method [Microsoft TV Technologies]","GetTag method [Microsoft TV Technologies]","IDvbDataBroadcastIDDescriptor interface","IDvbDataBroadcastIDDescriptor interface [Microsoft TV Technologies]","GetTag method","IDvbDataBroadcastIDDescriptor.GetTag","IDvbDataBroadcastIDDescriptor::GetTag","dvbsiparser/IDvbDataBroadcastIDDescriptor::GetTag","mstv.idvbdatabroadcastiddescriptor_gettag"]
old-location: mstv\idvbdatabroadcastiddescriptor_gettag.htm
tech.root: mstv
ms.assetid: 7c3c13f0-03b0-47fe-bd87-5bb6d32ef838
ms.date: 12/05/2018
ms.keywords: GetTag, GetTag method [Microsoft TV Technologies], GetTag method [Microsoft TV Technologies],IDvbDataBroadcastIDDescriptor interface, IDvbDataBroadcastIDDescriptor interface [Microsoft TV Technologies],GetTag method, IDvbDataBroadcastIDDescriptor.GetTag, IDvbDataBroadcastIDDescriptor::GetTag, dvbsiparser/IDvbDataBroadcastIDDescriptor::GetTag, mstv.idvbdatabroadcastiddescriptor_gettag
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IDvbDataBroadcastIDDescriptor::GetTag
 - dvbsiparser/IDvbDataBroadcastIDDescriptor::GetTag
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
 - IDvbDataBroadcastIDDescriptor.GetTag
---

# IDvbDataBroadcastIDDescriptor::GetTag


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

Gets the tag that identifies a Digital Video Broadcast (DVB) data broadcast ID descriptor.

## -parameters

### -param pbVal [out]

Receives the descriptor tag. For data broadcast ID descriptors, this value is 0x66.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/previous-versions/windows/desktop/api/dvbsiparser/nn-dvbsiparser-idvbdatabroadcastiddescriptor">IDvbDataBroadcastIDDescriptor</a>