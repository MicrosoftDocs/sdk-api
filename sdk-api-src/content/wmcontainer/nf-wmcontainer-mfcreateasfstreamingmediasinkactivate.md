---
UID: NF:wmcontainer.MFCreateASFStreamingMediaSinkActivate
title: MFCreateASFStreamingMediaSinkActivate function
author: windows-sdk-content
description: Creates an activation object for the ASF streaming sink.
old-location: mf\mfcreateasfstreamingmediasinkactivate.htm
old-project: medfound
ms.assetid: ffcab5ee-400a-424f-ab98-3c9e36ef40ce
ms.author: windowssdkdev
ms.date: 06/05/2018
ms.keywords: MFCreateASFStreamingMediaSinkActivate, MFCreateASFStreamingMediaSinkActivate function [Media Foundation], mf.mfcreateasfstreamingmediasinkactivate, wmcontainer/MFCreateASFStreamingMediaSinkActivate
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: wmcontainer.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
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
req.typenames: MFASF_STREAMSELECTOR_FLAGS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - mf.dll
api_name:
 - MFCreateASFStreamingMediaSinkActivate
product: Windows
targetos: Windows
req.lib: Mf.lib
req.dll: Mf.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# MFCreateASFStreamingMediaSinkActivate function


## -description


Creates an activation object for the ASF streaming sink.

The  ASF streaming sink enables  an application to write streaming Advanced Systems Format (ASF)  packets to an HTTP byte stream.
      The activation object can be used to create the ASF streaming sink in another process.


## -parameters




### -param pByteStreamActivate

A pointer to the  <a href="https://msdn.microsoft.com/c0936e3c-3cd1-4c1e-a336-2dee7d943963">IMFActivate</a> interface of an activation object. The caller  implements this interface.  The <a href="https://msdn.microsoft.com/120b8070-6732-450d-8334-b3910f7bb4d2">IMFActivate::ActivateObject</a> method of the activation object must create a byte-stream object. The byte stream exposes the <a href="https://msdn.microsoft.com/690035b7-2855-4714-938f-f8250ec70d24">IMFByteStream</a> interface. The ASF streaming sink will write data to this byte stream.


### -param pContentInfo

A pointer to an <a href="https://msdn.microsoft.com/6b7f8b68-fe98-4aeb-9842-a80ac6235999">ASF ContentInfo Object</a> that contains the properties that describe the ASF content. These  settings can contain  stream settings, encoding properties, and metadata. For more information about these properties, see <a href="https://msdn.microsoft.com/30e3c10b-1310-4194-8b83-221dfe73b03c">Setting Properties in the ContentInfo Object</a>.


### -param ppIActivate

Receives a pointer to the <a href="https://msdn.microsoft.com/c0936e3c-3cd1-4c1e-a336-2dee7d943963">IMFActivate</a> interface of the activation object that is used to create the ASF streaming-media sink. To create the media sink, the application must call <a href="https://msdn.microsoft.com/120b8070-6732-450d-8334-b3910f7bb4d2">IMFActivate::ActivateObject</a> by using the received pointer. The <b>ActivateObject</b> method also calls   <b>IMFActivate::Activate</b> on the byte stream activate object specified by  <i>pByteStreamActivate</i>, to create it so that the media sink can write streamed content in the byte stream. The caller must release the <b>IMFActivate</b> interface pointer of the media sink activation object received in <i>ppIActivate</i>.


## -returns



If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



Starting in Windows 7, Media Foundation provides an ASF streaming  sink that writes the content in  a live streaming scenario. This function should be used in secure transcode scenarios where this  media sink needs to be created and configured in the remote
process. Like the ASF file sink, the new media sink performs ASF related tasks such as writing the ASF header, generating data packets (muxing). The content is written to a caller-implemented byte stream such as an HTTP byte stream.
The caller must also provide an activation object that media sink can use to create the byte stream remotely.  

In addition, it performs transcryption for streaming protected content. It hosts the Windows Media Digital Rights Management (DRM) for Network Devices Output Trust Authority (OTA) that handles the license request and response. For more information, see <a href="https://msdn.microsoft.com/6f4ac19a-0972-4152-a64c-6c719efb396c">IMFDRMNetHelper</a> interface.

The new media sink does not perform any time adjustments.  If the clock seeks, the timestamps are not changed.




## -see-also




<a href="https://msdn.microsoft.com/bfa34529-e1f9-462b-9c99-b65cd526d364">MFCreateASFStreamingMediaSink</a>



<a href="https://msdn.microsoft.com/3018ffa7-e709-45b0-8b2b-7640d5633378">Media Foundation Functions</a>
 

 

