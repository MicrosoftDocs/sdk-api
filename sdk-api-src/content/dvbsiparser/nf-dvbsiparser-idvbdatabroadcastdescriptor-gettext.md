---
UID: NF:dvbsiparser.IDvbDataBroadcastDescriptor.GetText
title: IDvbDataBroadcastDescriptor::GetText (dvbsiparser.h)
description: Gets the text that describes the data from a Digital Video Broadcast (DVB) data broadcast descriptor.
helpviewer_keywords: ["GetText","GetText method [Microsoft TV Technologies]","GetText method [Microsoft TV Technologies]","IDvbDataBroadcastDescriptor interface","IDvbDataBroadcastDescriptor interface [Microsoft TV Technologies]","GetText method","IDvbDataBroadcastDescriptor.GetText","IDvbDataBroadcastDescriptor::GetText","dvbsiparser/IDvbDataBroadcastDescriptor::GetText","mstv.idvbdatabroadcastdescriptor_gettext"]
old-location: mstv\idvbdatabroadcastdescriptor_gettext.htm
tech.root: mstv
ms.assetid: 3b25a5fa-5829-4c7f-8858-59fdddccdc65
ms.date: 12/05/2018
ms.keywords: GetText, GetText method [Microsoft TV Technologies], GetText method [Microsoft TV Technologies],IDvbDataBroadcastDescriptor interface, IDvbDataBroadcastDescriptor interface [Microsoft TV Technologies],GetText method, IDvbDataBroadcastDescriptor.GetText, IDvbDataBroadcastDescriptor::GetText, dvbsiparser/IDvbDataBroadcastDescriptor::GetText, mstv.idvbdatabroadcastdescriptor_gettext
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
 - IDvbDataBroadcastDescriptor::GetText
 - dvbsiparser/IDvbDataBroadcastDescriptor::GetText
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
 - IDvbDataBroadcastDescriptor.GetText
---

# IDvbDataBroadcastDescriptor::GetText


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

Gets the text that describes the data 
from a Digital Video Broadcast (DVB) data broadcast descriptor.

## -parameters

### -param pbLen [in, out]

Specifies or receives the length of the
description, in bytes.

### -param pbVal [out]

Receives the description text.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/previous-versions/windows/desktop/api/dvbsiparser/nn-dvbsiparser-idvbdatabroadcastdescriptor">IDvbDataBroadcastDescriptor</a>