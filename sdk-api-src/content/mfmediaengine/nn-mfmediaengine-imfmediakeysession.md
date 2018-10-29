---
UID: NN:mfmediaengine.IMFMediaKeySession
title: IMFMediaKeySession
author: windows-sdk-content
description: Represents a session with the Digital Rights Management (DRM) key system.
old-location: mf\imfmediakeysession.htm
tech.root: medfound
ms.assetid: 07f97bc9-9da2-4655-9ab9-5e17abc57d6d
ms.author: windowssdkdev
ms.date: 10/26/2018
ms.keywords: IMFMediaKeySession, IMFMediaKeySession interface [Media Foundation], IMFMediaKeySession interface [Media Foundation],described, mf.imfmediakeysession, mfmediaengine/IMFMediaKeySession
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
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
 - IMFMediaKeySession
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMFMediaKeySession interface


## -description


Represents a session with the Digital Rights Management (DRM) key system.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMFMediaKeySession</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IMFMediaKeySession</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IMFMediaKeySession</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/97c6b4bd-a973-4475-a325-0373af9b54b1">Close</a>
</td>
<td align="left" width="63%">
Closes the media key session and must be called before the key session is released.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/eaf3a411-7282-496c-8095-79a8913a0f8e">get_KeySystem</a>
</td>
<td align="left" width="63%">
Gets the name of the  key system name the media keys object was created with.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/779ebea9-69ff-469a-8ee0-06d570ede6cb">get_SessionId</a>
</td>
<td align="left" width="63%">
Gets a unique session id created for this session.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/4693b7d5-59ee-472f-83fc-1ecbcc165dac">GetError</a>
</td>
<td align="left" width="63%">
Gets the error state associated with the media key session.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/29e66037-5f18-4724-b6f2-d85555e6af69">Update</a>
</td>
<td align="left" width="63%">
Passes in a key value with any associated data required by the Content Decryption Module for the given key system.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/3e367190-4c88-430e-adbf-9837e1bf0d2b">Media Foundation Interfaces</a>
 

 

