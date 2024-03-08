---
UID: NF:dvbsiparser.IIsdbSeriesDescriptor.GetSeriesId
title: IIsdbSeriesDescriptor::GetSeriesId (dvbsiparser.h)
description: Gets a unique series identifier from an Integrated Services Digital Broadcasting (ISDB) series descriptor.
helpviewer_keywords: ["GetSeriesId","GetSeriesId method [Microsoft TV Technologies]","GetSeriesId method [Microsoft TV Technologies]","IIsdbSeriesDescriptor interface","IIsdbSeriesDescriptor interface [Microsoft TV Technologies]","GetSeriesId method","IIsdbSeriesDescriptor.GetSeriesId","IIsdbSeriesDescriptor::GetSeriesId","dvbsiparser/IIsdbSeriesDescriptor::GetSeriesId","mstv.iisdbseriesdescriptor_getseriesid"]
old-location: mstv\iisdbseriesdescriptor_getseriesid.htm
tech.root: mstv
ms.assetid: 90de5108-1d40-475b-83fe-20b68fa3f748
ms.date: 12/05/2018
ms.keywords: GetSeriesId, GetSeriesId method [Microsoft TV Technologies], GetSeriesId method [Microsoft TV Technologies],IIsdbSeriesDescriptor interface, IIsdbSeriesDescriptor interface [Microsoft TV Technologies],GetSeriesId method, IIsdbSeriesDescriptor.GetSeriesId, IIsdbSeriesDescriptor::GetSeriesId, dvbsiparser/IIsdbSeriesDescriptor::GetSeriesId, mstv.iisdbseriesdescriptor_getseriesid
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
 - IIsdbSeriesDescriptor::GetSeriesId
 - dvbsiparser/IIsdbSeriesDescriptor::GetSeriesId
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
 - IIsdbSeriesDescriptor.GetSeriesId
---

# IIsdbSeriesDescriptor::GetSeriesId


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

Gets a unique series identifier from an Integrated Services Digital Broadcasting (ISDB) series descriptor.

## -parameters

### -param pwVal [out]

Receives the series identifier.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/previous-versions/windows/desktop/api/dvbsiparser/nn-dvbsiparser-iisdbseriesdescriptor">IIsdbSeriesDescriptor</a>