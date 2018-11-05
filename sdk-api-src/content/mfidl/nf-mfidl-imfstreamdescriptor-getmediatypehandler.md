---
UID: NF:mfidl.IMFStreamDescriptor.GetMediaTypeHandler
title: IMFStreamDescriptor::GetMediaTypeHandler
author: windows-sdk-content
description: Retrieves a media type handler for the stream. The media type handler can be used to enumerate supported media types for the stream, get the current media type, and set the media type.
old-location: mf\imfstreamdescriptor_getmediatypehandler.htm
tech.root: medfound
ms.assetid: 8e991417-fe15-4749-94c4-26c621692b52
ms.author: windowssdkdev
ms.date: 11/02/2018
ms.keywords: 8e991417-fe15-4749-94c4-26c621692b52, GetMediaTypeHandler, GetMediaTypeHandler method [Media Foundation], GetMediaTypeHandler method [Media Foundation],IMFStreamDescriptor interface, IMFStreamDescriptor interface [Media Foundation],GetMediaTypeHandler method, IMFStreamDescriptor.GetMediaTypeHandler, IMFStreamDescriptor::GetMediaTypeHandler, mf.imfstreamdescriptor_getmediatypehandler, mfidl/IMFStreamDescriptor::GetMediaTypeHandler
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: mfidl.h
req.include-header: 
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
 - IMFStreamDescriptor.GetMediaTypeHandler
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMFStreamDescriptor::GetMediaTypeHandler


## -description



Retrieves a media type handler for the stream. The media type handler can be used to enumerate supported media types for the stream, get the current media type, and set the media type.




## -parameters




### -param ppMediaTypeHandler [out]

Receives a pointer to the <a href="https://msdn.microsoft.com/5b937bf7-4f86-4dc1-a4d5-7e724dcf5b36">IMFMediaTypeHandler</a> interface. The caller must release the interface.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



This interface is available on the following platforms if the Windows Media Format 11 SDK redistributable components are installed:

<ul>
<li>Windows XP with Service Pack 2 (SP2) and later.</li>
<li>Windows XP Media Center Edition 2005 with KB900325 (Windows XP Media Center Edition 2005) and KB925766 (October 2006 Update Rollup for Windows XP Media Center Edition) installed.</li>
</ul>



## -see-also




<a href="https://msdn.microsoft.com/a076dc6e-d9cb-4f7e-8cc2-b66292da295f">IMFStreamDescriptor</a>



<a href="https://msdn.microsoft.com/714c8bda-5ce1-47e2-ba73-9304e26b3129">Presentation Descriptors</a>
 

 

