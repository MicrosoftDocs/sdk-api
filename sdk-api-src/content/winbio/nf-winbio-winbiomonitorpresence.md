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

# WinBioMonitorPresence function


## -description


Turns on the face-recognition or iris-monitoring mechanism for the specified biometric unit. Starting with Windows 10, build 1607, this  function is available to use with a mobile image.


## -parameters




### -param SessionHandle [in]

An asynchronous handle for the biometric session that you obtained by  calling the <a href="https://msdn.microsoft.com/711EDE14-A2EE-415D-8FB6-562D71D68146">WinBioAsyncOpenSession</a> function with the <i>PoolType</i> parameter set to <b>WINBIO_POOL_SYSTEM</b>.


### -param UnitId [in]

The identifier of the biometric unit for which you want to turn on the  face-recognition or iris-monitoring mechanism.


## -returns



If the function parameters are acceptable, it returns <b>S_OK</b>. If the function parameters are not acceptable, it returns an <b>HRESULT</b> value that indicates the error.  
Possible values include, but are not limited to, those in the following table.  For a list of common error codes, see <a href="https://msdn.microsoft.com/ce52efc3-92c7-40e4-ac49-0c54049e169f">Common HRESULT Values</a>.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><b>E_HANDLE</b></b></dt>
</dl>
</td>
<td width="60%">
The session handle is not valid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><b>E_INVALIDARG</b></b></dt>
</dl>
</td>
<td width="60%">
The <i>UnitId</i> parameter cannot equal zero.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><b>WINBIO_E_INCORRECT_SESSION_TYPE</b></b></dt>
</dl>
</td>
<td width="60%">
The session handle does not correspond to an asynchronous biometric session.

</td>
</tr>
</table>
 

The actual success or failure of the operation itself is returned to the your notification function in a <a href="https://msdn.microsoft.com/1C8A4557-3851-4AB2-BB9B-AE199EB9D024">WINBIO_ASYNC_RESULT</a> structure.




## -remarks



A single biometric session can have only one active presence monitor at any point in time.

After you successfully call <b>WinBioMonitorPresence</b>, your notification  function receives notifications in the form of a <a href="https://msdn.microsoft.com/1C8A4557-3851-4AB2-BB9B-AE199EB9D024">WINBIO_ASYNC_RESULT</a> structure with an <b>Operation</b> member equal to <b>WINBIO_OPERATION_MONITOR_PRESENCE</b>. You should then examine the <b>Parameters.MonitorPresence</b> member of the <b>WINBIO_ASYNC_RESULT</b> structure for more information.

To stop receiving notifications, call either <a href="https://msdn.microsoft.com/62176608-1545-47d2-b4be-37bb2a4a064b">WinBioCancel</a> or <a href="https://msdn.microsoft.com/b0adcf87-2f99-4154-a4fb-fb2f07181cd0">WinBioCloseSession</a> with the original asynchronous handle value.




## -see-also




<a href="https://msdn.microsoft.com/1C8A4557-3851-4AB2-BB9B-AE199EB9D024">WINBIO_ASYNC_RESULT</a>



<a href="https://msdn.microsoft.com/711EDE14-A2EE-415D-8FB6-562D71D68146">WinBioAsyncOpenSession</a>



<a href="https://msdn.microsoft.com/62176608-1545-47d2-b4be-37bb2a4a064b">WinBioCancel</a>



<a href="https://msdn.microsoft.com/b0adcf87-2f99-4154-a4fb-fb2f07181cd0">WinBioCloseSession</a>
 

 

