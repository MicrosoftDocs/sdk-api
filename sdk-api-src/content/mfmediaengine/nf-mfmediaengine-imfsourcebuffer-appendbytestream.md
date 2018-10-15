---
UID: NF:mfmediaengine.IMFSourceBuffer.AppendByteStream
title: IMFSourceBuffer::AppendByteStream
author: windows-sdk-content
description: Appends the media segment from the specified byte stream to the IMFSourceBuffer.
old-location: mf\imfsourcebuffer_appendbytestream.htm
tech.root: medfound
ms.assetid: 1a4fc611-4923-48ad-bc92-c3686d855c13
ms.author: windowssdkdev
ms.date: 10/10/2018
ms.keywords: AppendByteStream, AppendByteStream method [Media Foundation], AppendByteStream method [Media Foundation],IMFSourceBuffer interface, IMFSourceBuffer interface [Media Foundation],AppendByteStream method, IMFSourceBuffer.AppendByteStream, IMFSourceBuffer::AppendByteStream, mf.imfsourcebuffer_appendbytestream, mfmediaengine/IMFSourceBuffer::AppendByteStream
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: mfmediaengine.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8.1 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Mfmediaengine.idl
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
 - mfmediaengine.h
api_name:
 - IMFSourceBuffer.AppendByteStream
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMFSourceBuffer::AppendByteStream


## -description


Appends the media segment from the specified byte stream to the <a href="https://msdn.microsoft.com/f241e232-9013-46d0-be97-2d6b5246cff3">IMFSourceBuffer</a>.


## -parameters




### -param pStream [in]

The media segment data.


### -param pMaxLen [in]

The maximum length of the media segment data.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/f241e232-9013-46d0-be97-2d6b5246cff3">IMFSourceBuffer</a>
 

 

