---
UID: NF:dvbsiparser.IIsdbSeriesDescriptor.GetLastEpisodeNumber
title: IIsdbSeriesDescriptor::GetLastEpisodeNumber (dvbsiparser.h)
description: Gets the number of the last episode of a series from an Integrated Services Digital Broadcasting (ISDB) series descriptor.
helpviewer_keywords: ["GetLastEpisodeNumber","GetLastEpisodeNumber method [Microsoft TV Technologies]","GetLastEpisodeNumber method [Microsoft TV Technologies]","IIsdbSeriesDescriptor interface","IIsdbSeriesDescriptor interface [Microsoft TV Technologies]","GetLastEpisodeNumber method","IIsdbSeriesDescriptor.GetLastEpisodeNumber","IIsdbSeriesDescriptor::GetLastEpisodeNumber","dvbsiparser/IIsdbSeriesDescriptor::GetLastEpisodeNumber","mstv.iisdbseriesdescriptor_getlastepisodenumber"]
old-location: mstv\iisdbseriesdescriptor_getlastepisodenumber.htm
tech.root: mstv
ms.assetid: 23cae82f-a40f-47c6-b9ee-0d91a87d9b70
ms.date: 12/05/2018
ms.keywords: GetLastEpisodeNumber, GetLastEpisodeNumber method [Microsoft TV Technologies], GetLastEpisodeNumber method [Microsoft TV Technologies],IIsdbSeriesDescriptor interface, IIsdbSeriesDescriptor interface [Microsoft TV Technologies],GetLastEpisodeNumber method, IIsdbSeriesDescriptor.GetLastEpisodeNumber, IIsdbSeriesDescriptor::GetLastEpisodeNumber, dvbsiparser/IIsdbSeriesDescriptor::GetLastEpisodeNumber, mstv.iisdbseriesdescriptor_getlastepisodenumber
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
 - IIsdbSeriesDescriptor::GetLastEpisodeNumber
 - dvbsiparser/IIsdbSeriesDescriptor::GetLastEpisodeNumber
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
 - IIsdbSeriesDescriptor.GetLastEpisodeNumber
---

# IIsdbSeriesDescriptor::GetLastEpisodeNumber


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

Gets the number of the last episode of a series from an Integrated Services Digital Broadcasting (ISDB) series descriptor.

## -parameters

### -param pwVal [out]

Receives the last episode number.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/previous-versions/windows/desktop/api/dvbsiparser/nn-dvbsiparser-iisdbseriesdescriptor">IIsdbSeriesDescriptor</a>