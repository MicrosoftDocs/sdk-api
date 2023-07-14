---
UID: NF:dvbsiparser.IDvbTeletextDescriptor.GetLength
title: IDvbTeletextDescriptor::GetLength (dvbsiparser.h)
description: Gets the body length of a Digital Video Broadcast (DVB) teletext descriptor.
helpviewer_keywords: ["GetLength","GetLength method [Microsoft TV Technologies]","GetLength method [Microsoft TV Technologies]","IDvbTeletextDescriptor interface","IDvbTeletextDescriptor interface [Microsoft TV Technologies]","GetLength method","IDvbTeletextDescriptor.GetLength","IDvbTeletextDescriptor::GetLength","dvbsiparser/IDvbTeletextDescriptor::GetLength","mstv.idvbteletextdescriptor_getlength"]
old-location: mstv\idvbteletextdescriptor_getlength.htm
tech.root: mstv
ms.assetid: e785d05a-d4f1-40d8-b93e-ea944373f4c3
ms.date: 12/05/2018
ms.keywords: GetLength, GetLength method [Microsoft TV Technologies], GetLength method [Microsoft TV Technologies],IDvbTeletextDescriptor interface, IDvbTeletextDescriptor interface [Microsoft TV Technologies],GetLength method, IDvbTeletextDescriptor.GetLength, IDvbTeletextDescriptor::GetLength, dvbsiparser/IDvbTeletextDescriptor::GetLength, mstv.idvbteletextdescriptor_getlength
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
 - IDvbTeletextDescriptor::GetLength
 - dvbsiparser/IDvbTeletextDescriptor::GetLength
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
 - IDvbTeletextDescriptor.GetLength
---

# IDvbTeletextDescriptor::GetLength


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

Gets the body length of a Digital Video Broadcast (DVB) teletext descriptor.

## -parameters

### -param pbVal [out]

Receives the length of the teletext descriptor, in bytes.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/previous-versions/windows/desktop/api/dvbsiparser/nn-dvbsiparser-idvbteletextdescriptor">IDvbTeletextDescriptor</a>