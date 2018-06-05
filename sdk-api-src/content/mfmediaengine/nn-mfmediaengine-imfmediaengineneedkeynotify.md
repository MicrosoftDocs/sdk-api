---
UID: NN:mfmediaengine.IMFMediaEngineNeedKeyNotify
title: IMFMediaEngineNeedKeyNotify
author: windows-sdk-content
description: Represents a callback to the media engine to notify key request data.
old-location: mf\imfmediaengineneedkeynotify.htm
old-project: medfound
ms.assetid: bbedfbe8-9389-4b4f-8d52-111c787a6268
ms.author: windowssdkdev
ms.date: 05/22/2018
ms.keywords: IMFMediaEngineNeedKeyNotify, IMFMediaEngineNeedKeyNotify interface [Media Foundation], IMFMediaEngineNeedKeyNotify interface [Media Foundation],described, mf.imfmediaengineneedkeynotify, mfmediaengine/IMFMediaEngineNeedKeyNotify
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
tech.root: 
req.typenames: MF_TIMED_TEXT_WRITING_MODE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	mfmediaengine.h
api_name:
-	IMFMediaEngineNeedKeyNotify
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IMFMediaEngineNeedKeyNotify interface


## -description


Represents a callback to the media engine to notify key request data.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMFMediaEngineNeedKeyNotify</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IMFMediaEngineNeedKeyNotify</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IMFMediaEngineNeedKeyNotify</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/2b9a64d6-1a0f-4375-973a-42734ac5658e">NeedKey</a>
</td>
<td align="left" width="63%">
Notifies the application that a key or keys are needed along with any initialization data.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/3e367190-4c88-430e-adbf-9837e1bf0d2b">Media Foundation Interfaces</a>
 

 

