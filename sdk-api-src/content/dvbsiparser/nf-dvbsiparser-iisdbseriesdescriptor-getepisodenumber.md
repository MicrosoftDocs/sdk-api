---
UID: NF:dvbsiparser.IIsdbSeriesDescriptor.GetEpisodeNumber
title: IIsdbSeriesDescriptor::GetEpisodeNumber (dvbsiparser.h)
description: Gets the episode number from an Integrated Services Digital Broadcasting (ISDB) series descriptor.
helpviewer_keywords: ["GetEpisodeNumber","GetEpisodeNumber method [Microsoft TV Technologies]","GetEpisodeNumber method [Microsoft TV Technologies]","IIsdbSeriesDescriptor interface","IIsdbSeriesDescriptor interface [Microsoft TV Technologies]","GetEpisodeNumber method","IIsdbSeriesDescriptor.GetEpisodeNumber","IIsdbSeriesDescriptor::GetEpisodeNumber","dvbsiparser/IIsdbSeriesDescriptor::GetEpisodeNumber","mstv.iisdbseriesdescriptor_getepisodenumber"]
old-location: mstv\iisdbseriesdescriptor_getepisodenumber.htm
tech.root: mstv
ms.assetid: 1a28ff17-4a5e-4245-845e-1307830fb3fd
ms.date: 12/05/2018
ms.keywords: GetEpisodeNumber, GetEpisodeNumber method [Microsoft TV Technologies], GetEpisodeNumber method [Microsoft TV Technologies],IIsdbSeriesDescriptor interface, IIsdbSeriesDescriptor interface [Microsoft TV Technologies],GetEpisodeNumber method, IIsdbSeriesDescriptor.GetEpisodeNumber, IIsdbSeriesDescriptor::GetEpisodeNumber, dvbsiparser/IIsdbSeriesDescriptor::GetEpisodeNumber, mstv.iisdbseriesdescriptor_getepisodenumber
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
 - IIsdbSeriesDescriptor::GetEpisodeNumber
 - dvbsiparser/IIsdbSeriesDescriptor::GetEpisodeNumber
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
 - IIsdbSeriesDescriptor.GetEpisodeNumber
---

# IIsdbSeriesDescriptor::GetEpisodeNumber


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

Gets the episode number from an Integrated Services Digital Broadcasting (ISDB) series descriptor.

## -parameters

### -param pwVal [out]

Receives the episode number.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/previous-versions/windows/desktop/api/dvbsiparser/nn-dvbsiparser-iisdbseriesdescriptor">IIsdbSeriesDescriptor</a>