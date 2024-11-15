---
UID: NF:mmdeviceapi.ActivateAudioInterfaceAsync
title: ActivateAudioInterfaceAsync function (mmdeviceapi.h)
description: Enables Windows Store apps to access preexisting Component Object Model (COM) interfaces in the WASAPI family.
helpviewer_keywords: ["ActivateAudioInterfaceAsync","ActivateAudioInterfaceAsync function [Core Audio]","coreaudio.activateaudiointerfaceasync","mmdeviceapi/ActivateAudioInterfaceAsync"]
old-location: coreaudio\activateaudiointerfaceasync.htm
tech.root: CoreAudio
ms.assetid: 7BAFD9DB-DCD7-4093-A24B-9A8556C6C45B
ms.date: 12/05/2018
ms.keywords: ActivateAudioInterfaceAsync, ActivateAudioInterfaceAsync function [Core Audio], coreaudio.activateaudiointerfaceasync, mmdeviceapi/ActivateAudioInterfaceAsync
req.header: mmdeviceapi.h
req.include-header: Mmdevapi.idl
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2012 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Mmdevapi.lib
req.dll: Mmdevapi.dll
req.irql: No
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ActivateAudioInterfaceAsync
 - mmdeviceapi/ActivateAudioInterfaceAsync
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Mmdevapi.dll
api_name:
 - ActivateAudioInterfaceAsync
---

# ActivateAudioInterfaceAsync function


## -description

Enables Windows Store apps to access preexisting Component Object Model (COM) interfaces in the <a href="/windows/desktop/CoreAudio/wasapi">WASAPI</a> family.

## -parameters

### -param deviceInterfacePath [in]

A device interface ID for an audio device. This is normally retrieved from a <a href="/uwp/api/windows.devices.enumeration.deviceinformation">DeviceInformation</a> object or one of the methods of the <a href="/uwp/api/windows.media.devices.mediadevice">MediaDevice</a> class. 

The GUIDs <a href="/windows/desktop/CoreAudio/devinterface-xxx-guids">DEVINTERFACE_AUDIO_CAPTURE</a>  and <b>DEVINTERFACE_AUDIO_RENDER</b>  represent the default audio capture and render device respectively. Call <a href="/windows/desktop/api/combaseapi/nf-combaseapi-stringfromiid">StringFromIID</a> to convert either of these GUIDs to an <b>LPCWSTR</b> to use for this argument.

Specify **AUDIOCLIENT_ACTIVATION_TYPE_PROCESS_LOOPBACK** to activate the audio interface for process loopback capture. For sample code that demonstrates the process loopback capture scenario, see the [Application Loopback API Capture Sample](https://docs.microsoft.com/en-us/samples/microsoft/windows-classic-samples/applicationloopbackaudio-sample/).

### -param riid [in]

The IID of a COM interface in the <a href="/windows/desktop/CoreAudio/wasapi">WASAPI</a> family, such as <a href="/windows/desktop/api/audioclient/nn-audioclient-iaudioclient">IAudioClient</a>.

### -param activationParams [in]

Interface-specific activation parameters. For more information, see the <i>pActivationParams</i> parameter in <a href="/windows/desktop/api/mmdeviceapi/nf-mmdeviceapi-immdevice-activate">IMMDevice::Activate</a>.

Starting with Windows 10 Build 20438, you can specify [AUDIOCLIENT_ACTIVATION_PARAMS](/windows/desktop/api/audioclientactivationparams/ns-audioclientactivationparams-audioclient_activation_params) to activate the interface to include or exclude audio streams associated with a specified process ID.

### -param completionHandler [in]

An interface implemented by the caller that is called by Windows when the result of the activation procedure is available.

### -param activationOperation

Returns an <a href="/windows/desktop/api/mmdeviceapi/nn-mmdeviceapi-iactivateaudiointerfaceasyncoperation">IActivateAudioInterfaceAsyncOperation</a> interface that represents the asynchronous operation of activating the requested <b>WASAPI</b> interface.

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
The underlying object and asynchronous operation were created successfully.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_ILLEGAL_METHOD_CALL </b></dt>
</dl>
</td>
<td width="60%">
On versions of Windows previous to Windows 10, this error may result if the function is called from an incorrect COM apartment, or if the passed <a href="/windows/desktop/api/mmdeviceapi/nn-mmdeviceapi-iactivateaudiointerfacecompletionhandler">IActivateAudioInterfaceCompletionHandler</a> is not implemented on an agile object (aggregating a free-threaded marshaler).

</td>
</tr>
</table>

## -remarks

This function enables Windows Store apps to  activate certain <a href="/windows/desktop/CoreAudio/wasapi">WASAPI</a> COM interfaces after using Windows Runtime APIs in the <b>Windows.Devices</b> and <a href="/uwp/api/windows.media.devices">Windows.Media.Devices</a> namespaces to select an audio device.  

For many implementations, an application must call this function from the main UI thread to activate a COM interface in the <a href="/windows/desktop/CoreAudio/wasapi">WASAPI</a> family so that the system can show a dialog to the user. The application passes an <a href="/windows/desktop/api/mmdeviceapi/nn-mmdeviceapi-iactivateaudiointerfacecompletionhandler">IActivateAudioInterfaceCompletionHandler</a> callback COM interface through <i>completionHandler</i>. Windows calls a method in the application’s <b>IActivateAudioInterfaceCompletionHandler</b> interface from a worker thread in the COM Multi-threaded Apartment (MTA) when the activation results are available. The application can then call a method in the <a href="/windows/desktop/api/mmdeviceapi/nn-mmdeviceapi-iactivateaudiointerfaceasyncoperation">IActivateAudioInterfaceAsyncOperation</a> interface  to retrieve the result code and the requested <b>WASAPI</b> interface. There are some activations that are explicitly safe and therefore don't require that this function be called from the main UI thread. These explicitly safe activations include:

<ul>
<li>Calling <b>ActivateAudioInterfaceAsync</b> with a <i>deviceInterfacePath</i> that specifies an audio render device and an <i>riid</i> that specifies the <a href="/windows/desktop/api/audioclient/nn-audioclient-iaudioclient">IAudioClient</a> interface.</li>
<li>Calling <b>ActivateAudioInterfaceAsync</b> with a <i>deviceInterfacePath</i> that specifies an audio render device and an <i>riid</i> that specifies the <a href="/windows/desktop/api/endpointvolume/nn-endpointvolume-iaudioendpointvolume">IAudioEndpointVolume</a> interface.</li>
<li>Calling <b>ActivateAudioInterfaceAsync</b> from a session 0 service. For more information, see <a href="/windows/desktop/services/services">Services</a>.</li>
</ul>
Windows holds a reference to the application's <a href="/windows/desktop/api/mmdeviceapi/nn-mmdeviceapi-iactivateaudiointerfacecompletionhandler">IActivateAudioInterfaceCompletionHandler</a> interface until the operation is complete and the application releases the <a href="/windows/desktop/api/mmdeviceapi/nn-mmdeviceapi-iactivateaudiointerfaceasyncoperation">IActivateAudioInterfaceAsyncOperation</a> interface. 

<div class="alert"><b>Important</b>  <p class="note">Applications must not free the object implementing the <b>IActivateAudioInterfaceCompletionHandler</b> until the completion handler callback has executed. 

</div>
<div> </div>
Depending on which <a href="/windows/desktop/CoreAudio/wasapi">WASAPI</a> interface is activated, this function may display a consent prompt the first time it is called. For example, when the application calls this function to activate <a href="/windows/desktop/api/audioclient/nn-audioclient-iaudioclient">IAudioClient</a> to access a microphone, the purpose of the consent prompt is to get the user's permission for the app to access the microphone. For more information about the consent prompt, see <a href="/windows/uwp/security/index">Guidelines for devices that access personal data</a>.


<b>ActivateAudioInterfaceAsync</b> must be called on the main UI thread so that the consent prompt can be shown. If the consent prompt can’t be shown, the user can’t grant device access to the app.

On versions of Windows previous to Windows 10, <b>ActivateAudioInterfaceAsync</b> must be called on a thread in a COM Single-Threaded Apartment (STA), when opening a device for audio capture. The <i>completionHandler</i> that is passed into <b>ActivateAudioInterfaceAsync</b> needs to implement <a href="/windows/desktop/api/objidl/nn-objidl-iagileobject">IAgileObject</a> to ensure that there is no deadlock when the <i>completionHandler</i> is called from the MTA. Otherwise, an <b>E_ILLEGAL_METHOD_CALL</b> will occur.

## -see-also

<a href="/windows/desktop/CoreAudio/core-audio-functions">Core Audio Functions</a>



<a href="/windows/desktop/api/mmdeviceapi/nn-mmdeviceapi-iactivateaudiointerfaceasyncoperation">IActivateAudioInterfaceAsyncOperation</a>



<a href="/windows/desktop/api/mmdeviceapi/nn-mmdeviceapi-iactivateaudiointerfacecompletionhandler">IActivateAudioInterfaceCompletionHandler</a>
