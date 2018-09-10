---
UID: NN:mfmediaengine.IMFMediaEngineEME
title: IMFMediaEngineEME
author: windows-sdk-content
description: Implemented by the media engine to add encrypted media extensions methods.
old-location: mf\imfmediaengineeme.htm
tech.root: medfound
ms.assetid: d03045d5-bafe-4e65-98da-e9ea8104c169
ms.author: windowssdkdev
ms.date: 08/07/2018
ms.keywords: IMFMediaEngineEME, IMFMediaEngineEME interface [Media Foundation], IMFMediaEngineEME interface [Media Foundation],described, mf.imfmediaengineeme, mfmediaengine/IMFMediaEngineEME
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
 - IMFMediaEngineEME
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMFMediaEngineEME interface


## -description


Implemented by the media engine to add encrypted media extensions methods.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMFMediaEngineEME</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IMFMediaEngineEME</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IMFMediaEngineEME</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/e6556a02-445d-4436-80de-e4156d6a3d63">get_Keys</a>
</td>
<td align="left" width="63%">
Gets the media keys object associated with the media engine or <b>null</b> if there is not a media keys object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/659b566e-d488-489d-9a12-bfe9695c5f94">SetMediaKeys</a>
</td>
<td align="left" width="63%">
Sets the media keys object to use with the media engine.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/3e367190-4c88-430e-adbf-9837e1bf0d2b">Media Foundation Interfaces</a>
 

 

