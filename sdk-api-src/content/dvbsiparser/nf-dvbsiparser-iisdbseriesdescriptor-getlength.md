---
UID: NF:dvbsiparser.IIsdbSeriesDescriptor.GetLength
title: IIsdbSeriesDescriptor::GetLength (dvbsiparser.h)
description: Gets the body length of an Integrated Services Digital Broadcasting (ISDB) series descriptor, in bytes.
helpviewer_keywords: ["GetLength","GetLength method [Microsoft TV Technologies]","GetLength method [Microsoft TV Technologies]","IIsdbSeriesDescriptor interface","IIsdbSeriesDescriptor interface [Microsoft TV Technologies]","GetLength method","IIsdbSeriesDescriptor.GetLength","IIsdbSeriesDescriptor::GetLength","dvbsiparser/IIsdbSeriesDescriptor::GetLength","mstv.iisdbseriesdescriptor_getlength"]
old-location: mstv\iisdbseriesdescriptor_getlength.htm
tech.root: mstv
ms.assetid: 703e4406-7fca-4d96-83de-56fd2ff52d30
ms.date: 12/05/2018
ms.keywords: GetLength, GetLength method [Microsoft TV Technologies], GetLength method [Microsoft TV Technologies],IIsdbSeriesDescriptor interface, IIsdbSeriesDescriptor interface [Microsoft TV Technologies],GetLength method, IIsdbSeriesDescriptor.GetLength, IIsdbSeriesDescriptor::GetLength, dvbsiparser/IIsdbSeriesDescriptor::GetLength, mstv.iisdbseriesdescriptor_getlength
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
 - IIsdbSeriesDescriptor::GetLength
 - dvbsiparser/IIsdbSeriesDescriptor::GetLength
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
 - IIsdbSeriesDescriptor.GetLength
---

# IIsdbSeriesDescriptor::GetLength


## -description

 Gets the body length of an Integrated Services Digital Broadcasting (ISDB) series descriptor, in bytes.

## -parameters

### -param pbVal [out]

Receives the descriptor length.

## -returns

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.

## -see-also

<a href="/previous-versions/windows/desktop/api/dvbsiparser/nn-dvbsiparser-iisdbseriesdescriptor">IIsdbSeriesDescriptor</a>