---
UID: NF:mmdeviceapi.IMMDevice.Activate
title: IMMDevice::Activate
author: windows-sdk-content
description: The Activate method creates a COM object with the specified interface.
old-location: coreaudio\immdevice_activate.htm
tech.root: CoreAudio
ms.assetid: 12e4a117-1fa3-49c8-949b-8973edf7e12e
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: Activate, Activate method [Core Audio], Activate method [Core Audio],IMMDevice interface, IMMDevice interface [Core Audio],Activate method, IMMDevice.Activate, IMMDevice::Activate, IMMDeviceActivate, coreaudio.immdevice_activate, mmdeviceapi/IMMDevice::Activate
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: mmdeviceapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
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
 - Mmdeviceapi.h
api_name:
 - IMMDevice.Activate
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMMDevice::Activate


## -description



The <b>Activate</b> method creates a COM object with the specified interface.




## -parameters




### -param iid [in]

The interface identifier. This parameter is a reference to a GUID that identifies the interface that the caller requests be activated. The caller will use this interface to communicate with the COM object. Set this parameter to one of the following interface identifiers:

IID_IAudioClient

IID_IAudioEndpointVolume

IID_IAudioMeterInformation

IID_IAudioSessionManager

IID_IAudioSessionManager2

IID_IBaseFilter

IID_IDeviceTopology

IID_IDirectSound

IID_IDirectSound8

IID_IDirectSoundCapture

IID_IDirectSoundCapture8

IID_IMFTrustedOutput

IID_ISpatialAudioClient

IID_ISpatialAudioMetadataClient

For more information, see Remarks.


### -param dwClsCtx [in]

The execution context in which the code that manages the newly created object will run. The caller can restrict the context by setting this parameter to the bitwise <b>OR</b> of one or more <b>CLSCTX</b> enumeration values. Alternatively, the client can avoid imposing any context restrictions by specifying CLSCTX_ALL. For more information about <b>CLSCTX</b>, see the Windows SDK documentation.


### -param pActivationParams [in]

Set to <b>NULL</b> to activate an <a href="https://msdn.microsoft.com/5088a3f1-5001-4ed9-a495-9e91df613ab0">IAudioClient</a>, <a href="https://msdn.microsoft.com/5e3e7ffc-8822-4b1b-b9af-206ec1e767e2">IAudioEndpointVolume</a>, <a href="https://msdn.microsoft.com/eff1c1cd-792b-489a-8381-4b783c57f005">IAudioMeterInformation</a>, <a href="https://msdn.microsoft.com/606b0a42-d1d1-4196-911f-5b095bf56c4e">IAudioSessionManager</a>, or <a href="https://msdn.microsoft.com/1b509f69-6277-40c0-a293-02afc30d464a">IDeviceTopology</a> interface on an audio endpoint device. When activating an <b>IBaseFilter</b>, <b>IDirectSound</b>, <b>IDirectSound8</b>, <b>IDirectSoundCapture</b>, or <b>IDirectSoundCapture8</b> interface on the device, the caller can specify a pointer to a <b>PROPVARIANT</b> structure that contains stream-initialization information. For more information, see Remarks.


### -param ppInterface [out]

Pointer to a pointer variable into which the method writes the address of the interface specified by parameter <i>iid</i>. Through this method, the caller obtains a counted reference to the interface. The caller is responsible for releasing the interface, when it is no longer needed, by calling the interface's <b>Release</b> method. If the <b>Activate</b> call fails,  <i>*ppInterface</i> is <b>NULL</b>.


## -returns



If the method succeeds, it returns S_OK. If it fails, possible return codes include, but are not limited to, the values shown in the following table.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_NOINTERFACE</b></dt>
</dl>
</td>
<td width="60%">
The object does not support the requested interface type.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
Parameter <i>ppInterface</i> is <b>NULL</b>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
The <i>pActivationParams</i> parameter must be <b>NULL</b> for the specified interface; or <i>pActivationParams</i> points to invalid data.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
Out of memory.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>AUDCLNT_E_DEVICE_INVALIDATED</b></dt>
</dl>
</td>
<td width="60%">
The user has removed either the audio endpoint device or the adapter device that the endpoint device connects to.

</td>
</tr>
</table>
 




## -remarks



This method creates a COM object with an interface that is specified by the <i>iid</i> parameter. The method is similar to the Windows <b>CoCreateInstance</b> function, except that the caller does not supply a CLSID as a parameter. For more information about <b>CoCreateInstance</b>, see the Windows SDK documentation.

A client can call the <b>Activate</b> method of the <b>IMMDevice</b> interface for a particular audio endpoint device to obtain a counted reference to an interface on that device. The method can activate the following interfaces:

<ul>
<li>
<a href="https://msdn.microsoft.com/5088a3f1-5001-4ed9-a495-9e91df613ab0">IAudioClient</a>
</li>
<li>
<a href="https://msdn.microsoft.com/5e3e7ffc-8822-4b1b-b9af-206ec1e767e2">IAudioEndpointVolume</a>
</li>
<li>
<a href="https://msdn.microsoft.com/eff1c1cd-792b-489a-8381-4b783c57f005">IAudioMeterInformation</a>
</li>
<li>
<a href="https://msdn.microsoft.com/606b0a42-d1d1-4196-911f-5b095bf56c4e">IAudioSessionManager</a>
</li>
<li>
<a href="https://msdn.microsoft.com/476dac90-d0c4-499c-973e-33ea55546659">IAudioSessionManager2</a>
</li>
<li>IBaseFilter
          </li>
<li>
<a href="https://msdn.microsoft.com/1b509f69-6277-40c0-a293-02afc30d464a">IDeviceTopology</a>
</li>
<li>IDirectSound
          </li>
<li>IDirectSound8
          </li>
<li>IDirectSoundCapture
          </li>
<li>IDirectSoundCapture8
          </li>
<li>IMFTrustedOutput</li>
</ul>
To obtain the interface ID for an interface, use the <b>__uuidof</b> operator. For example, the interface ID of <b>IAudioCaptureClient</b> is defined as follows:

<pre class="syntax" xml:space="preserve"><code>
const IID IID_IAudioClient  __uuidof(IAudioCaptureClient)
</code></pre>
For information about the <b>__uuidof</b> operator, see the Windows SDK documentation. For information about <b>IBaseFilter</b>, <b>IDirectSound</b>, <b>IDirectSound8</b>, <b>IDirectSoundCapture</b>,  <b>IDirectSoundCapture8</b>, and <b>IMFTrustedOutput</b> see the Windows SDK documentation.

The <i>pActivationParams</i> parameter should be <b>NULL</b> for an <b>Activate</b> call to create an <b>IAudioClient</b>, <b>IAudioEndpointVolume</b>, <b>IAudioMeterInformation</b>, <b>IAudioSessionManager</b>, or <b>IDeviceTopology</b> interface for an audio endpoint device.

For an <b>Activate</b> call to create an <b>IBaseFilter</b>, <b>IDirectSound</b>, <b>IDirectSound8</b>, <b>IDirectSoundCapture</b>, or <b>IDirectSoundCapture8</b> interface, the caller can, as an option, specify a non-<b>NULL</b> value for <i>pActivationParams</i>. In this case, <i>pActivationParams</i> points to a <b>PROPVARIANT</b> structure that contains stream-initialization information. Set the <b>vt</b> member of the structure to VT_BLOB. Set the <b>blob.pBlobData</b> member to point to a <a href="https://msdn.microsoft.com/d8d16c1c-5306-42a7-885b-4e1c5ee7634d">DIRECTX_AUDIO_ACTIVATION_PARAMS</a> structure that contains an audio session GUID and stream-initialization flags. Set the <b>blob.cbSize</b> member to <b>sizeof</b>(<b>DIRECTX_AUDIO_ACTIVATION_PARAMS</b>). For a code example, see <a href="https://msdn.microsoft.com/54f42bda-b4a0-465c-9ce6-9102d2908776">Device Roles for DirectShow Applications</a>. For more information about <b>PROPVARIANT</b>, see the Windows SDK documentation.

An <b>IBaseFilter</b>, <b>IDirectSound</b>, <b>IDirectSound8</b>, <b>IDirectSoundCapture</b>, or <b>IDirectSoundCapture8</b> interface instance that is created by the <b>Activate</b> method encapsulates a stream on the audio endpoint device. During the <b>Activate</b> call, the DirectSound system module creates the stream by calling the <a href="https://msdn.microsoft.com/eb778503-06f8-4705-9f8d-9a4fd886ae27">IAudioClient::Initialize</a> method. If <i>pActivationParams</i> is non-<b>NULL</b>, DirectSound supplies the audio session GUID and stream-initialization flags from the <b>DIRECTX_AUDIO_ACTIVATION_PARAMS</b> structure as input parameters to the <b>Initialize</b> call. If <i>pActivationParams</i> is <b>NULL</b>, DirectSound sets the <b>Initialize</b> method's <i>AudioSessionGuid</i> and <i>StreamFlags</i> parameters to their respective default values, <b>NULL</b> and 0. These values instruct the method to assign the stream to the process-specific session that is identified by the session GUID value GUID_NULL.

<b>Activate</b> can activate an <b>IDirectSound</b> or <b>IDirectSound8</b> interface only on a rendering endpoint device. It can activate an <b>IDirectSoundCapture</b> or <b>IDirectSoundCapture8</b> interface only on a capture endpoint device. An <b>Activate</b> call to activate an <b>IDirectSound</b> or <b>IDirectSoundCapture8</b> interface on a capture device or an <b>IDirectSoundCapture</b> or <b>IDirectSoundCapture8</b> interface on a rendering device fails and returns error code E_NOINTERFACE.

In Windows 7, a client can call <b>IMMDevice::Activate</b> and specify, <b>IID_IMFTrustedOutput</b>, to create an output trust authorities (OTA) object and retrieve a pointer to the object's <a href="https://msdn.microsoft.com/14342d8b-3c76-4c13-8cbe-a60bb66084c8">IMFTrustedOutput</a> interface. OTAs can operate inside or outside the Media Foundation's protected media path (PMP) and send content outside the Media Foundation pipeline. If the caller is outside PMP, then the OTA may not operate in the PMP,  and the protection settings are less robust. For information about using protected objects for audio and example code, see <a href="https://msdn.microsoft.com/27a50026-9e48-48b1-9249-7528a97333c9">Protected User Mode Audio (PUMA)</a>.

For general information about protected objects and <a href="https://msdn.microsoft.com/14342d8b-3c76-4c13-8cbe-a60bb66084c8">IMFTrustedOutput</a>, see "Protected Media Path" in  Media Foundation documentation.

<div class="alert"><b>Note</b>  When using the <a href="https://msdn.microsoft.com/950778D4-79FE-4222-951F-5A456A633124">ISpatialAudioClient</a> interfaces on an Xbox One Development Kit (XDK) title, you must first call <b>EnableSpatialAudio</b> before calling <a href="https://msdn.microsoft.com/ebdd2dcd-82c5-423f-a85d-04388f5078ec">IMMDeviceEnumerator::EnumAudioEndpoints</a> or <a href="https://msdn.microsoft.com/96776d2a-27b7-490a-b3a8-04782ec34f91">IMMDeviceEnumerator::GetDefaultAudioEndpoint</a>. Failure to do so will result in an E_NOINTERFACE error being returned from the call to Activate. <b>EnableSpatialAudio</b> is only available for XDK titles, and does not need to be called for Universal Windows Platform apps running on Xbox One, nor for any non-Xbox One devices.</div>
<div> </div>
For code examples that call the <b>Activate</b> method, see the following topics:

<ul>
<li>
<a href="https://msdn.microsoft.com/00bfcfd1-6592-43e3-90ad-730c92aa4cd3">Rendering a Stream</a>
</li>
<li>
<a href="https://msdn.microsoft.com/5ac421e5-74a4-40e8-af6f-a99a05ebc3e0">Device Topologies</a>
</li>
<li>
<a href="https://msdn.microsoft.com/72bf9164-96c6-4543-b858-19480b032fdb">Using the IKsControl Interface to Access Audio Properties</a>
</li>
<li>
<a href="https://msdn.microsoft.com/91a93b79-2563-4b25-af5d-ca5f7d35d77b">Audio Events for Legacy Audio Applications</a>
</li>
<li>
<a href="https://msdn.microsoft.com/C99C342E-0BD9-486A-92AA-F8DCB72C1B00">Render Spatial Sound Using Spatial Audio Objects</a>
</li>
</ul>



## -see-also




<a href="https://msdn.microsoft.com/5088a3f1-5001-4ed9-a495-9e91df613ab0">IAudioClient Interface</a>



<a href="https://msdn.microsoft.com/5e3e7ffc-8822-4b1b-b9af-206ec1e767e2">IAudioEndpointVolume Interface</a>



<a href="https://msdn.microsoft.com/eff1c1cd-792b-489a-8381-4b783c57f005">IAudioMeterInformation Interface</a>



<a href="https://msdn.microsoft.com/606b0a42-d1d1-4196-911f-5b095bf56c4e">IAudioSessionManager Interface</a>



<a href="https://msdn.microsoft.com/1b509f69-6277-40c0-a293-02afc30d464a">IDeviceTopology Interface</a>



<a href="https://msdn.microsoft.com/12b05e7e-81b2-49fd-bb9f-d5ad3315c580">IMMDevice Interface</a>
 

 

