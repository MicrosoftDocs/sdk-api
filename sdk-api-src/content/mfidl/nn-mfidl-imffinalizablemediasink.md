---
UID: NN:mfidl.IMFFinalizableMediaSink
title: IMFFinalizableMediaSink
author: windows-sdk-content
description: Optionally supported by media sinks to perform required tasks before shutdown.
old-location: mf\imffinalizablemediasink.htm
old-project: medfound
ms.assetid: e60c2773-f2fc-469e-a698-036390cbed16
ms.author: windowssdkdev
ms.date: 07/18/2018
ms.keywords: IMFFinalizableMediaSink, IMFFinalizableMediaSink interface [Media Foundation], IMFFinalizableMediaSink interface [Media Foundation],described, e60c2773-f2fc-469e-a698-036390cbed16, mf.imffinalizablemediasink, mfidl/IMFFinalizableMediaSink
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: mfidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
req.typenames: MFSensorDeviceMode
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mfuuid.lib
 - mfuuid.dll
api_name:
 - IMFFinalizableMediaSink
product: Windows
targetos: Windows
req.lib: Mfuuid.lib
req.dll: Mfplat.dll
req.irql: 
req.product: GDI+ 1.1
---

# IMFFinalizableMediaSink interface


## -description


Optionally supported by media sinks to perform required tasks before shutdown. This interface is typically exposed by archive sinks—that is, media sinks that write to a file. It is used to perform tasks such as flushing data to disk or updating a file header.

To get a pointer to this interface, call <b>QueryInterface</b> on the media sink.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMFFinalizableMediaSink</b> interface inherits from <a href="https://msdn.microsoft.com/103e6fd8-a18f-480a-8261-099623014659">IMFMediaSink</a>. <b>IMFFinalizableMediaSink</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IMFFinalizableMediaSink</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/fbcb7722-ba64-40a6-9c43-26a6b8dce7f6">BeginFinalize</a>
</td>
<td align="left" width="63%">
Notifies the media sink to complete its final tasks.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/1b2a9b24-69da-41c7-8379-3f3d066d2582">EndFinalize</a>
</td>
<td align="left" width="63%">
Called when the asynchronous callback given to <a href="https://msdn.microsoft.com/fbcb7722-ba64-40a6-9c43-26a6b8dce7f6">BeginFinalize</a> is invoked.

</td>
</tr>
</table> 


## -remarks



If a media sink exposes this interface, the Media Session will call <a href="https://msdn.microsoft.com/fbcb7722-ba64-40a6-9c43-26a6b8dce7f6">BeginFinalize</a> on the sink before the session closes.




## -see-also




<a href="https://msdn.microsoft.com/103e6fd8-a18f-480a-8261-099623014659">IMFMediaSink</a>



<a href="https://msdn.microsoft.com/3e367190-4c88-430e-adbf-9837e1bf0d2b">Media Foundation Interfaces</a>
 

 

