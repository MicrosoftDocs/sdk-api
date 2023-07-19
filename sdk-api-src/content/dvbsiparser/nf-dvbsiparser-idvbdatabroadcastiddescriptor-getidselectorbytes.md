---
UID: NF:dvbsiparser.IDvbDataBroadcastIDDescriptor.GetIDSelectorBytes
title: IDvbDataBroadcastIDDescriptor::GetIDSelectorBytes (dvbsiparser.h)
description: Gets the data from the selector in a Digital Video Broadcast (DVB) data broadcast ID descriptor. The selector is defined by the broadcast standard for the network.
helpviewer_keywords: ["GetIDSelectorBytes","GetIDSelectorBytes method [Microsoft TV Technologies]","GetIDSelectorBytes method [Microsoft TV Technologies]","IDvbDataBroadcastIDDescriptor interface","IDvbDataBroadcastIDDescriptor interface [Microsoft TV Technologies]","GetIDSelectorBytes method","IDvbDataBroadcastIDDescriptor.GetIDSelectorBytes","IDvbDataBroadcastIDDescriptor::GetIDSelectorBytes","dvbsiparser/IDvbDataBroadcastIDDescriptor::GetIDSelectorBytes","mstv.idvbdatabroadcastiddescriptor_getidselectorbytes"]
old-location: mstv\idvbdatabroadcastiddescriptor_getidselectorbytes.htm
tech.root: mstv
ms.assetid: b41614d6-61e4-4548-9c15-63ef100d2ab8
ms.date: 12/05/2018
ms.keywords: GetIDSelectorBytes, GetIDSelectorBytes method [Microsoft TV Technologies], GetIDSelectorBytes method [Microsoft TV Technologies],IDvbDataBroadcastIDDescriptor interface, IDvbDataBroadcastIDDescriptor interface [Microsoft TV Technologies],GetIDSelectorBytes method, IDvbDataBroadcastIDDescriptor.GetIDSelectorBytes, IDvbDataBroadcastIDDescriptor::GetIDSelectorBytes, dvbsiparser/IDvbDataBroadcastIDDescriptor::GetIDSelectorBytes, mstv.idvbdatabroadcastiddescriptor_getidselectorbytes
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
 - IDvbDataBroadcastIDDescriptor::GetIDSelectorBytes
 - dvbsiparser/IDvbDataBroadcastIDDescriptor::GetIDSelectorBytes
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
 - IDvbDataBroadcastIDDescriptor.GetIDSelectorBytes
---

# IDvbDataBroadcastIDDescriptor::GetIDSelectorBytes


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

Gets the data from the selector in a Digital Video Broadcast (DVB) data broadcast ID descriptor. The selector is defined by the broadcast standard for the network.

## -parameters

### -param pbLen [in, out]

Specifies or gets the number of selector bytes for this descriptor.

### -param pbVal [out]

Receives the selector bytes.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/previous-versions/windows/desktop/api/dvbsiparser/nn-dvbsiparser-idvbdatabroadcastiddescriptor">IDvbDataBroadcastIDDescriptor</a>