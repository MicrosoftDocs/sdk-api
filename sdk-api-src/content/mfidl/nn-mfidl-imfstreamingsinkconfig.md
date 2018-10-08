---
UID: NN:mfidl.IMFStreamingSinkConfig
title: IMFStreamingSinkConfig
author: windows-sdk-content
description: Passes configuration information to the media sinks that are used for streaming the content.
old-location: mf\imfstreamingsinkconfig.htm
tech.root: medfound
ms.assetid: 5eaef815-9660-487a-885d-457cd270ba3d
ms.author: windowssdkdev
ms.date: 10/05/2018
ms.keywords: IMFStreamingSinkConfig, IMFStreamingSinkConfig interface [Media Foundation], IMFStreamingSinkConfig interface [Media Foundation],described, mf.imfstreamingsinkconfig, mfidl/IMFStreamingSinkConfig
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: mfidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps \| UWP apps]
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mfidl.h
api_name:
 - IMFStreamingSinkConfig
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMFStreamingSinkConfig interface


## -description


Passes configuration information to the media sinks that are used for streaming the content.  Optionally, this interface is supported by media sinks. The built-in ASF streaming media sink and the MP3 media sink implement this interface.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMFStreamingSinkConfig</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IMFStreamingSinkConfig</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IMFStreamingSinkConfig</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/22a75b19-9949-48fe-8844-511b11fbf20b">StartStreaming</a>
</td>
<td align="left" width="63%">
Called by the streaming media client before the Media Session starts streaming to specify the byte offset or the time offset.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/3e367190-4c88-430e-adbf-9837e1bf0d2b">Media Foundation Interfaces</a>
 

 

