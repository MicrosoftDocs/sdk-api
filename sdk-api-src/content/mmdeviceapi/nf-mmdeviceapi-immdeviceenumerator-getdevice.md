---
UID: NF:mmdeviceapi.IMMDeviceEnumerator.GetDevice
title: IMMDeviceEnumerator::GetDevice
author: windows-sdk-content
description: The GetDevice method retrieves an audio endpoint device that is identified by an endpoint ID string.
old-location: coreaudio\immdeviceenumerator_getdevice.htm
old-project: CoreAudio
ms.assetid: 88cd7acc-a5d7-406d-ac73-bae357ad2ee2
ms.author: windowssdkdev
ms.date: 06/04/2018
ms.keywords: GetDevice, GetDevice method [Core Audio], GetDevice method [Core Audio],IMMDeviceEnumerator interface, IMMDeviceEnumerator interface [Core Audio],GetDevice method, IMMDeviceEnumerator.GetDevice, IMMDeviceEnumerator::GetDevice, IMMDeviceEnumeratorGetDevice, coreaudio.immdeviceenumerator_getdevice, mmdeviceapi/IMMDeviceEnumerator::GetDevice
ms.prod: windows
ms.technology: windows-sdk
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
 - IMMDeviceEnumerator.GetDevice
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IMMDeviceEnumerator::GetDevice


## -description



The <b>GetDevice</b> method retrieves an audio endpoint device that is identified by an <a href="https://msdn.microsoft.com/3c955e2d-daaa-4b77-8ca5-890383bb2d39">endpoint ID string</a>.




## -parameters




### -param pwstrId [in]

Pointer to a string containing the endpoint ID. The caller typically obtains this string from the <a href="https://msdn.microsoft.com/b2f56713-856c-408e-8993-1d13e234dc89">IMMDevice::GetId</a> method or from one of the methods in the <a href="https://msdn.microsoft.com/76d3cd52-30bd-48b0-8adc-c23991a60d1b">IMMNotificationClient</a> interface.


### -param ppDevice [out]

Pointer to a pointer variable into which the method writes the address of the <a href="https://msdn.microsoft.com/12b05e7e-81b2-49fd-bb9f-d5ad3315c580">IMMDevice</a> interface for the specified device. Through this method, the caller obtains a counted reference to the interface. The caller is responsible for releasing the interface, when it is no longer needed, by calling the interface's <b>Release</b> method. If the <b>GetDevice</b> call fails,  <i>*ppDevice</i> is <b>NULL</b>.


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
Parameter <i>pwstrId</i> or <i>ppDevice</i> is <b>NULL</b>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_NOTFOUND</b></dt>
</dl>
</td>
<td width="60%">
The device ID does not identify an audio device that is in this system.

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



If two programs are running in two different processes and both need to access the same audio endpoint device, one program cannot simply pass the device's <b>IMMDevice</b> interface to the other program. However, the programs can access the same device by following these steps:

<ol>
<li>The first program calls the <b>IMMDevice::GetId</b> method in the first process to obtain the endpoint ID string that identifies the device.</li>
<li>The first program passes the endpoint ID string across the process boundary to the second program.</li>
<li>To obtain a reference to the device's <b>IMMDevice</b> interface in the second process, the second program calls <b>GetDevice</b> with the endpoint ID string.</li>
</ol>
For more information about the <b>GetDevice</b> method, see the following topics:

<ul>
<li>
<a href="https://msdn.microsoft.com/3c955e2d-daaa-4b77-8ca5-890383bb2d39">Endpoint ID Strings</a>
</li>
<li>
<a href="https://msdn.microsoft.com/91a93b79-2563-4b25-af5d-ca5f7d35d77b">Audio Events for Legacy Audio Applications</a>
</li>
</ul>
For code examples that use the <b>GetDevice</b> method, see the following topics:

<ul>
<li>
<a href="https://msdn.microsoft.com/ad8753ba-ad20-4122-b0f2-eb165f98db67">Device Properties</a>
</li>
<li>
<a href="https://msdn.microsoft.com/b31500d6-a79d-4e6e-878e-6bd77055f1ad">Device Events</a>
</li>
<li>
<a href="https://msdn.microsoft.com/72bf9164-96c6-4543-b858-19480b032fdb">Using the IKsControl Interface to Access Audio Properties</a>
</li>
</ul>



## -see-also




<a href="https://msdn.microsoft.com/12b05e7e-81b2-49fd-bb9f-d5ad3315c580">IMMDevice Interface</a>



<a href="https://msdn.microsoft.com/b2f56713-856c-408e-8993-1d13e234dc89">IMMDevice::GetId</a>



<a href="https://msdn.microsoft.com/1abdeac1-c156-40b8-8b8c-5ddb51e410aa">IMMDeviceEnumerator Interface</a>



<a href="https://msdn.microsoft.com/76d3cd52-30bd-48b0-8adc-c23991a60d1b">IMMNotificationClient Interface</a>
 

 

