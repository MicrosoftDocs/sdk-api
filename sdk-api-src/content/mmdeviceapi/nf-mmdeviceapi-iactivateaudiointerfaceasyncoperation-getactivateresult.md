---
UID: NF:mmdeviceapi.IActivateAudioInterfaceAsyncOperation.GetActivateResult
title: IActivateAudioInterfaceAsyncOperation::GetActivateResult (mmdeviceapi.h)
description: Gets the results of an asynchronous activation of a WASAPI interface initiated by an application calling the ActivateAudioInterfaceAsync function.
helpviewer_keywords: ["GetActivateResult","GetActivateResult method [Core Audio]","GetActivateResult method [Core Audio]","IActivateAudioInterfaceAsyncOperation interface","IActivateAudioInterfaceAsyncOperation interface [Core Audio]","GetActivateResult method","IActivateAudioInterfaceAsyncOperation.GetActivateResult","IActivateAudioInterfaceAsyncOperation::GetActivateResult","coreaudio.iactivateaudiointerfaceasyncoperation_getactivateresult","mmdeviceapi/IActivateAudioInterfaceAsyncOperation::GetActivateResult"]
old-location: coreaudio\iactivateaudiointerfaceasyncoperation_getactivateresult.htm
tech.root: CoreAudio
ms.assetid: 4dd0e555-ee62-40f6-9b4a-57c6063981bf
ms.date: 12/05/2018
ms.keywords: GetActivateResult, GetActivateResult method [Core Audio], GetActivateResult method [Core Audio],IActivateAudioInterfaceAsyncOperation interface, IActivateAudioInterfaceAsyncOperation interface [Core Audio],GetActivateResult method, IActivateAudioInterfaceAsyncOperation.GetActivateResult, IActivateAudioInterfaceAsyncOperation::GetActivateResult, coreaudio.iactivateaudiointerfaceasyncoperation_getactivateresult, mmdeviceapi/IActivateAudioInterfaceAsyncOperation::GetActivateResult
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
 - IActivateAudioInterfaceAsyncOperation::GetActivateResult
 - mmdeviceapi/IActivateAudioInterfaceAsyncOperation::GetActivateResult
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
 - IActivateAudioInterfaceAsyncOperation.GetActivateResult
---

# IActivateAudioInterfaceAsyncOperation::GetActivateResult


## -description

Gets the results of an asynchronous activation of a <a href="/windows/desktop/CoreAudio/wasapi">WASAPI</a> interface initiated by an application calling the <a href="/windows/desktop/api/mmdeviceapi/nf-mmdeviceapi-activateaudiointerfaceasync">ActivateAudioInterfaceAsync</a> function.

## -parameters

### -param activateResult [out]

### -param activatedInterface [out]

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
<dt><b>E_ILLEGAL_METHOD_CALL</b></dt>
</dl>
</td>
<td width="60%">
The method was called before the asynchronous operation was complete. 

</td>
</tr>
</table>

## -remarks

An application calls this method after Windows calls the <a href="/windows/desktop/api/mmdeviceapi/nf-mmdeviceapi-iactivateaudiointerfacecompletionhandler-activatecompleted">ActivateCompleted</a> method of the application’s <a href="/windows/desktop/api/mmdeviceapi/nn-mmdeviceapi-iactivateaudiointerfacecompletionhandler">IActivateAudioInterfaceCompletionHandler</a> interface.

The result code returned through <i>activateResult</i> may depend on the requested interface. For additional information, see <a href="/windows/desktop/api/mmdeviceapi/nf-mmdeviceapi-immdevice-activate">IMMDevice::Activate</a>. A result code of <b>E_ACCESSDENIED</b> might indicate that the user has not given consent to access the device in a manner required by the requested <a href="/windows/desktop/CoreAudio/wasapi">WASAPI</a> interface. 

The returned <i>activatedInterface</i> may be <b>NULL</b> if <i>activateResult</i> is not a success code.

## -see-also

<a href="/windows/desktop/api/mmdeviceapi/nf-mmdeviceapi-activateaudiointerfaceasync">ActivateAudioInterfaceAsync</a>



<a href="/windows/desktop/api/mmdeviceapi/nn-mmdeviceapi-iactivateaudiointerfaceasyncoperation">IActivateAudioInterfaceAsyncOperation</a>