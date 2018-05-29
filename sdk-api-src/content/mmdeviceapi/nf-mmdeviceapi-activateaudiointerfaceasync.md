---
UID: NF:mmdeviceapi.ActivateAudioInterfaceAsync
title: ActivateAudioInterfaceAsync function
author: windows-sdk-content
description: Enables Windows Store apps to access preexisting Component Object Model (COM) interfaces in the WASAPI family.
old-location: coreaudio\activateaudiointerfaceasync.htm
old-project: CoreAudio
ms.assetid: 7BAFD9DB-DCD7-4093-A24B-9A8556C6C45B
ms.author: windowssdkdev
ms.date: 05/09/2018
ms.keywords: ActivateAudioInterfaceAsync, ActivateAudioInterfaceAsync function [Core Audio], coreaudio.activateaudiointerfaceasync, mmdeviceapi/ActivateAudioInterfaceAsync
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: mmdeviceapi.h
req.include-header: Mmdevapi.idl
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
req.typenames: EndpointFormFactor
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	Mmdevapi.dll
api_name:
-	ActivateAudioInterfaceAsync
product: Windows
targetos: Windows
req.lib: Mmdevapi.lib
req.dll: Mmdevapi.dll
req.irql: No
req.product: GDI+ 1.1
---

# ActivateAudioInterfaceAsync function


## -description


Enables Windows Store apps to access preexisting Component Object Model (COM) interfaces in the <a href="https://msdn.microsoft.com/452b9725-b0b9-4888-bbb5-a23e0067e840">WASAPI</a> family. 


## -parameters




### -param deviceInterfacePath [in]

A device interface ID for an audio device. This is normally retrieved from a <a href="https://msdn.microsoft.com/8a53fdec-5fbe-4958-806a-4f840e6de6b5">DeviceInformation</a> object or one of the methods of the <a href="https://msdn.microsoft.com/def5c669-d6bd-440c-97aa-3c154375aa7e">MediaDevice</a> class. 

The GUIDs <a href="https://msdn.microsoft.com/2503463B-D7C6-4C82-8421-424D79FD1C2A">DEVINTERFACE_AUDIO_CAPTURE</a>  and <b>DEVINTERFACE_AUDIO_RENDER</b>  represent the default audio capture and render device respectively. Call <a href="https://msdn.microsoft.com/92e59631-0675-4bca-bcd4-a1f83ab6ec8a">StringFromIID</a> to convert either of these GUIDs to an <b>LPCWSTR</b> to use for this argument.


### -param riid [in]

The IID of a COM interface in the <a href="https://msdn.microsoft.com/452b9725-b0b9-4888-bbb5-a23e0067e840">WASAPI</a> family, such as <a href="https://msdn.microsoft.com/5088a3f1-5001-4ed9-a495-9e91df613ab0">IAudioClient</a>.


### -param activationParams [in]

Interface-specific activation parameters. For more information, see the <i>pActivationParams</i> parameter in <a href="https://msdn.microsoft.com/12e4a117-1fa3-49c8-949b-8973edf7e12e">IMMDevice::Activate</a>. 


### -param completionHandler [in]

An interface implemented by the caller that is called by Windows when the result of the activation procedure is available.


### -param activationOperation

TBD




#### - createAsync

Returns an <a href="https://msdn.microsoft.com/43b25a67-d9a8-4749-a654-c7310039c553">IActivateAudioInterfaceAsyncOperation</a> interface that represents the asynchronous operation of activating the requested <b>WASAPI</b> interface.


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
This error may result if the function is called from an incorrect COM apartment, or if the passed <a href="https://msdn.microsoft.com/04ff7cbb-fd33-40d9-9c11-4f716c6423b0">IActivateAudioInterfaceCompletionHandler</a> is not implemented on an agile object (aggregating a free-threaded marshaler).

</td>
</tr>
</table>
 




## -remarks



This function enables Windows Store apps to  activate certain <a href="https://msdn.microsoft.com/452b9725-b0b9-4888-bbb5-a23e0067e840">WASAPI</a> COM interfaces after using Windows Runtime APIs in the <b>Windows.Devices</b> and <a href="https://msdn.microsoft.com/bc763133-e3cf-4c81-82dc-2e3868f85dde">Windows.Media.Devices</a> namespaces to select an audio device.  

An application must call this function from the main UI thread to activate a COM interface in the <a href="https://msdn.microsoft.com/452b9725-b0b9-4888-bbb5-a23e0067e840">WASAPI</a> family. The application passes an <a href="https://msdn.microsoft.com/04ff7cbb-fd33-40d9-9c11-4f716c6423b0">IActivateAudioInterfaceCompletionHandler</a> callback COM interface through <i>completionHandler</i>. Windows calls a method in the application’s <b>IActivateAudioInterfaceCompletionHandler</b> interface from a worker thread in the COM Multi-threaded Apartment (MTA) when the activation results are available. The application can then call a method in the <a href="https://msdn.microsoft.com/43b25a67-d9a8-4749-a654-c7310039c553">IActivateAudioInterfaceAsyncOperation</a> interface  to retrieve the result code and the requested <b>WASAPI</b> interface.

Windows holds a reference to the application's <a href="https://msdn.microsoft.com/04ff7cbb-fd33-40d9-9c11-4f716c6423b0">IActivateAudioInterfaceCompletionHandler</a> interface until the operation is complete and the application releases the <a href="https://msdn.microsoft.com/43b25a67-d9a8-4749-a654-c7310039c553">IActivateAudioInterfaceAsyncOperation</a> interface. 

<div class="alert"><b>Important</b>  <p class="note">Applications must not free the object implementing the <b>IActivateAudioInterfaceCompletionHandler</b> until the completion handler callback has executed. 

</div>
<div> </div>
Depending on which <a href="https://msdn.microsoft.com/452b9725-b0b9-4888-bbb5-a23e0067e840">WASAPI</a> interface is activated, this function may display a consent prompt the first time it is called. For example, when the application calls this function to activate <a href="https://msdn.microsoft.com/5088a3f1-5001-4ed9-a495-9e91df613ab0">IAudioClient</a> to access a microphone, the purpose of the consent prompt is to get the user's permission for the app to access the microphone. For more information about the consent prompt, see <a href="https://msdn.microsoft.com/83BDE569-9464-49FD-9CED-E280C4AF96EF">Guidelines for devices that access personal data</a>.


<b>ActivateAudioInterfaceAsync</b> must be called on the main UI thread so that the consent prompt can be shown. If the consent prompt can’t be shown, the user can’t grant device access to the app.

<b>ActivateAudioInterfaceAsync</b> must be called on a thread in a COM Single-Threaded Apartment (STA). The <i>completionHandler</i> that is passed into <b>ActivateAudioInterfaceAsync</b> needs to implement <a href="https://msdn.microsoft.com/787A22DE-AEAB-4570-BB97-C49D656E5D40">IAgileObject</a> to ensure that there is no deadlock when the <i>completionHandler</i> is called from the MTA. Otherwise, an <b>E_ILLEGAL_METHOD_CALL</b> will occur.




## -see-also




<a href="https://msdn.microsoft.com/96F0AE0B-B357-4236-8B47-33353927D3C8">Core Audio Functions</a>



<a href="https://msdn.microsoft.com/43b25a67-d9a8-4749-a654-c7310039c553">IActivateAudioInterfaceAsyncOperation</a>



<a href="https://msdn.microsoft.com/04ff7cbb-fd33-40d9-9c11-4f716c6423b0">IActivateAudioInterfaceCompletionHandler</a>
 

 

