---
UID: NN:mfmediaengine.IMFMediaEngineNotify
title: IMFMediaEngineNotify
author: windows-driver-content
description: Callback interface for the IMFMediaEngine interface.
old-location: mf\imfmediaenginenotify.htm
old-project: medfound
ms.assetid: 85D702D4-3C9B-4848-81F2-3634C2B6AE1A
ms.author: windowsdriverdev
ms.date: 4/23/2018
ms.keywords: IMFMediaEngineNotify, IMFMediaEngineNotify interface [Media Foundation], IMFMediaEngineNotify interface [Media Foundation], described, mf.imfmediaenginenotify, mfmediaengine/IMFMediaEngineNotify
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: interface
req.header: mfmediaengine.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps | UWP apps]
req.target-min-winversvr: Windows Server 2012 [desktop apps | UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: MF_TIMED_TEXT_WRITING_MODE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	mfmediaengine.h
api_name:
-	IMFMediaEngineNotify
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IMFMediaEngineNotify interface


## -description


Callback interface for the <a href="https://msdn.microsoft.com/A0023F18-2D28-4F0D-9B00-B8FB11567034">IMFMediaEngine</a> interface.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMFMediaEngineNotify</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IMFMediaEngineNotify</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IMFMediaEngineNotify</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/F6B9E025-53C4-4459-9EC4-EA228065FAD3">EventNotify</a>
</td>
<td align="left" width="63%">
Notifies the application when a playback event occurs.

</td>
</tr>
</table> 


## -remarks



To set the callback pointer on the Media Engine, set the <a href="https://msdn.microsoft.com/5FAEF29A-B978-410A-8F5B-EB6F7E35EE6D">MF_MEDIA_ENGINE_CALLBACK</a> attribute in the <a href="https://msdn.microsoft.com/EDEAD2C4-5695-4E63-9E9E-B09D75B60B7F">IMFMediaEngineClassFactory::CreateInstance</a> method.




## -see-also




<a href="https://msdn.microsoft.com/3e367190-4c88-430e-adbf-9837e1bf0d2b">Media Foundation Interfaces</a>
 

 

