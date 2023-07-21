---
UID: NF:dvbsiparser.IDvbSubtitlingDescriptor.GetTag
title: IDvbSubtitlingDescriptor::GetTag (dvbsiparser.h)
description: Gets the tag for a Digital Video Broadcast (DVB) subtitling descriptor.
helpviewer_keywords: ["GetTag","GetTag method [Microsoft TV Technologies]","GetTag method [Microsoft TV Technologies]","IDvbSubtitlingDescriptor interface","IDvbSubtitlingDescriptor interface [Microsoft TV Technologies]","GetTag method","IDvbSubtitlingDescriptor.GetTag","IDvbSubtitlingDescriptor::GetTag","dvbsiparser/IDvbSubtitlingDescriptor::GetTag","mstv.idvbsubtitlingdescriptor_gettag"]
old-location: mstv\idvbsubtitlingdescriptor_gettag.htm
tech.root: mstv
ms.assetid: 2b16b66d-5e71-4204-984d-e9a9d677f4a9
ms.date: 12/05/2018
ms.keywords: GetTag, GetTag method [Microsoft TV Technologies], GetTag method [Microsoft TV Technologies],IDvbSubtitlingDescriptor interface, IDvbSubtitlingDescriptor interface [Microsoft TV Technologies],GetTag method, IDvbSubtitlingDescriptor.GetTag, IDvbSubtitlingDescriptor::GetTag, dvbsiparser/IDvbSubtitlingDescriptor::GetTag, mstv.idvbsubtitlingdescriptor_gettag
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
 - IDvbSubtitlingDescriptor::GetTag
 - dvbsiparser/IDvbSubtitlingDescriptor::GetTag
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
 - IDvbSubtitlingDescriptor.GetTag
---

# IDvbSubtitlingDescriptor::GetTag


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

Gets the tag for a Digital Video Broadcast (DVB) subtitling descriptor.

## -parameters

### -param pbVal [out]

Receives the subtitling descriptor tag. For subtitling descriptors, this tag value is "0x59".

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/previous-versions/windows/desktop/api/dvbsiparser/nn-dvbsiparser-idvbsubtitlingdescriptor">IDvbSubtitlingDescriptor</a>