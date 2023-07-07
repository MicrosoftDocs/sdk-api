---
UID: NF:dvbsiparser.IDvbLogicalChannel2Descriptor.GetCountOfLists
title: IDvbLogicalChannel2Descriptor::GetCountOfLists (dvbsiparser.h)
description: Gets the number of channel lists in a Digital Video Broadcast (DVB) logical channel descriptor.
helpviewer_keywords: ["GetCountOfLists","GetCountOfLists method [Microsoft TV Technologies]","GetCountOfLists method [Microsoft TV Technologies]","IDvbLogicalChannel2Descriptor interface","IDvbLogicalChannel2Descriptor interface [Microsoft TV Technologies]","GetCountOfLists method","IDvbLogicalChannel2Descriptor.GetCountOfLists","IDvbLogicalChannel2Descriptor::GetCountOfLists","dvbsiparser/IDvbLogicalChannel2Descriptor::GetCountOfLists","mstv.idvblogicalchannel2descriptor_getcountoflists"]
old-location: mstv\idvblogicalchannel2descriptor_getcountoflists.htm
tech.root: mstv
ms.assetid: 13a439d1-c6b6-49ab-a41e-caa27e320f37
ms.date: 12/05/2018
ms.keywords: GetCountOfLists, GetCountOfLists method [Microsoft TV Technologies], GetCountOfLists method [Microsoft TV Technologies],IDvbLogicalChannel2Descriptor interface, IDvbLogicalChannel2Descriptor interface [Microsoft TV Technologies],GetCountOfLists method, IDvbLogicalChannel2Descriptor.GetCountOfLists, IDvbLogicalChannel2Descriptor::GetCountOfLists, dvbsiparser/IDvbLogicalChannel2Descriptor::GetCountOfLists, mstv.idvblogicalchannel2descriptor_getcountoflists
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
 - IDvbLogicalChannel2Descriptor::GetCountOfLists
 - dvbsiparser/IDvbLogicalChannel2Descriptor::GetCountOfLists
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
 - IDvbLogicalChannel2Descriptor.GetCountOfLists
---

# IDvbLogicalChannel2Descriptor::GetCountOfLists


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

Gets the number of channel lists in a Digital Video Broadcast (DVB) logical channel descriptor.

## -parameters

### -param pbVal [out]

Receives the number of channel lists.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/previous-versions/windows/desktop/api/dvbsiparser/nn-dvbsiparser-idvblogicalchannel2descriptor">IDvbLogicalChannel2Descriptor</a>