---
UID: NF:mmdeviceapi.IMMDevice.GetId
title: IMMDevice::GetId (mmdeviceapi.h)
author: windows-sdk-content
description: The GetId method retrieves an endpoint ID string that identifies the audio endpoint device.
old-location: coreaudio\immdevice_getid.htm
tech.root: CoreAudio
ms.assetid: b2f56713-856c-408e-8993-1d13e234dc89
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: GetId, GetId method [Core Audio], GetId method [Core Audio],IMMDevice interface, IMMDevice interface [Core Audio],GetId method, IMMDevice.GetId, IMMDevice::GetId, IMMDeviceGetId, coreaudio.immdevice_getid, mmdeviceapi/IMMDevice::GetId
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
 - IMMDevice.GetId
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMMDevice::GetId


## -description



The <b>GetId</b> method retrieves an <a href="https://msdn.microsoft.com/3c955e2d-daaa-4b77-8ca5-890383bb2d39">endpoint ID string</a> that identifies the audio endpoint device.




## -parameters




### -param ppstrId [out]

Pointer to a pointer variable into which the method writes the address of a null-terminated, wide-character string containing the endpoint device ID. The method allocates the storage for the string. The caller is responsible for freeing the storage, when it is no longer needed, by calling the <b>CoTaskMemFree</b> function. If the <b>GetId</b> call fails,  <i>*ppstrId is NULL.</i> For information about <b>CoTaskMemFree</b>, see the Windows SDK documentation.


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
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
Parameter <i>pwstrId</i> is <b>NULL</b>.

</td>
</tr>
</table>
 




## -remarks



The endpoint ID string obtained from this method identifies the audio endpoint device that is represented by the <b>IMMDevice</b> interface instance. A client can use the endpoint ID string to create an instance of the audio endpoint device at a later time or in a different process by calling the <a href="https://msdn.microsoft.com/88cd7acc-a5d7-406d-ac73-bae357ad2ee2">IMMDeviceEnumerator::GetDevice</a> method. Clients should treat the contents of the endpoint ID string as opaque. That is, clients should <i>not</i> attempt to parse the contents of the string to obtain information about the device. The reason is that the string format is undefined and might change from one implementation of the MMDevice API system module to the next.

For code examples that call the <b>GetId</b> method, see the following topics:

<ul>
<li>
<a href="https://msdn.microsoft.com/ad8753ba-ad20-4122-b0f2-eb165f98db67">Device Properties</a>
</li>
<li>
<a href="https://msdn.microsoft.com/54dcaa0e-2652-406d-ba24-c8885924acc6">Device Roles for Legacy Windows Multimedia Applications</a>
</li>
</ul>



## -see-also




<a href="https://msdn.microsoft.com/12b05e7e-81b2-49fd-bb9f-d5ad3315c580">IMMDevice Interface</a>



<a href="https://msdn.microsoft.com/88cd7acc-a5d7-406d-ac73-bae357ad2ee2">IMMDeviceEnumerator::GetDevice</a>
 

 

