---
UID: NN:mmdeviceapi.IActivateAudioInterfaceAsyncOperation
title: IActivateAudioInterfaceAsyncOperation (mmdeviceapi.h)
author: windows-sdk-content
description: Represents an asynchronous operation activating a WASAPI interface and provides a method to retrieve the results of the activation.
old-location: coreaudio\iactivateaudiointerfaceasyncoperation.htm
tech.root: CoreAudio
ms.assetid: 43b25a67-d9a8-4749-a654-c7310039c553
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IActivateAudioInterfaceAsyncOperation, IActivateAudioInterfaceAsyncOperation interface [Core Audio], IActivateAudioInterfaceAsyncOperation interface [Core Audio],described, coreaudio.iactivateaudiointerfaceasyncoperation, mmdeviceapi/IActivateAudioInterfaceAsyncOperation
ms.topic: interface
f1_keywords: 
 - "mmdeviceapi/IActivateAudioInterfaceAsyncOperation"
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
req.dll: Mmdevapi.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Mmdevapi.dll
api_name:
 - IActivateAudioInterfaceAsyncOperation
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IActivateAudioInterfaceAsyncOperation interface


## -description


Represents an asynchronous operation activating a <a href="https://docs.microsoft.com/windows/desktop/CoreAudio/wasapi">WASAPI</a> interface and provides a method to retrieve the results of the activation.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IActivateAudioInterfaceAsyncOperation</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IActivateAudioInterfaceAsyncOperation</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IActivateAudioInterfaceAsyncOperation</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mmdeviceapi/nf-mmdeviceapi-iactivateaudiointerfaceasyncoperation-getactivateresult">GetActivateResult</a>
</td>
<td align="left" width="63%">
Gets the results of an asynchronous activation of a <a href="https://docs.microsoft.com/windows/desktop/CoreAudio/wasapi">WASAPI</a> interface initiated by an application calling the <a href="https://docs.microsoft.com/windows/desktop/api/mmdeviceapi/nf-mmdeviceapi-activateaudiointerfaceasync">ActivateAudioInterfaceAsync</a> function.

</td>
</tr>
</table> 


## -remarks



<b>When to implement:</b>  
Implemented by Windows and returned from the function <a href="https://docs.microsoft.com/windows/desktop/api/mmdeviceapi/nf-mmdeviceapi-activateaudiointerfaceasync">ActivateAudioInterfaceAsync</a>. 





## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/mmdeviceapi/nf-mmdeviceapi-activateaudiointerfaceasync">ActivateAudioInterfaceAsync</a>



<a href="https://docs.microsoft.com/windows/desktop/CoreAudio/core-audio-interfaces">Core Audio Interfaces</a>



<a href="https://docs.microsoft.com/windows/desktop/api/mmdeviceapi/nn-mmdeviceapi-iactivateaudiointerfacecompletionhandler">IActivateAudioInterfaceCompletionHandler</a>
 

 

