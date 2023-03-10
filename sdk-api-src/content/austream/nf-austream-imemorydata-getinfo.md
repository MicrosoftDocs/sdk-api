---
UID: NF:austream.IMemoryData.GetInfo
title: IMemoryData::GetInfo (austream.h)
description: Note  This interface is deprecated. New applications should not use it. Retrieves information describing an audio data object.
helpviewer_keywords: ["GetInfo","GetInfo method [DirectShow]","GetInfo method [DirectShow]","IMemoryData interface","IMemoryData interface [DirectShow]","GetInfo method","IMemoryData.GetInfo","IMemoryData::GetInfo","IMemoryDataGetInfo","austream/IMemoryData::GetInfo","dshow.imemorydata_getinfo"]
old-location: dshow\imemorydata_getinfo.htm
tech.root: dshow
ms.assetid: 9e9538c4-2f11-401e-a3c1-f8aa6c24f725
ms.date: 12/05/2018
ms.keywords: GetInfo, GetInfo method [DirectShow], GetInfo method [DirectShow],IMemoryData interface, IMemoryData interface [DirectShow],GetInfo method, IMemoryData.GetInfo, IMemoryData::GetInfo, IMemoryDataGetInfo, austream/IMemoryData::GetInfo, dshow.imemorydata_getinfo
req.header: austream.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
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
 - IMemoryData::GetInfo
 - austream/IMemoryData::GetInfo
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - austream.h
api_name:
 - IMemoryData.GetInfo
---

# IMemoryData::GetInfo


## -description

<div class="alert"><b>Note</b>  This interface is deprecated. New applications should not use it.</div>
<div> </div>
Retrieves information describing an audio data object.

## -parameters

### -param pdwLength [out]

Length of memory in bytes, if non-<b>NULL</b>.

### -param ppbData [out]

Pointer to the memory, if non-<b>NULL</b>.

### -param pcbActualData [out]

Length of data in bytes, if non-<b>NULL</b>.

## -returns

Returns an <b>HRESULT</b> value.

## -remarks

This method determines how much data the object currently contains as last set by <a href="/windows/desktop/api/austream/nf-austream-imemorydata-setactual">SetActual</a>.

## -see-also

<a href="/windows/desktop/api/austream/nn-austream-imemorydata">IMemoryData Interface</a>