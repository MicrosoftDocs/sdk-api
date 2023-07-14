---
UID: NF:dvbsiparser.IDvbDataBroadcastDescriptor.GetTextLength
title: IDvbDataBroadcastDescriptor::GetTextLength (dvbsiparser.h)
description: Gets length of the text description, in bytes, from a Digital Video Broadcast (DVB) data broadcast descriptor.
helpviewer_keywords: ["GetTextLength","GetTextLength method [Microsoft TV Technologies]","GetTextLength method [Microsoft TV Technologies]","IDvbDataBroadcastDescriptor interface","IDvbDataBroadcastDescriptor interface [Microsoft TV Technologies]","GetTextLength method","IDvbDataBroadcastDescriptor.GetTextLength","IDvbDataBroadcastDescriptor::GetTextLength","dvbsiparser/IDvbDataBroadcastDescriptor::GetTextLength","mstv.idvbdatabroadcastdescriptor_gettextlength"]
old-location: mstv\idvbdatabroadcastdescriptor_gettextlength.htm
tech.root: mstv
ms.assetid: a5ae91ff-d984-4955-aa1c-d166fb491d79
ms.date: 12/05/2018
ms.keywords: GetTextLength, GetTextLength method [Microsoft TV Technologies], GetTextLength method [Microsoft TV Technologies],IDvbDataBroadcastDescriptor interface, IDvbDataBroadcastDescriptor interface [Microsoft TV Technologies],GetTextLength method, IDvbDataBroadcastDescriptor.GetTextLength, IDvbDataBroadcastDescriptor::GetTextLength, dvbsiparser/IDvbDataBroadcastDescriptor::GetTextLength, mstv.idvbdatabroadcastdescriptor_gettextlength
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
 - IDvbDataBroadcastDescriptor::GetTextLength
 - dvbsiparser/IDvbDataBroadcastDescriptor::GetTextLength
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
 - IDvbDataBroadcastDescriptor.GetTextLength
---

# IDvbDataBroadcastDescriptor::GetTextLength


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

Gets length of the text description, in bytes, from a Digital Video Broadcast (DVB)
data broadcast descriptor.

## -parameters

### -param pbVal [out]

Receives the text description length.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/previous-versions/windows/desktop/api/dvbsiparser/nn-dvbsiparser-idvbdatabroadcastdescriptor">IDvbDataBroadcastDescriptor</a>