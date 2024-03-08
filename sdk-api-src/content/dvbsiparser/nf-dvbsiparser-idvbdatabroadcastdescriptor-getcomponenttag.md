---
UID: NF:dvbsiparser.IDvbDataBroadcastDescriptor.GetComponentTag
title: IDvbDataBroadcastDescriptor::GetComponentTag (dvbsiparser.h)
description: Gets the component tag from a Digital Video Broadcast (DVB) data broadcast descriptor. The component tag identifies a component stream within the service.
helpviewer_keywords: ["GetComponentTag","GetComponentTag method [Microsoft TV Technologies]","GetComponentTag method [Microsoft TV Technologies]","IDvbDataBroadcastDescriptor interface","IDvbDataBroadcastDescriptor interface [Microsoft TV Technologies]","GetComponentTag method","IDvbDataBroadcastDescriptor.GetComponentTag","IDvbDataBroadcastDescriptor::GetComponentTag","dvbsiparser/IDvbDataBroadcastDescriptor::GetComponentTag","mstv.idvbdatabroadcastdescriptor_getcomponenttag"]
old-location: mstv\idvbdatabroadcastdescriptor_getcomponenttag.htm
tech.root: mstv
ms.assetid: 3b4c93ff-063b-4ebb-bc9a-09ec9cb6d538
ms.date: 12/05/2018
ms.keywords: GetComponentTag, GetComponentTag method [Microsoft TV Technologies], GetComponentTag method [Microsoft TV Technologies],IDvbDataBroadcastDescriptor interface, IDvbDataBroadcastDescriptor interface [Microsoft TV Technologies],GetComponentTag method, IDvbDataBroadcastDescriptor.GetComponentTag, IDvbDataBroadcastDescriptor::GetComponentTag, dvbsiparser/IDvbDataBroadcastDescriptor::GetComponentTag, mstv.idvbdatabroadcastdescriptor_getcomponenttag
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
 - IDvbDataBroadcastDescriptor::GetComponentTag
 - dvbsiparser/IDvbDataBroadcastDescriptor::GetComponentTag
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
 - IDvbDataBroadcastDescriptor.GetComponentTag
---

# IDvbDataBroadcastDescriptor::GetComponentTag


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

Gets the component tag from a Digital Video Broadcast (DVB) data broadcast descriptor.
   The component tag identifies a component stream within the service.

## -parameters

### -param pbVal [out]

Receives the component tag.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/previous-versions/windows/desktop/api/dvbsiparser/nn-dvbsiparser-idvbdatabroadcastdescriptor">IDvbDataBroadcastDescriptor</a>