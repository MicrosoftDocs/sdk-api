---
UID: NN:mmdeviceapi.IActivateAudioInterfaceAsyncOperation
title: IActivateAudioInterfaceAsyncOperation
author: windows-sdk-content
description: Represents an asynchronous operation activating a WASAPI interface and provides a method to retrieve the results of the activation.
old-location: coreaudio\iactivateaudiointerfaceasyncoperation.htm
old-project: CoreAudio
ms.assetid: 43b25a67-d9a8-4749-a654-c7310039c553
ms.author: windowssdkdev
ms.date: 06/04/2018
ms.keywords: IActivateAudioInterfaceAsyncOperation, IActivateAudioInterfaceAsyncOperation interface [Core Audio], IActivateAudioInterfaceAsyncOperation interface [Core Audio],described, coreaudio.iactivateaudiointerfaceasyncoperation, mmdeviceapi/IActivateAudioInterfaceAsyncOperation
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: mmdeviceapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps | UWP apps]
req.target-min-winversvr: Windows Server 2012 [desktop apps | UWP apps]
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
 - Mmdevapi.dll
api_name:
 - IActivateAudioInterfaceAsyncOperation
product: Windows
targetos: Windows
req.lib: 
req.dll: Mmdevapi.dll
req.irql: 
req.product: GDI+ 1.1
---

# IActivateAudioInterfaceAsyncOperation interface


## -description


Represents an asynchronous operation activating a <a href="https://msdn.microsoft.com/452b9725-b0b9-4888-bbb5-a23e0067e840">WASAPI</a> interface and provides a method to retrieve the results of the activation.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IActivateAudioInterfaceAsyncOperation</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IActivateAudioInterfaceAsyncOperation</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/4dd0e555-ee62-40f6-9b4a-57c6063981bf">GetActivateResult</a>
</td>
<td align="left" width="63%">
Gets the results of an asynchronous activation of a <a href="https://msdn.microsoft.com/452b9725-b0b9-4888-bbb5-a23e0067e840">WASAPI</a> interface initiated by an application calling the <a href="https://msdn.microsoft.com/7BAFD9DB-DCD7-4093-A24B-9A8556C6C45B">ActivateAudioInterfaceAsync</a> function.

</td>
</tr>
</table> 


## -remarks



<b>When to implement:</b>  
Implemented by Windows and returned from the function <a href="https://msdn.microsoft.com/7BAFD9DB-DCD7-4093-A24B-9A8556C6C45B">ActivateAudioInterfaceAsync</a>. 





## -see-also




<a href="https://msdn.microsoft.com/7BAFD9DB-DCD7-4093-A24B-9A8556C6C45B">ActivateAudioInterfaceAsync</a>



<a href="https://msdn.microsoft.com/b18e2094-e974-4c23-b70b-ace5a168132d">Core Audio Interfaces</a>



<a href="https://msdn.microsoft.com/04ff7cbb-fd33-40d9-9c11-4f716c6423b0">IActivateAudioInterfaceCompletionHandler</a>
 

 

