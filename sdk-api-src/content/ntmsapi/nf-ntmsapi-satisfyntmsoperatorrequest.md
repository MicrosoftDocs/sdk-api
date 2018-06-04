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

# SatisfyNtmsOperatorRequest function


## -description


<p class="CCE_Message">[<a href="https://msdn.microsoft.com/af7186f8-7921-48e3-a4fd-23259a6e9018">Removable Storage Manager</a> is no longer available as of Windows 7 and  Windows Server 2008 R2.]

The 
<b>SatisfyNtmsOperatorRequest</b> function completes the specified RSM operator request.


## -parameters




### -param hSession [in]

Handle to the session returned by the 
<a href="https://msdn.microsoft.com/5a323911-e99c-4f81-9580-0feac2f0a54e">OpenNtmsSession</a> function.


### -param lpRequestId [in]

Operator request object ID. This value is returned by 
<a href="https://msdn.microsoft.com/d2c146d0-f1f9-4810-a489-91b5c4ca3431">SubmitNtmsOperatorRequest</a>.


## -returns



This function returns one of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_ACCESS_DENIED</b></dt>
</dl>
</td>
<td width="60%">
The user that tried to execute this function does not have administrator privileges. Only an administrator of the RSM server can satisfy operator requests.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_OBJECT_NOT_FOUND</b></dt>
</dl>
</td>
<td width="60%">
The operator request object ID was not found. This error occurs if the request is completed before the operation has been satisfied or when an request ID that is not valid is specified.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_SUCCESS</b></dt>
</dl>
</td>
<td width="60%">
The operator request has been satisfied.

</td>
</tr>
</table>
 




## -remarks



If an application detects that the operator did not acknowledge a satisfied operator request, the application can use the 
<b>SatisfyNtmsOperatorRequest</b> function to remove the request.

For a list of the existing operator requests to cancel with the 
<b>SatisfyNtmsOperatorRequest</b> function, see the 
<a href="https://msdn.microsoft.com/bbbb2888-36f5-4667-90f0-088382ad32f5">EnumerateNtmsObject</a> function.




## -see-also




<a href="https://msdn.microsoft.com/d0ba65fe-0355-4bd6-b9ad-98e8f7992827">CancelNtmsOperatorRequest</a>



<a href="removable_storage_manager_functions.htm">Operator Request Functions</a>



<a href="https://msdn.microsoft.com/d2c146d0-f1f9-4810-a489-91b5c4ca3431">SubmitNtmsOperatorRequest</a>



<a href="https://msdn.microsoft.com/abc78047-a6d7-4e98-baec-5e4ba394c64f">WaitForNtmsOperatorRequest</a>
 

 

