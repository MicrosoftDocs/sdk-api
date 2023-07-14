---
UID: NF:dvbsiparser.IIsdbSeriesDescriptor.GetExpireDate
title: IIsdbSeriesDescriptor::GetExpireDate (dvbsiparser.h)
description: Gets a series expiration date from an Integrated Services Digital Broadcasting (ISDB) series descriptor.
helpviewer_keywords: ["GetExpireDate","GetExpireDate method [Microsoft TV Technologies]","GetExpireDate method [Microsoft TV Technologies]","IIsdbSeriesDescriptor interface","IIsdbSeriesDescriptor interface [Microsoft TV Technologies]","GetExpireDate method","IIsdbSeriesDescriptor.GetExpireDate","IIsdbSeriesDescriptor::GetExpireDate","dvbsiparser/IIsdbSeriesDescriptor::GetExpireDate","mstv.iisdbseriesdescriptor_getexpiredate"]
old-location: mstv\iisdbseriesdescriptor_getexpiredate.htm
tech.root: mstv
ms.assetid: 0d658904-4f81-443b-b69d-814e606dabc4
ms.date: 12/05/2018
ms.keywords: GetExpireDate, GetExpireDate method [Microsoft TV Technologies], GetExpireDate method [Microsoft TV Technologies],IIsdbSeriesDescriptor interface, IIsdbSeriesDescriptor interface [Microsoft TV Technologies],GetExpireDate method, IIsdbSeriesDescriptor.GetExpireDate, IIsdbSeriesDescriptor::GetExpireDate, dvbsiparser/IIsdbSeriesDescriptor::GetExpireDate, mstv.iisdbseriesdescriptor_getexpiredate
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
 - IIsdbSeriesDescriptor::GetExpireDate
 - dvbsiparser/IIsdbSeriesDescriptor::GetExpireDate
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
 - IIsdbSeriesDescriptor.GetExpireDate
---

# IIsdbSeriesDescriptor::GetExpireDate


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

Gets a series expiration date from an Integrated Services Digital Broadcasting (ISDB) series descriptor.

## -parameters

### -param pfValid [out]

Receives a flag that indicates whether the series expiration date in the descriptor expire_date field is valid.

### -param pmdtVal [out]

Receives the date and time when the series expires.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/previous-versions/windows/desktop/api/dvbsiparser/nn-dvbsiparser-iisdbseriesdescriptor">IIsdbSeriesDescriptor</a>