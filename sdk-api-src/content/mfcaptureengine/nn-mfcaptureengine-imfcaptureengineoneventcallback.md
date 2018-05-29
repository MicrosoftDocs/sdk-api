---
UID: NN:mfcaptureengine.IMFCaptureEngineOnEventCallback
title: IMFCaptureEngineOnEventCallback
author: windows-sdk-content
description: Callback interface for receiving events from the capture engine.
old-location: mf\imfcaptureengineoneventcallback.htm
old-project: medfound
ms.assetid: 6F04F843-160C-4F49-9841-ECC1450F4A58
ms.author: windowssdkdev
ms.date: 05/22/2018
ms.keywords: IMFCaptureEngineOnEventCallback, IMFCaptureEngineOnEventCallback interface [Media Foundation], IMFCaptureEngineOnEventCallback interface [Media Foundation],described, mf.imfcaptureengineoneventcallback, mfcaptureengine/IMFCaptureEngineOnEventCallback
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: mfcaptureengine.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: MF_CAPTURE_ENGINE_STREAM_CATEGORY
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	mfcaptureengine.h
api_name:
-	IMFCaptureEngineOnEventCallback
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IMFCaptureEngineOnEventCallback interface


## -description


Callback interface for receiving events from the capture engine.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMFCaptureEngineOnEventCallback</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IMFCaptureEngineOnEventCallback</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IMFCaptureEngineOnEventCallback</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/26C5B2E5-0543-49FC-915A-DCE097FF66BA">OnEvent</a>
</td>
<td align="left" width="63%">
Called by the capture engine to notify the application of a capture event.

</td>
</tr>
</table> 


## -remarks



To set the callback interface on the capture engine, call the <a href="https://msdn.microsoft.com/23EC8B49-2F67-4FB8-AFFA-409823ACCF59">IMFCaptureEngine::Initialize</a> method.




## -see-also




<a href="https://msdn.microsoft.com/3e367190-4c88-430e-adbf-9837e1bf0d2b">Media Foundation Interfaces</a>
 

 

