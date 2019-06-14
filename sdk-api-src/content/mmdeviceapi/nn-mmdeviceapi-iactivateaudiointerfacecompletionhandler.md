---
UID: NN:mmdeviceapi.IActivateAudioInterfaceCompletionHandler
title: IActivateAudioInterfaceCompletionHandler (mmdeviceapi.h)
author: windows-sdk-content
description: Provides a callback to indicate that activation of a WASAPI interface is complete.
old-location: coreaudio\iactivateaudiointerfacecompletionhandler.htm
tech.root: CoreAudio
ms.assetid: 04ff7cbb-fd33-40d9-9c11-4f716c6423b0
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IActivateAudioInterfaceCompletionHandler, IActivateAudioInterfaceCompletionHandler interface [Core Audio], IActivateAudioInterfaceCompletionHandler interface [Core Audio],described, coreaudio.iactivateaudiointerfacecompletionhandler, mmdeviceapi/IActivateAudioInterfaceCompletionHandler
ms.topic: interface
req.header: mmdeviceapi.h
req.include-header: 
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
req.lib: 
req.dll: 
req.irql: 
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
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IActivateAudioInterfaceCompletionHandler interface


## -description


Provides a callback to indicate that activation of a <a href="https://docs.microsoft.com/windows/desktop/CoreAudio/wasapi">WASAPI</a> interface is complete.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IActivateAudioInterfaceCompletionHandler</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IActivateAudioInterfaceCompletionHandler</b> also has these types of members:
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
<a href="https://docs.microsoft.com/windows/desktop/api/mmdeviceapi/nf-mmdeviceapi-iactivateaudiointerfacecompletionhandler-activatecompleted">ActivateCompleted</a>
</td>
<td align="left" width="63%">
Indicates that activation of a <a href="https://docs.microsoft.com/windows/desktop/CoreAudio/wasapi">WASAPI</a> interface is complete and results are available.

</td>
</tr>
</table> 


## -remarks



<b>When to implement:</b>  
An application implements this interface if it calls the <a href="https://docs.microsoft.com/windows/desktop/api/mmdeviceapi/nf-mmdeviceapi-activateaudiointerfaceasync">ActivateAudioInterfaceAsync</a> function.


The implementation must be agile (aggregating a free-threaded marshaler).




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/mmdeviceapi/nf-mmdeviceapi-activateaudiointerfaceasync">ActivateAudioInterfaceAsync</a>



<a href="https://docs.microsoft.com/windows/desktop/CoreAudio/core-audio-interfaces">Core Audio Interfaces</a>



<a href="https://docs.microsoft.com/windows/desktop/api/mmdeviceapi/nn-mmdeviceapi-iactivateaudiointerfaceasyncoperation">IActivateAudioInterfaceAsyncOperation</a>
 

 

