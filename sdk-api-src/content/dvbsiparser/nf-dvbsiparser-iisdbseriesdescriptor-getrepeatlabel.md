---
UID: NF:dvbsiparser.IIsdbSeriesDescriptor.GetRepeatLabel
title: IIsdbSeriesDescriptor::GetRepeatLabel (dvbsiparser.h)
description: Gets a label that identifies a series repeat from an Integrated Services Digital Broadcasting (ISDB) series descriptor.
helpviewer_keywords: ["GetRepeatLabel","GetRepeatLabel method [Microsoft TV Technologies]","GetRepeatLabel method [Microsoft TV Technologies]","IIsdbSeriesDescriptor interface","IIsdbSeriesDescriptor interface [Microsoft TV Technologies]","GetRepeatLabel method","IIsdbSeriesDescriptor.GetRepeatLabel","IIsdbSeriesDescriptor::GetRepeatLabel","dvbsiparser/IIsdbSeriesDescriptor::GetRepeatLabel","mstv.iisdbseriesdescriptor_getrepeatlabel"]
old-location: mstv\iisdbseriesdescriptor_getrepeatlabel.htm
tech.root: mstv
ms.assetid: 04b47836-0c27-41da-b71d-6c4abca6dd56
ms.date: 12/05/2018
ms.keywords: GetRepeatLabel, GetRepeatLabel method [Microsoft TV Technologies], GetRepeatLabel method [Microsoft TV Technologies],IIsdbSeriesDescriptor interface, IIsdbSeriesDescriptor interface [Microsoft TV Technologies],GetRepeatLabel method, IIsdbSeriesDescriptor.GetRepeatLabel, IIsdbSeriesDescriptor::GetRepeatLabel, dvbsiparser/IIsdbSeriesDescriptor::GetRepeatLabel, mstv.iisdbseriesdescriptor_getrepeatlabel
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
 - IIsdbSeriesDescriptor::GetRepeatLabel
 - dvbsiparser/IIsdbSeriesDescriptor::GetRepeatLabel
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
 - IIsdbSeriesDescriptor.GetRepeatLabel
---

# IIsdbSeriesDescriptor::GetRepeatLabel


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

Gets a label that identifies a series repeat from an Integrated Services Digital Broadcasting (ISDB) series descriptor.

## -parameters

### -param pbVal [out]

Receives the repeat label. If this label is zero, the series is an original broadcast.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/previous-versions/windows/desktop/api/dvbsiparser/nn-dvbsiparser-iisdbseriesdescriptor">IIsdbSeriesDescriptor</a>