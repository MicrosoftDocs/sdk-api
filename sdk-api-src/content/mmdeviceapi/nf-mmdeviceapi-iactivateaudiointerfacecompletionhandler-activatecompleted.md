---
UID: NF:mmdeviceapi.IActivateAudioInterfaceCompletionHandler.ActivateCompleted
title: IActivateAudioInterfaceCompletionHandler::ActivateCompleted (mmdeviceapi.h)
description: Indicates that activation of a WASAPI interface is complete and results are available.
helpviewer_keywords: ["ActivateCompleted","ActivateCompleted method [Core Audio]","ActivateCompleted method [Core Audio]","IActivateAudioInterfaceCompletionHandler interface","IActivateAudioInterfaceCompletionHandler interface [Core Audio]","ActivateCompleted method","IActivateAudioInterfaceCompletionHandler.ActivateCompleted","IActivateAudioInterfaceCompletionHandler::ActivateCompleted","coreaudio.iactivateaudiointerfacecompletionhandler_activatecompleted","mmdeviceapi/IActivateAudioInterfaceCompletionHandler::ActivateCompleted"]
old-location: coreaudio\iactivateaudiointerfacecompletionhandler_activatecompleted.htm
tech.root: CoreAudio
ms.assetid: f434db12-ab8e-40ca-8a55-b02f28ea5575
ms.date: 12/05/2018
ms.keywords: ActivateCompleted, ActivateCompleted method [Core Audio], ActivateCompleted method [Core Audio],IActivateAudioInterfaceCompletionHandler interface, IActivateAudioInterfaceCompletionHandler interface [Core Audio],ActivateCompleted method, IActivateAudioInterfaceCompletionHandler.ActivateCompleted, IActivateAudioInterfaceCompletionHandler::ActivateCompleted, coreaudio.iactivateaudiointerfacecompletionhandler_activatecompleted, mmdeviceapi/IActivateAudioInterfaceCompletionHandler::ActivateCompleted
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IActivateAudioInterfaceCompletionHandler::ActivateCompleted
 - mmdeviceapi/IActivateAudioInterfaceCompletionHandler::ActivateCompleted
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mmdeviceapi.h
api_name:
 - IActivateAudioInterfaceCompletionHandler.ActivateCompleted
---

# IActivateAudioInterfaceCompletionHandler::ActivateCompleted


## -description

Indicates that activation of a <a href="/windows/desktop/CoreAudio/wasapi">WASAPI</a> interface is complete and results are available.

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

An application implements this method if it calls the <a href="/windows/desktop/api/mmdeviceapi/nf-mmdeviceapi-activateaudiointerfaceasync">ActivateAudioInterfaceAsync</a> function. When Windows calls this method, the results of the activation are available. The application can then retrieve the results by calling the <a href="/windows/desktop/api/mmdeviceapi/nf-mmdeviceapi-iactivateaudiointerfaceasyncoperation-getactivateresult">GetActivateResult</a> method of the <a href="/windows/desktop/api/mmdeviceapi/nn-mmdeviceapi-iactivateaudiointerfaceasyncoperation">IActivateAudioInterfaceAsyncOperation</a> interface, passed through the <i>activateOperation</i> parameter.

## -see-also

<a href="/windows/desktop/api/mmdeviceapi/nf-mmdeviceapi-activateaudiointerfaceasync">ActivateAudioInterfaceAsync</a>



<a href="/windows/desktop/api/mmdeviceapi/nn-mmdeviceapi-iactivateaudiointerfacecompletionhandler">IActivateAudioInterfaceCompletionHandler</a>