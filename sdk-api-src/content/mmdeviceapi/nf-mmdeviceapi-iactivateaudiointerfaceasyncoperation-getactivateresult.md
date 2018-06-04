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

# IActivateAudioInterfaceAsyncOperation::GetActivateResult


## -description


Gets the results of an asynchronous activation of a <a href="https://msdn.microsoft.com/452b9725-b0b9-4888-bbb5-a23e0067e840">WASAPI</a> interface initiated by an application calling the <a href="https://msdn.microsoft.com/7BAFD9DB-DCD7-4093-A24B-9A8556C6C45B">ActivateAudioInterfaceAsync</a> function.


## -parameters




### -param activateResult [out]


### -param activatedInterface [out]


## -returns



The function returns an <b>HRESULT</b>. Possible values include, but are not limited to, those in the following table.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_ILLEGAL_METHOD_CALL</b></dt>
</dl>
</td>
<td width="60%">
The method was called before the asynchronous operation was complete. 

</td>
</tr>
</table>
 




## -remarks



An application calls this method after Windows calls the <a href="https://msdn.microsoft.com/f434db12-ab8e-40ca-8a55-b02f28ea5575">ActivateCompleted</a> method of the application’s <a href="https://msdn.microsoft.com/04ff7cbb-fd33-40d9-9c11-4f716c6423b0">IActivateAudioInterfaceCompletionHandler</a> interface.

The result code returned through <i>activateResult</i> may depend on the requested interface. For additional information, see <a href="https://msdn.microsoft.com/12e4a117-1fa3-49c8-949b-8973edf7e12e">IMMDevice::Activate</a>. A result code of <b>E_ACCESSDENIED</b> might indicate that the user has not given consent to access the device in a manner required by the requested <a href="https://msdn.microsoft.com/452b9725-b0b9-4888-bbb5-a23e0067e840">WASAPI</a> interface. 

The returned <i>activatedInterface</i> may be <b>NULL</b> if <i>activateResult</i> is not a success code. 




## -see-also




<a href="https://msdn.microsoft.com/7BAFD9DB-DCD7-4093-A24B-9A8556C6C45B">ActivateAudioInterfaceAsync</a>



<a href="https://msdn.microsoft.com/43b25a67-d9a8-4749-a654-c7310039c553">IActivateAudioInterfaceAsyncOperation</a>
 

 

