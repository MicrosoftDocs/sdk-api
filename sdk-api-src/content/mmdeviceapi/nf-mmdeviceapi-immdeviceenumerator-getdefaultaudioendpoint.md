---
UID: NF:mmdeviceapi.IMMDeviceEnumerator.GetDefaultAudioEndpoint
title: IMMDeviceEnumerator::GetDefaultAudioEndpoint
author: windows-sdk-content
description: The GetDefaultAudioEndpoint method retrieves the default audio endpoint for the specified data-flow direction and role.
old-location: coreaudio\immdeviceenumerator_getdefaultaudioendpoint.htm
old-project: CoreAudio
ms.assetid: 96776d2a-27b7-490a-b3a8-04782ec34f91
ms.author: windowssdkdev
ms.date: 08/14/2018
ms.keywords: GetDefaultAudioEndpoint, GetDefaultAudioEndpoint method [Core Audio], GetDefaultAudioEndpoint method [Core Audio],IMMDeviceEnumerator interface, IMMDeviceEnumerator interface [Core Audio],GetDefaultAudioEndpoint method, IMMDeviceEnumerator.GetDefaultAudioEndpoint, IMMDeviceEnumerator::GetDefaultAudioEndpoint, IMMDeviceEnumeratorGetDefaultAudioEndpoint, coreaudio.immdeviceenumerator_getdefaultaudioendpoint, mmdeviceapi/IMMDeviceEnumerator::GetDefaultAudioEndpoint
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: mmdeviceapi.h
req.include-header: 
req.redist: 
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
tech.root: 
req.typenames: EndpointFormFactor
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Mmdeviceapi.h
api_name:
 - IMMDeviceEnumerator.GetDefaultAudioEndpoint
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IMMDeviceEnumerator::GetDefaultAudioEndpoint


## -description



The <b>GetDefaultAudioEndpoint</b> method retrieves the default audio endpoint for the specified data-flow direction and role.




## -parameters




### -param dataFlow [in]

The data-flow direction for the endpoint device. The caller should set this parameter to one of the following two <a href="https://msdn.microsoft.com/d79315aa-d753-4674-84c2-9ba601f36f57">EDataFlow</a> enumeration values:

eRender

eCapture

The data-flow direction for a rendering device is eRender. The data-flow direction for a capture device is eCapture.


### -param role [in]

The role of the endpoint device. The caller should set this parameter to one of the following <a href="https://msdn.microsoft.com/0d0d3174-8489-4951-858c-024d58477ae0">ERole</a> enumeration values:

eConsole

eMultimedia

eCommunications

For more information, see Remarks.


### -param ppEndpoint






#### - ppDevice [out]

Pointer to a pointer variable into which the method writes the address of the <a href="https://msdn.microsoft.com/12b05e7e-81b2-49fd-bb9f-d5ad3315c580">IMMDevice</a> interface of the endpoint object for the default audio endpoint device. Through this method, the caller obtains a counted reference to the interface. The caller is responsible for releasing the interface, when it is no longer needed, by calling the interface's <b>Release</b> method. If the <b>GetDefaultAudioEndpoint</b> call fails,  <i>*ppDevice</i> is <b>NULL</b>.


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
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
Parameter <i>ppDevice</i> is <b>NULL</b>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
Parameter <i>dataFlow</i> or <i>role</i> is out of range.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_NOTFOUND</b></dt>
</dl>
</td>
<td width="60%">
No device is available.

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
</table>
 




## -remarks



<b>Note</b>

In Windows Vista, the MMDevice API supports <a href="https://msdn.microsoft.com/aa787004-0d3e-448b-80dd-92055f841aee">device roles</a> but the system-supplied user interface programs do not. The user interface in Windows Vista enables the user to select a default audio device for rendering and a default audio device for capture. When the user changes the default rendering or capture device, the system assigns all three device roles (eConsole, eMultimedia, and eCommunications) to that device. Thus, <b>GetDefaultAudioEndpoint</b> always selects the default rendering or capture device, regardless of which role is indicated by the <i>role</i> parameter. In a future version of Windows, the user interface might enable the user to assign individual roles to different devices. In that case, the selection of a rendering or capture device by <b>GetDefaultAudioEndpoint</b> might depend on the <i>role</i> parameter. Thus, the behavior of an audio application developed to run in Windows Vista might change when run in a future version of Windows. For more information, see <a href="https://msdn.microsoft.com/3b2cb1fe-0f11-4509-a6f3-513d2755cd29">Device Roles in Windows Vista</a>.

This method retrieves the default endpoint device for the specified data-flow direction (rendering or capture) and role. For example, a client can get the default console playback device by making the following call:

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>
  hr = pDevEnum-&gt;GetDefaultAudioEndpoint(
                   eRender, eConsole, &amp;pDeviceOut);
</pre>
</td>
</tr>
</table></span></div>
In the preceding code fragment, variable <i>hr</i> is of type <b>HRESULT</b>, <i>pDevEnum</i> is a pointer to an <b>IMMDeviceEnumerator</b> interface, and <i>pDeviceOut</i> is a pointer to an <b>IMMDevice</b> interface.

A Windows system might contain some combination of audio endpoint devices such as desktop speakers, high-fidelity headphones, desktop microphones, headsets with speaker and microphones, and high-fidelity multichannel speakers. The user can assign appropriate roles to the devices. For example, an application that manages voice communications streams can call <b>GetDefaultAudioEndpoint</b> to identify the designated rendering and capture devices for that role.

If only a single rendering or capture device is available, the system always assigns all three rendering or capture roles to that device. If the method fails to find a rendering or capture device for the specified role, this means that no rendering or capture device is available at all. If no device is available, the method sets  <i>*ppEndpoint</i> = <b>NULL</b> and returns ERROR_NOT_FOUND.

For code examples that call the <b>GetDefaultAudioEndpoint</b> method, see the following topics:

<ul>
<li>
<a href="https://msdn.microsoft.com/00bfcfd1-6592-43e3-90ad-730c92aa4cd3">Rendering a Stream</a>
</li>
<li>
<a href="https://msdn.microsoft.com/91a93b79-2563-4b25-af5d-ca5f7d35d77b">Audio Events for Legacy Audio Applications</a>
</li>
</ul>



## -see-also




<a href="https://msdn.microsoft.com/12b05e7e-81b2-49fd-bb9f-d5ad3315c580">IMMDevice Interface</a>



<a href="https://msdn.microsoft.com/1abdeac1-c156-40b8-8b8c-5ddb51e410aa">IMMDeviceEnumerator Interface</a>
 

 

