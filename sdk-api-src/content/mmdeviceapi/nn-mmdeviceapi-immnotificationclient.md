---
UID: NN:mmdeviceapi.IMMNotificationClient
title: IMMNotificationClient
author: windows-sdk-content
description: The IMMNotificationClient interface provides notifications when an audio endpoint device is added or removed, when the state or properties of an endpoint device change, or when there is a change in the default role assigned to an endpoint device.
old-location: coreaudio\immnotificationclient.htm
old-project: CoreAudio
ms.assetid: 76d3cd52-30bd-48b0-8adc-c23991a60d1b
ms.author: windowssdkdev
ms.date: 05/09/2018
ms.keywords: IMMNotificationClient, IMMNotificationClient interface [Core Audio], IMMNotificationClient interface [Core Audio],described, coreaudio.immnotificationclient, mmdeviceapi/IMMNotificationClient
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
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
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Mmdeviceapi.h
api_name:
-	IMMNotificationClient
product: Windows
targetos: Windows
req.lib: 
req.dll: Mmdevapi.dll
req.irql: 
req.product: GDI+ 1.1
---

# IMMNotificationClient interface


## -description



The <b>IMMNotificationClient</b> interface provides notifications when an <a href="https://msdn.microsoft.com/773714fb-3b00-4f03-988f-05c5835f87cf">audio endpoint device</a> is added or removed, when the state or properties of an endpoint device change, or when there is a change in the default role assigned to an endpoint device. Unlike the other interfaces in this section, which are implemented by the MMDevice API system component, an MMDevice API client implements the <b>IMMNotificationClient</b> interface. To receive notifications, the client passes a pointer to its <b>IMMNotificationClient</b> interface instance as a parameter to the <a href="https://msdn.microsoft.com/2c524f64-0b35-4433-9768-582dcb580a74">IMMDeviceEnumerator::RegisterEndpointNotificationCallback</a> method.

After registering its <b>IMMNotificationClient</b> interface, the client receives event notifications in the form of callbacks through the methods of the interface.

Each method in the <b>IMMNotificationClient</b> interface receives, as one of its input parameters, an <a href="https://msdn.microsoft.com/3c955e2d-daaa-4b77-8ca5-890383bb2d39">endpoint ID string</a> that identifies the audio endpoint device that is the subject of the notification. The string uniquely identifies the device with respect to all of the other audio endpoint devices in the system. The methods in the <b>IMMNotificationClient</b> interface implementation should treat this string as opaque. That is, none of the methods should attempt to parse the contents of the string to obtain information about the device. The reason is that the string format is undefined and might change from one implementation of the MMDevice API system module to the next.

A client can use the endpoint ID string that it receives as an input parameter in a call to an <b>IMMNotificationClient</b> method in two ways:

<ul>
<li>The client can create an instance of the device that the endpoint ID string identifies. The client does this by calling the <a href="https://msdn.microsoft.com/88cd7acc-a5d7-406d-ac73-bae357ad2ee2">IMMDeviceEnumerator::GetDevice</a> method and supplying the endpoint ID string as an input parameter.</li>
<li>The client can compare the endpoint ID string with the endpoint ID string of an existing device instance. To obtain the second endpoint ID string, the client calls the <a href="https://msdn.microsoft.com/b2f56713-856c-408e-8993-1d13e234dc89">IMMDevice::GetId</a> method of the device instance. If the two strings match, they identify the same device.</li>
</ul>
In implementing the <b>IMMNotificationClient</b> interface, the client should observe these rules to avoid deadlocks and undefined behavior:

<ul>
<li>The methods of the interface must be nonblocking. The client should never wait on a synchronization object during an event callback.</li>
<li>To avoid dead locks, the client should never call <a href="https://msdn.microsoft.com/2c524f64-0b35-4433-9768-582dcb580a74">IMMDeviceEnumerator::RegisterEndpointNotificationCallback</a> or <a href="https://msdn.microsoft.com/dc1e85af-f399-469d-806a-a2d80b700b75">IMMDeviceEnumerator::UnregisterEndpointNotificationCallback</a> in its implementation of  <b>IMMNotificationClient</b> methods. </li>
<li>The client should never release the final reference on an MMDevice API object during an event callback.</li>
</ul>
For a code example that implements the <b>IMMNotificationClient</b> interface, see <a href="https://msdn.microsoft.com/b31500d6-a79d-4e6e-878e-6bd77055f1ad">Device Events</a>.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMMNotificationClient</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IMMNotificationClient</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IMMNotificationClient</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/3d484e5d-bdc6-41f1-bd94-ab0c9e109222">OnDefaultDeviceChanged</a>
</td>
<td align="left" width="63%">
Notifies the client that the default audio endpoint device for a particular role has changed.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/c839493d-e53c-4afe-b53d-af9d1a6f2965">OnDeviceAdded</a>
</td>
<td align="left" width="63%">
Indicates that a new audio endpoint device has been added.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/0adacdd2-5fa3-4d27-a299-fa0d41b6d285">OnDeviceRemoved</a>
</td>
<td align="left" width="63%">
Indicates that an audio endpoint device has been removed.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/4725a300-c84b-40cd-93a6-6ef6c8e89708">OnDeviceStateChanged</a>
</td>
<td align="left" width="63%">
Indicates that the state of an audio endpoint device has changed.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/194aa7d1-4885-49c4-b9c3-2c47468c139f">OnPropertyValueChanged</a>
</td>
<td align="left" width="63%">
Indicates that the value of a property belonging to an audio endpoint device has changed.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/b18e2094-e974-4c23-b70b-ace5a168132d">Core Audio Interfaces</a>



<a href="https://msdn.microsoft.com/b2f56713-856c-408e-8993-1d13e234dc89">IMMDevice::GetId</a>



<a href="https://msdn.microsoft.com/88cd7acc-a5d7-406d-ac73-bae357ad2ee2">IMMDeviceEnumerator::GetDevice</a>



<a href="https://msdn.microsoft.com/2c524f64-0b35-4433-9768-582dcb580a74">IMMDeviceEnumerator::RegisterEndpointNotificationCallback</a>



<a href="https://msdn.microsoft.com/dc1e85af-f399-469d-806a-a2d80b700b75">IMMDeviceEnumerator::UnregisterEndpointNotificationCallback</a>



<a href="https://msdn.microsoft.com/3a8fd734-0761-4b5b-ba04-677c7c040988">MMDevice API</a>
 

 

