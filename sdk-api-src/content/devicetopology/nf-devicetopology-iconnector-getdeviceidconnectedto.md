---
UID: NF:devicetopology.IConnector.GetDeviceIdConnectedTo
title: IConnector::GetDeviceIdConnectedTo
author: windows-sdk-content
description: The GetDeviceIdConnectedTo method gets the device identifier of the audio device, if any, that this connector is connected to.
old-location: coreaudio\iconnector_getdeviceidconnectedto.htm
tech.root: CoreAudio
ms.assetid: 8f62bdeb-4765-467f-b68d-d94fc9a51dfb
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: GetDeviceIdConnectedTo, GetDeviceIdConnectedTo method [Core Audio], GetDeviceIdConnectedTo method [Core Audio],IConnector interface, IConnector interface [Core Audio],GetDeviceIdConnectedTo method, IConnector.GetDeviceIdConnectedTo, IConnector::GetDeviceIdConnectedTo, IConnectorGetDeviceIdConnectedTo, coreaudio.iconnector_getdeviceidconnectedto, devicetopology/IConnector::GetDeviceIdConnectedTo
ms.topic: method
req.header: devicetopology.h
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
 - Devicetopology.h
api_name:
 - IConnector.GetDeviceIdConnectedTo
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IConnector::GetDeviceIdConnectedTo


## -description



The <b>GetDeviceIdConnectedTo</b> method gets the device identifier of the audio device, if any, that this connector is connected to.




## -parameters




### -param ppwstrDeviceId [out]

Pointer to a string pointer into which the method writes the address of a null-terminated, wide-character string that contains the device identifier of the connected device. The method allocates the storage for the string. The caller is responsible for freeing the storage, when it is no longer needed, by calling the <b>CoTaskMemFree</b> function. If the <b>GetDeviceIdConnectedTo</b> call fails,  <i>*ppwstrDeviceId</i> is <b>NULL</b>. For information about <b>CoTaskMemFree</b>, see the Windows SDK documentation.


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
Pointer <i>ppwstrDeviceId</i> is <b>NULL</b>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_NOTFOUND</b></dt>
</dl>
</td>
<td width="60%">
This connector is not connected, or the other side of the connection is not another device topology (for example, a Software_IO connection).

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_MEMORY</b></dt>
</dl>
</td>
<td width="60%">
Out of memory.

</td>
</tr>
</table>
 




## -remarks



The device identifier obtained from this method can be used as an input parameter to the <a href="https://msdn.microsoft.com/88cd7acc-a5d7-406d-ac73-bae357ad2ee2">IMMDeviceEnumerator::GetDevice</a> method.

This method is functionally equivalent to, but more efficient than, the following series of method calls:

<ul>
<li>Call the <a href="https://msdn.microsoft.com/bee0187c-5650-4b54-89b7-e63874048ed0">IConnector::GetConnectedTo</a> method to obtain the <a href="https://msdn.microsoft.com/6eb5b439-3ac7-4c0b-84e2-b246c1b946a5">IConnector</a> interface of the "to" connector.</li>
<li>Call the <b>IConnector::QueryInterface</b> method (with parameter <i>iid</i> set to <b>REFIID</b> IID_IPart) to obtain the <a href="https://msdn.microsoft.com/3bcfab9f-fad8-4605-8780-0b7c2068fcdf">IPart</a> interface of the "to" connector.</li>
<li>Call the <a href="https://msdn.microsoft.com/5ad5fc66-6452-4d55-8c6a-a20a87431302">IPart::GetTopologyObject</a> method to obtain the <a href="https://msdn.microsoft.com/1b509f69-6277-40c0-a293-02afc30d464a">IDeviceTopology</a> interface of the "to" device (the device that contains the "to" connector).</li>
<li>Call the <a href="https://msdn.microsoft.com/2ecf8f23-7cfd-447a-ab76-8a23b79f5d6c">IDeviceTopology::GetDeviceId</a> method to obtain the device ID of the "to" device.</li>
</ul>



## -see-also




<a href="https://msdn.microsoft.com/6eb5b439-3ac7-4c0b-84e2-b246c1b946a5">IConnector Interface</a>



<a href="https://msdn.microsoft.com/88cd7acc-a5d7-406d-ac73-bae357ad2ee2">IMMDeviceEnumerator::GetDevice</a>
 

 

