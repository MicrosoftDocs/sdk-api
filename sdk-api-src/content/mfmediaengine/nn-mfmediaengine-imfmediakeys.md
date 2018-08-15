---
UID: NN:mfmediaengine.IMFMediaKeys
title: IMFMediaKeys
author: windows-sdk-content
description: Represents a media keys used for decrypting media data using a Digital Rights Management (DRM) key system.
old-location: mf\imfmediakeys.htm
old-project: medfound
ms.assetid: 0689d938-e0be-46d7-bfed-add431331a90
ms.author: windowssdkdev
ms.date: 08/07/2018
ms.keywords: IMFMediaKeys, IMFMediaKeys interface [Media Foundation], IMFMediaKeys interface [Media Foundation],described, mf.imfmediakeys, mfmediaengine/IMFMediaKeys
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: mfmediaengine.h
req.include-header: 
req.redist: 
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
tech.root: 
req.typenames: MF_MEDIA_ENGINE_KEYERR
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mfmediaengine.h
api_name:
 - IMFMediaKeys
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IMFMediaKeys interface


## -description


Represents a media keys used for decrypting media data using a Digital Rights Management (DRM) key system. 


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMFMediaKeys</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IMFMediaKeys</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IMFMediaKeys</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/9f11433c-7cff-4a59-9d4a-7f4b56ba62cf">CreateSession</a>
</td>
<td align="left" width="63%">
Creates a media key session object using the specified initialization data and custom data.
.


</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d60ee85b-b5fc-4d06-a3a2-f61ff3635d99">get_KeySystem</a>
</td>
<td align="left" width="63%">
Gets the key system string the <b>IMFMediaKeys</b> object was created with.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/35d76cbc-04c7-49e7-9451-6b032ccd2937">GetSuspendNotify</a>
</td>
<td align="left" width="63%">
Gets the suspend notify interface of the Content Decryption Module (CDM).

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/464b598c-5fa7-40af-83ba-8619fbd84b04">Shutdown</a>
</td>
<td align="left" width="63%">


</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/3e367190-4c88-430e-adbf-9837e1bf0d2b">Media Foundation Interfaces</a>
 

 

