---
UID: NF:mfreadwrite.MFCreateSinkWriterFromMediaSink
title: MFCreateSinkWriterFromMediaSink function
author: windows-sdk-content
description: Creates the sink writer from a media sink.
old-location: mf\mfcreatesinkwriterfrommediasink.htm
tech.root: medfound
ms.assetid: 77bd81fe-bcbd-4bcd-9d3a-dd9fe6154337
ms.author: windowssdkdev
ms.date: 11/09/2018
ms.keywords: MFCreateSinkWriterFromMediaSink, MFCreateSinkWriterFromMediaSink function [Media Foundation], mf.mfcreatesinkwriterfrommediasink, mfreadwrite/MFCreateSinkWriterFromMediaSink
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
 - MFCreateSinkWriterFromMediaSink
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# MFCreateSinkWriterFromMediaSink function


## -description


Creates the sink writer from a media sink.


## -parameters




### -param pMediaSink [in]

Pointer to the <a href="https://msdn.microsoft.com/103e6fd8-a18f-480a-8261-099623014659">IMFMediaSink</a> interface of a media sink. 


### -param pAttributes [in]

Pointer to the <a href="https://msdn.microsoft.com/e12259f4-b631-4d4a-a296-c1cc6334b962">IMFAttributes</a> interface. You can use this parameter to configure the sink writer. For more information, see <a href="https://msdn.microsoft.com/f27b9beb-f35f-400e-a337-50d9de21e91e">Sink Writer Attributes</a>. This parameter can be <b>NULL</b>. 


### -param ppSinkWriter [out]

Receives a pointer to the <a href="https://msdn.microsoft.com/76fb915e-1586-429a-88a5-bd1290799352">IMFSinkWriter</a> interface. The caller must release the interface.


## -returns



If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



Call <b>CoInitialize(Ex)</b> and <a href="https://msdn.microsoft.com/b4472e40-3681-4b26-9385-4df7bf19c2d8">MFStartup</a> before calling this function.

When you are done using the media sink, call the media sink's <a href="https://msdn.microsoft.com/acda4e37-2dd0-4322-90fc-8f48d6842054">IMFMediaSink::Shutdown</a> method. (The sink writer does not shut down the media sink.) Release the sink writer before calling <b>Shutdown</b> on the media sink.

This function is available on Windows Vista if Platform Update Supplement for Windows Vista is installed.




## -see-also




<a href="https://msdn.microsoft.com/3018ffa7-e709-45b0-8b2b-7640d5633378">Media Foundation Functions</a>
 

 

