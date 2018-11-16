---
UID: NF:austream.IMemoryData.GetInfo
title: IMemoryData::GetInfo
author: windows-sdk-content
description: Note  This interface is deprecated. New applications should not use it. Retrieves information describing an audio data object.
old-location: dshow\imemorydata_getinfo.htm
tech.root: DirectShow
ms.assetid: 9e9538c4-2f11-401e-a3c1-f8aa6c24f725
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: GetInfo, GetInfo method [DirectShow], GetInfo method [DirectShow],IMemoryData interface, IMemoryData interface [DirectShow],GetInfo method, IMemoryData.GetInfo, IMemoryData::GetInfo, IMemoryDataGetInfo, austream/IMemoryData::GetInfo, dshow.imemorydata_getinfo
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - austream.h
api_name:
 - IMemoryData.GetInfo
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- austream.h
: 
- IMemoryData.GetInfo
: 
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



This method determines how much data the object currently contains as last set by <a href="https://msdn.microsoft.com/22d9c24b-deb0-429a-ad9c-f6d286c7cdeb">SetActual</a>.




## -see-also




<a href="https://msdn.microsoft.com/0e809ae7-381c-4ada-8940-5d42bf5c03da">IMemoryData Interface</a>
 

 

