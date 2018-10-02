---
UID: NF:mfreadwrite.MFCreateSourceReaderFromMediaSource
title: MFCreateSourceReaderFromMediaSource function
author: windows-sdk-content
description: Creates the source reader from a media source.
old-location: mf\mfcreatesourcereaderfrommediasource.htm
tech.root: MedFound
ms.assetid: 924e1813-b025-435b-9770-52503a9eb619
ms.author: windowssdkdev
ms.date: 09/27/2018
ms.keywords: MFCreateSourceReaderFromMediaSource, MFCreateSourceReaderFromMediaSource function [Media Foundation], mf.mfcreatesourcereaderfrommediasource, mfreadwrite/MFCreateSourceReaderFromMediaSource
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: mfreadwrite.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7, Windows Vista and Platform Update Supplement for Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Mfreadwrite.lib
req.dll: Mfreadwrite.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - mfreadwrite.dll
api_name:
 - MFCreateSourceReaderFromMediaSource
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# MFCreateSourceReaderFromMediaSource function


## -description


Creates the source reader from a media source.


## -parameters




### -param pMediaSource [in]

A pointer to the <a href="https://msdn.microsoft.com/8b579f61-6fea-4b20-a051-7633fc01fa05">IMFMediaSource</a> interface of a media source.


### -param pAttributes [in]

Pointer to the <a href="https://msdn.microsoft.com/e12259f4-b631-4d4a-a296-c1cc6334b962">IMFAttributes</a> interface. You can use this parameter to configure the source reader. For more information, see <a href="https://msdn.microsoft.com/312a588a-848b-4563-893a-fac49a4ca465">Source Reader Attributes</a>. This parameter can be <b>NULL</b>.


### -param ppSourceReader [out]

Receives a pointer to the <a href="https://msdn.microsoft.com/7d3cc314-6b9e-437c-afda-ee1965a12721">IMFSourceReader</a> interface. The caller must release the interface.


## -returns



The method returns an <b>HRESULT</b>. Possible values include, but are not limited to, those in the following table.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><b>S_OK</b></b></dt>
</dl>
</td>
<td width="60%">
The method succeeded.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><b>MF_E_DRM_UNSUPPORTED</b></b></dt>
</dl>
</td>
<td width="60%">
The source contains protected content.

</td>
</tr>
</table>
 




## -remarks



Call <b>CoInitialize(Ex)</b> and <a href="https://msdn.microsoft.com/b4472e40-3681-4b26-9385-4df7bf19c2d8">MFStartup</a> before calling this function.

By default, when the application releases the source reader, the source reader shuts down the media source by calling <a href="https://msdn.microsoft.com/c7f890a8-74bd-4418-bb02-a3fee62dec6d">IMFMediaSource::Shutdown</a> on the media source. At that point, the application can no longer use the media source.

To change this default behavior, set the <a href="https://msdn.microsoft.com/c85f5994-8005-48c9-8a05-0316f48f4142">MF_SOURCE_READER_DISCONNECT_MEDIASOURCE_ON_SHUTDOWN</a> attribute in the <i>pAttributes</i> parameter. If this attribute is <b>TRUE</b>, the application is responsible for  shutting down the media source.

When using the Source Reader, do not call any of the following methods on the media source:<ul>
<li>
<a href="https://msdn.microsoft.com/113b3dc7-918e-427e-aa70-cf474b951c6d">IMFMediaSource::Pause</a>
</li>
<li>
<a href="https://msdn.microsoft.com/0a5abafe-1525-4bda-946c-05a6145e57ee">IMFMediaSource::Start</a>
</li>
<li>
<a href="https://msdn.microsoft.com/aa7af7a0-a6c2-4c9e-9f98-d36716679297">IMFMediaSource::Stop</a>
</li>
<li>All <a href="https://msdn.microsoft.com/a37d0840-c896-43a0-b3d1-c2a6aaff1b25">IMFMediaEventGenerator</a> methods</li>
</ul>


This function is available on Windows Vista if Platform Update Supplement for Windows Vista is installed.




## -see-also




<a href="https://msdn.microsoft.com/3018ffa7-e709-45b0-8b2b-7640d5633378">Media Foundation Functions</a>



<a href="https://msdn.microsoft.com/8a17a754-53ef-4c05-9189-7978d864b17a">Source Reader</a>
 

 

