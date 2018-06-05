---
UID: NF:amstream.IAMMediaStream.JoinFilter
title: IAMMediaStream::JoinFilter
author: windows-sdk-content
description: Note  This interface is deprecated. New applications should not use it. The JoinFilter method connects a media stream to the Media Stream filter, which is used internally by the multimedia stream object. Applications should not call this method.
old-location: dshow\iammediastream_joinfilter.htm
old-project: DirectShow
ms.assetid: 638ab6e1-7663-4f15-a487-e22496672ddb
ms.author: windowssdkdev
ms.date: 05/29/2018
ms.keywords: IAMMediaStream interface [DirectShow],JoinFilter method, IAMMediaStream.JoinFilter, IAMMediaStream::JoinFilter, IAMMediaStreamJoinFilter, JoinFilter, JoinFilter method [DirectShow], JoinFilter method [DirectShow],IAMMediaStream interface, amstream/IAMMediaStream::JoinFilter, dshow.iammediastream_joinfilter
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
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	amstream.h
api_name:
-	IAMMediaStream.JoinFilter
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# IAMMediaStream::JoinFilter


## -description



<div class="alert"><b>Note</b>  This interface is deprecated. New applications should not use it.</div>
<div> </div>
The <code>JoinFilter</code> method connects a media stream to the Media Stream filter, which is used internally by the multimedia stream object. Applications should not call this method.




## -parameters




### -param pMediaStreamFilter [in]

Pointer to the filter's <a href="https://msdn.microsoft.com/1ac4976b-7088-47ac-9689-58c143746f05">IMediaStreamFilter</a> interface.


## -returns



Returns S_OK if successful.




## -see-also




<a href="https://msdn.microsoft.com/14185e7d-d08d-4fd8-a255-075eaf12a708">IAMMediaStream Interface</a>
 

 

