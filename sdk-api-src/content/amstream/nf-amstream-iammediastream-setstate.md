---
UID: NF:amstream.IAMMediaStream.SetState
title: IAMMediaStream::SetState
author: windows-sdk-content
description: Note  This interface is deprecated. New applications should not use it. The SetState method sets the filter state.
old-location: dshow\iammediastream_setstate.htm
old-project: DirectShow
ms.assetid: 2134c2cf-4d78-438c-8fb9-a96f87f682d9
ms.author: windowssdkdev
ms.date: 07/16/2018
ms.keywords: IAMMediaStream interface [DirectShow],SetState method, IAMMediaStream.SetState, IAMMediaStream::SetState, IAMMediaStreamSetState, SetState, SetState method [DirectShow], SetState method [DirectShow],IAMMediaStream interface, amstream/IAMMediaStream::SetState, dshow.iammediastream_setstate
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: amstream.h
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
tech.root: 
req.typenames: AMSI_RESULT
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - amstream.h
api_name:
 - IAMMediaStream.SetState
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# IAMMediaStream::SetState


## -description



<div class="alert"><b>Note</b>  This interface is deprecated. New applications should not use it.</div>
<div> </div>
The <code>SetState</code> method sets the filter state.




## -parameters




### -param State [in]

Sets the filter's state, as specified by the <a href="https://msdn.microsoft.com/41f88abc-57d1-4f80-a099-d17e624ab8a6">FILTER_STATE</a> enumerated type.


## -returns



Returns S_OK if successful or E_INVALIDARG if the <i>State</i> parameter is invalid.




## -remarks



Applications should not call this method.




## -see-also




<a href="https://msdn.microsoft.com/14185e7d-d08d-4fd8-a255-075eaf12a708">IAMMediaStream Interface</a>
 

 

