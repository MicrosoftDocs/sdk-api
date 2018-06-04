---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# IMbnInterface::GetHomeProvider


## -description


Gets the home provider.


## -parameters




### -param homeProvider [out, retval]

A pointer to an <a href="https://msdn.microsoft.com/f4a02ca2-6be4-4843-a657-5d5dde8be623">MBN_PROVIDER</a> structure that represents the home provider.  If this method returns any value other than <b>S_OK</b>, this parameter is <b>NULL</b>.  Upon completion, the calling application must free the memory allocated to the  <b>providerID</b> and <b>providerName</b> members of <b>MBN_PROVIDER</b> by calling <a href=" http://go.microsoft.com/fwlink/p/?linkid=120718">SysFreeString</a>


## -returns



This method can return one of these values.

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
The method completed successfully.  <i>homeProvider</i> contains valid values.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_PENDING</b></dt>
</dl>
</td>
<td width="60%">
The information is not available.  The Mobile Broadband service is currently probing to get the home provider.  The calling application can get notified when the home provider is available by registering for the <a href="https://msdn.microsoft.com/4da50033-d55c-4878-b05c-cbc43c156da0">OnHomeProviderAvailable</a> method of <a href="https://msdn.microsoft.com/3c641f14-9f53-4d69-9faa-2491189083df">IMbnInterfaceEvents</a>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_MBN_PIN_REQUIRED</b></dt>
</dl>
</td>
<td width="60%">
The device requires that a PIN must be entered for this operation.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_MBN_SIM_NOT_INSERTED</b></dt>
</dl>
</td>
<td width="60%">
The SIM is not inserted.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_MBN_BAD_SIM</b></dt>
</dl>
</td>
<td width="60%">
A bad SIM is inserted in the device.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>HRESULT_FROM_WIN32(ERROR_READ_FAULT)</b></dt>
</dl>
</td>
<td width="60%">
Unable to read from the SIM or device memory.  For example, the SIM does not have home provider information provisioned.

</td>
</tr>
</table>
 




## -remarks



<b>GetHomeProvider</b> returns the home provider information for the device. The <b>dataClass</b> field of returned <a href="https://msdn.microsoft.com/f4a02ca2-6be4-4843-a657-5d5dde8be623">MBN_PROVIDER</a> structure should be ignored.

For the recoverable errors <b>E_MBN_PIN_REQUIRED</b>, <b>E_MBN_SIM_NOT_INSERTED</b>, and <b>E_MBN_BAD_SIM</b>, the Mobile Broadband service will query the device again for the home provider when the error condition is over. For example, if the device requires a PIN to be entered to retrieve this information, then it will return <b>E_MBN_PIN_REQUIRED</b>. When the application enters the PIN to unlock the device, then the Mobile Broadband service will again try to get this information from the device. The system will update the application about the status of new query by calling the <a href="https://msdn.microsoft.com/4da50033-d55c-4878-b05c-cbc43c156da0">OnHomeProviderAvailable</a> method of <a href="https://msdn.microsoft.com/3c641f14-9f53-4d69-9faa-2491189083df">IMbnInterfaceEvents</a>.

The registered <a href="https://msdn.microsoft.com/4da50033-d55c-4878-b05c-cbc43c156da0">OnHomeProviderAvailable</a> method of <a href="https://msdn.microsoft.com/3c641f14-9f53-4d69-9faa-2491189083df">IMbnInterfaceEvents</a> can be either called when home provider information is available or the new query completed with error. Once this function returns success then this information will never change.




## -see-also




<a href="https://msdn.microsoft.com/958bce42-4772-4706-8900-1f83c5d3d52b">IMbnInterface</a>
 

 

