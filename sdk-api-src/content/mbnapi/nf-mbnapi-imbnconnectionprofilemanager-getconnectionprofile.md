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

# IMbnConnectionProfileManager::GetConnectionProfile


## -description


Gets a specific connection profile associated with the given Mobile Broadband device.


## -parameters




### -param mbnInterface [in]

An <a href="https://msdn.microsoft.com/958bce42-4772-4706-8900-1f83c5d3d52b">IMbnInterface</a> that represents the device for which the profile request applies.  If <i>mbnInterface</i> is <b>NULL</b>, then this function will return the profile of the given name associated with any device in the system.


### -param profileName [in]

A null-terminated string that contains the name of the connection profile.


### -param connectionProfile [out, retval]

An <a href="https://msdn.microsoft.com/f7730efe-e367-4642-8482-2a23052bab0c">IMbnConnectionProfile</a> interface that represents the desired connection profile.  If this method returns anything other than <b>S_OK</b>, this is <b>NULL</b>.


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
The method completed successfully.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_HANDLE</b></dt>
</dl>
</td>
<td width="60%">
The interface is invalid, most likely because the Mobile Broadband device has been removed from the system.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>HRESULT_FROM_WIN32(ERROR_NOT_FOUND)</b></dt>
</dl>
</td>
<td width="60%">
A profile with the given name does not exist.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>HRESULT_FROM_WIN32(ERROR_NOT_READY)</b></dt>
</dl>
</td>
<td width="60%">
The device is not ready.  Unable to obtain the subscriber ID because the device is  not <b>MBN_READY_STATE_INITIALIZED</b>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>HRESULT_FROM_WIN32(ERROR_NOT_FOUND)</b></dt>
</dl>
</td>
<td width="60%">
A profile with the given name does not exist.

</td>
</tr>
</table>
 




## -remarks



A connection profile is associated with the subscriber ID of the device. For GSM devices the subscriber ID is the International Mobile Subscriber Identity (IMSI) of the SIM.  For CDMA devices it is the Mobile Identification Number (MIN) string or the International Roaming MIN (IRM) string. 

If a new profile has been created using <a href="https://msdn.microsoft.com/b9c191cc-aa6f-4548-ad4a-f2b9808c5f23">CreateConnectionProfile</a>, then the caller must wait for the <a href="https://msdn.microsoft.com/94338c8c-2a89-412f-811e-5c50ecd9be70">OnConnectionProfileArrival</a> event to be received before calling <b>GetConnectionProfile</b> with the new profile's name; otherwise, the <b>GetConnectionProfile</b> API call may fail with <b>HRESULT_FROM_WIN32(ERROR_NOT_FOUND)</b>.





## -see-also




<a href="https://msdn.microsoft.com/a55e4183-f914-4064-a391-3bd31ca59160">IMbnConnectionProfileManager</a>
 

 

