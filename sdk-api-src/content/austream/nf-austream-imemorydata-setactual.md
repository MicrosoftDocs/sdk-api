---
UID: NF:austream.IMemoryData.SetActual
title: IMemoryData::SetActual method
author: windows-driver-content
description: Note  This interface is deprecated. New applications should not use it. Sets the amount of audio data currently in the object.
old-location: dshow\imemorydata_setactual.htm
old-project: DirectShow
ms.assetid: 22d9c24b-deb0-429a-ad9c-f6d286c7cdeb
ms.author: windowsdriverdev
ms.date: 4/26/2018
ms.keywords: IMemoryData, IMemoryData interface [DirectShow], SetActual method, IMemoryData::SetActual, IMemoryDataSetActual, SetActual method [DirectShow], SetActual method [DirectShow], IMemoryData interface, SetActual,IMemoryData.SetActual, austream/IMemoryData::SetActual, dshow.imemorydata_setactual
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
req.typenames: AUDIO_STREAM_CATEGORY
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	austream.h
api_name:
-	IMemoryData.SetActual
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# IMemoryData::SetActual method


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



This method is usually called by the <a href="https://msdn.microsoft.com/b4098876-6c11-4cc6-8b6d-16edc02316f3">IAudioMediaStream</a> or <a href="https://msdn.microsoft.com/53deec43-30ca-472e-9a82-750049686d2a">IAudioStreamSample</a> object, rather than by the application.




## -see-also




<a href="https://msdn.microsoft.com/0e809ae7-381c-4ada-8940-5d42bf5c03da">IMemoryData Interface</a>
 

 

