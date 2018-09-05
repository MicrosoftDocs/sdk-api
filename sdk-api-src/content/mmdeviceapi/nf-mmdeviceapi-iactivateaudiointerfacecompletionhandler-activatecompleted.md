---
UID: NF:mmdeviceapi.IActivateAudioInterfaceCompletionHandler.ActivateCompleted
title: IActivateAudioInterfaceCompletionHandler::ActivateCompleted
author: windows-sdk-content
description: Indicates that activation of a WASAPI interface is complete and results are available.
old-location: coreaudio\iactivateaudiointerfacecompletionhandler_activatecompleted.htm
old-project: CoreAudio
ms.assetid: f434db12-ab8e-40ca-8a55-b02f28ea5575
ms.author: windowssdkdev
ms.date: 08/24/2018
ms.keywords: ActivateCompleted, ActivateCompleted method [Core Audio], ActivateCompleted method [Core Audio],IActivateAudioInterfaceCompletionHandler interface, IActivateAudioInterfaceCompletionHandler interface [Core Audio],ActivateCompleted method, IActivateAudioInterfaceCompletionHandler.ActivateCompleted, IActivateAudioInterfaceCompletionHandler::ActivateCompleted, coreaudio.iactivateaudiointerfacecompletionhandler_activatecompleted, mmdeviceapi/IActivateAudioInterfaceCompletionHandler::ActivateCompleted
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
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
 - IActivateAudioInterfaceCompletionHandler.ActivateCompleted
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IActivateAudioInterfaceCompletionHandler::ActivateCompleted


## -description


Indicates that activation of a <a href="https://msdn.microsoft.com/452b9725-b0b9-4888-bbb5-a23e0067e840">WASAPI</a> interface is complete and results are available.


## -parameters




### -param activateOperation [in]

An interface representing the asynchronous operation of activating the requested <b>WASAPI</b> interface 


## -returns



The function returns an <b>HRESULT</b>. Possible values include, but are not limited to, those in the following table.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The function succeeded.

</td>
</tr>
</table>
 




## -remarks



An application implements this method if it calls the <a href="https://msdn.microsoft.com/7BAFD9DB-DCD7-4093-A24B-9A8556C6C45B">ActivateAudioInterfaceAsync</a> function. When Windows calls this method, the results of the activation are available. The application can then retrieve the results by calling the <a href="https://msdn.microsoft.com/4dd0e555-ee62-40f6-9b4a-57c6063981bf">GetActivateResult</a> method of the <a href="https://msdn.microsoft.com/43b25a67-d9a8-4749-a654-c7310039c553">IActivateAudioInterfaceAsyncOperation</a> interface, passed through the <i>activateOperation</i> parameter. 




## -see-also




<a href="https://msdn.microsoft.com/7BAFD9DB-DCD7-4093-A24B-9A8556C6C45B">ActivateAudioInterfaceAsync</a>



<a href="https://msdn.microsoft.com/04ff7cbb-fd33-40d9-9c11-4f716c6423b0">IActivateAudioInterfaceCompletionHandler</a>
 

 

