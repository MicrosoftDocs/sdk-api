---
UID: NN:mmdeviceapi.IActivateAudioInterfaceCompletionHandler
title: IActivateAudioInterfaceCompletionHandler
author: windows-sdk-content
description: Provides a callback to indicate that activation of a WASAPI interface is complete.
old-location: coreaudio\iactivateaudiointerfacecompletionhandler.htm
old-project: CoreAudio
ms.assetid: 04ff7cbb-fd33-40d9-9c11-4f716c6423b0
ms.author: windowssdkdev
ms.date: 08/14/2018
ms.keywords: IActivateAudioInterfaceCompletionHandler, IActivateAudioInterfaceCompletionHandler interface [Core Audio], IActivateAudioInterfaceCompletionHandler interface [Core Audio],described, coreaudio.iactivateaudiointerfacecompletionhandler, mmdeviceapi/IActivateAudioInterfaceCompletionHandler
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: mmdeviceapi.h
req.include-header: 
req.redist: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2012 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Mmdeviceapi.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: EndpointFormFactor
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mmdeviceapi.h
api_name:
 - IActivateAudioInterfaceCompletionHandler
product: Windows
targetos: Windows
req.lib: 
req.dll: Mmdevapi.dll
req.irql: 
req.product: GDI+ 1.1
---

# IActivateAudioInterfaceCompletionHandler interface


## -description


Provides a callback to indicate that activation of a <a href="https://msdn.microsoft.com/452b9725-b0b9-4888-bbb5-a23e0067e840">WASAPI</a> interface is complete.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IActivateAudioInterfaceCompletionHandler</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IActivateAudioInterfaceCompletionHandler</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IActivateAudioInterfaceCompletionHandler</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/f434db12-ab8e-40ca-8a55-b02f28ea5575">ActivateCompleted</a>
</td>
<td align="left" width="63%">
Indicates that activation of a <a href="https://msdn.microsoft.com/452b9725-b0b9-4888-bbb5-a23e0067e840">WASAPI</a> interface is complete and results are available.

</td>
</tr>
</table> 


## -remarks



<b>When to implement:</b>  
An application implements this interface if it calls the <a href="https://msdn.microsoft.com/7BAFD9DB-DCD7-4093-A24B-9A8556C6C45B">ActivateAudioInterfaceAsync</a> function.


The implementation must be agile (aggregating a free-threaded marshaler).




## -see-also




<a href="https://msdn.microsoft.com/7BAFD9DB-DCD7-4093-A24B-9A8556C6C45B">ActivateAudioInterfaceAsync</a>



<a href="https://msdn.microsoft.com/b18e2094-e974-4c23-b70b-ace5a168132d">Core Audio Interfaces</a>



<a href="https://msdn.microsoft.com/43b25a67-d9a8-4749-a654-c7310039c553">IActivateAudioInterfaceAsyncOperation</a>
 

 

