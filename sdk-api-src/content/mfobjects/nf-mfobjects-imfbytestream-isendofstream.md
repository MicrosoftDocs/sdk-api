---
UID: NF:mfobjects.IMFByteStream.IsEndOfStream
title: IMFByteStream::IsEndOfStream
author: windows-sdk-content
description: Queries whether the current position has reached the end of the stream.
old-location: mf\imfbytestream_isendofstream.htm
tech.root: medfound
ms.assetid: 5e5c02ea-d3fc-4d8d-aa8b-87aa033a3644
ms.author: windowssdkdev
ms.date: 10/10/2018
ms.keywords: 5e5c02ea-d3fc-4d8d-aa8b-87aa033a3644, IMFByteStream interface [Media Foundation],IsEndOfStream method, IMFByteStream.IsEndOfStream, IMFByteStream::IsEndOfStream, IsEndOfStream, IsEndOfStream method [Media Foundation], IsEndOfStream method [Media Foundation],IMFByteStream interface, mf.imfbytestream_isendofstream, mfobjects/IMFByteStream::IsEndOfStream
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: mfobjects.h
req.include-header: Mfidl.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Mfuuid.lib
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mfuuid.lib
 - mfuuid.dll
api_name:
 - IMFByteStream.IsEndOfStream
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMFByteStream::IsEndOfStream


## -description



Queries whether the current position has reached the end of the stream.




## -parameters




### -param pfEndOfStream [out]

Receives the value <b>TRUE</b> if the end of the stream has been reached, or <b>FALSE</b> otherwise.
          


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



This interface is available on the following platforms if the Windows Media Format 11 SDK redistributable components are installed:

<ul>
<li>Windows XP with Service Pack 2 (SP2) and later.</li>
<li>Windows XP Media Center Edition 2005 with KB900325 (Windows XP Media Center Edition 2005) and KB925766 (October 2006 Update Rollup for Windows XP Media Center Edition) installed.</li>
</ul>



## -see-also




<a href="https://msdn.microsoft.com/690035b7-2855-4714-938f-f8250ec70d24">IMFByteStream</a>
 

 

