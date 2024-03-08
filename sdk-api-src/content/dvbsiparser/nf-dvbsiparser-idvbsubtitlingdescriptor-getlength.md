---
UID: NF:dvbsiparser.IDvbSubtitlingDescriptor.GetLength
title: IDvbSubtitlingDescriptor::GetLength (dvbsiparser.h)
description: Gets the body length of a Digital Video Broadcast (DVB) subtitling descriptor.
helpviewer_keywords: ["GetLength","GetLength method [Microsoft TV Technologies]","GetLength method [Microsoft TV Technologies]","IDvbSubtitlingDescriptor interface","IDvbSubtitlingDescriptor interface [Microsoft TV Technologies]","GetLength method","IDvbSubtitlingDescriptor.GetLength","IDvbSubtitlingDescriptor::GetLength","dvbsiparser/IDvbSubtitlingDescriptor::GetLength","mstv.idvbsubtitlingdescriptor_getlength"]
old-location: mstv\idvbsubtitlingdescriptor_getlength.htm
tech.root: mstv
ms.assetid: 1b02c37c-4411-4d69-af5d-d758b18fe42c
ms.date: 12/05/2018
ms.keywords: GetLength, GetLength method [Microsoft TV Technologies], GetLength method [Microsoft TV Technologies],IDvbSubtitlingDescriptor interface, IDvbSubtitlingDescriptor interface [Microsoft TV Technologies],GetLength method, IDvbSubtitlingDescriptor.GetLength, IDvbSubtitlingDescriptor::GetLength, dvbsiparser/IDvbSubtitlingDescriptor::GetLength, mstv.idvbsubtitlingdescriptor_getlength
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
 - IDvbSubtitlingDescriptor::GetLength
 - dvbsiparser/IDvbSubtitlingDescriptor::GetLength
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
 - IDvbSubtitlingDescriptor.GetLength
---

# IDvbSubtitlingDescriptor::GetLength


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

Gets the body length of a Digital Video Broadcast (DVB) subtitling descriptor.

## -parameters

### -param pbVal [out]

Receives the number of bytes in the descriptor.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/previous-versions/windows/desktop/api/dvbsiparser/nn-dvbsiparser-idvbsubtitlingdescriptor">IDvbSubtitlingDescriptor</a>