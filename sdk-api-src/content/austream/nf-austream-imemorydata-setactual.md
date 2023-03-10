---
UID: NF:austream.IMemoryData.SetActual
title: IMemoryData::SetActual (austream.h)
description: Note  This interface is deprecated. New applications should not use it. Sets the amount of audio data currently in the object.
helpviewer_keywords: ["IMemoryData interface [DirectShow]","SetActual method","IMemoryData.SetActual","IMemoryData::SetActual","IMemoryDataSetActual","SetActual","SetActual method [DirectShow]","SetActual method [DirectShow]","IMemoryData interface","austream/IMemoryData::SetActual","dshow.imemorydata_setactual"]
old-location: dshow\imemorydata_setactual.htm
tech.root: dshow
ms.assetid: 22d9c24b-deb0-429a-ad9c-f6d286c7cdeb
ms.date: 12/05/2018
ms.keywords: IMemoryData interface [DirectShow],SetActual method, IMemoryData.SetActual, IMemoryData::SetActual, IMemoryDataSetActual, SetActual, SetActual method [DirectShow], SetActual method [DirectShow],IMemoryData interface, austream/IMemoryData::SetActual, dshow.imemorydata_setactual
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
 - IMemoryData::SetActual
 - austream/IMemoryData::SetActual
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
 - IMemoryData.SetActual
---

# IMemoryData::SetActual


## -description

<div class="alert"><b>Note</b>  This interface is deprecated. New applications should not use it.</div>
<div> </div>
Sets the amount of audio data currently in the object.

## -parameters

### -param cbDataValid [in]

Amount of data, in bytes.

## -returns

Returns S_OK if successful or E_POINTER if the required parameter is <b>NULL</b>.

## -remarks

This method is usually called by the <a href="/windows/desktop/api/austream/nn-austream-iaudiomediastream">IAudioMediaStream</a> or <a href="/windows/desktop/api/austream/nn-austream-iaudiostreamsample">IAudioStreamSample</a> object, rather than by the application.

## -see-also

<a href="/windows/desktop/api/austream/nn-austream-imemorydata">IMemoryData Interface</a>