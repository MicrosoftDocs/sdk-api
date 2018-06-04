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

# FaxExtUnregisterForEvents function


## -description


The <b>FaxExtUnregisterForEvents</b> callback function unregisters the fax extension DLL for notifications about configuration data changes related to a specific device and GUID.


## -parameters




### -param hNotification

Type: <b>HANDLE</b>

Specifies a <b>HANDLE</b> that indicates the registration handle from which the caller wishes to unregister.




The handle must be the return value from a previous call to the <a href="https://msdn.microsoft.com/a298f232-0670-4b0e-8962-4c111993dd36">FaxExtRegisterForEvents</a> function.


## -returns



Type: <b>DWORD</b>

If the function succeeds, the return value is <b>ERROR_SUCCESS</b>.





If the function fails, the return value is a nonzero error code defined in WinError.h. You can call the Win32 <b>FormatMessage</b> function specifying the FORMAT_MESSAGE_FROM_SYSTEM flag to retrieve a generic description of the error.





The <b>FaxExtUnregisterForEvents</b> function can return the following error codes.


<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_SUCCESS</b></dt>
</dl>
</td>
<td width="60%">
The unregistration process succeeded.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_NOT_FOUND</b></dt>
</dl>
</td>
<td width="60%">
The registration handle specified by the hNotification parameter was not found.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_PARAMETER</b></dt>
</dl>
</td>
<td width="60%">
The <i>hNotification</i> parameter is invalid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_NOT_ENOUGH_MEMORY</b></dt>
</dl>
</td>
<td width="60%">
Not enough memory is available to complete the operation.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_GEN_FAILURE</b></dt>
</dl>
</td>
<td width="60%">
An internal failure at the fax server prevents access to the data.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_SHUTDOWN_IN_PROGRESS</b></dt>
</dl>
</td>
<td width="60%">
The server is shutting down.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_BUSY</b></dt>
</dl>
</td>
<td width="60%">
The server cannot process a request for notifications while it is sending a notification about a data change. You should try calling the function at a later time.

</td>
</tr>
</table>
 




## -remarks



When the fax extension calls this fax service callback function, it must use the function pointer exposed by the fax service when the service calls the <a href="https://msdn.microsoft.com/1dce2986-d56c-45c5-a482-81c012904fef">FaxExtInitializeConfig</a> function.

The fax extension can call the <b>FaxExtUnregisterForEvents</b> function to stop receiving notifications about device configuration data changes. An extension registers for notifications by calling the fax service's callback function <a href="https://msdn.microsoft.com/a298f232-0670-4b0e-8962-4c111993dd36">FaxExtRegisterForEvents</a>.

The fax service passes a pointer to the <b>FaxExtUnregisterForEvents</b> callback function when the fax service calls the <a href="https://msdn.microsoft.com/1dce2986-d56c-45c5-a482-81c012904fef">FaxExtInitializeConfig</a> function. The PFAX_EXT_UNREGISTER_FOR_EVENTS data type is a pointer to a <b>FaxExtUnregisterForEvents</b> function.




## -see-also




<a href="https://msdn.microsoft.com/1dce2986-d56c-45c5-a482-81c012904fef">FaxExtInitializeConfig</a>



<a href="https://msdn.microsoft.com/a298f232-0670-4b0e-8962-4c111993dd36">FaxExtRegisterForEvents</a>
 

 

