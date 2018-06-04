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

# CSecureChannelServer::MACUpdate


## -description



The <b>MACUpdate</b> method updates the message authentication code (MAC) value with a parameter value.




## -parameters




### -param hMAC [in]

Handle to the array containing the MAC for the current parameter data. The handle is returned by the <b>MACInit</b> method.


### -param pbData [in]

Pointer to the data to be added to the MAC value for the current parameter data.


### -param dwDataLen

<b>DWORD</b> specifying the length of the data to which <i>pbData</i> points.


## -returns



The method returns an <b>HRESULT</b>. All the interface methods in Windows Media Device Manager can return any of the following classes of error codes:

<ul>
<li>Standard COM error codes </li>
<li>Windows error codes converted to HRESULT values </li>
<li>Windows Media Device Manager error codes </li>
</ul>
For an extensive list of possible error codes, see <a href="https://msdn.microsoft.com/library/windows/hardware/dn938542">Error Codes</a>.

Possible values include, but are not limited to, those in the following table.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td>S_OK</td>
<td>The method succeeded.</td>
</tr>
<tr>
<td>E_INVALIDARG</td>
<td>A parameter is invalid or is a <b>NULL</b> pointer.</td>
</tr>
<tr>
<td>E_FAIL</td>
<td>An unspecified error occurred.</td>
</tr>
</table>
 




## -remarks



<b>MACUpdate</b> must be called repeatedly with each piece of data to add to the message authentication code (MAC) . <b>MACUpdate</b> must be called after <b>MACInit</b> because <b>MACInit</b> acquires the MAC handle. <b>MACFinal</b> must be called after <b>MACUpdate</b>.


#### Examples

See the example code for <a href="https://msdn.microsoft.com/92161bf3-8e2f-4b4a-a09a-98e33637df27">MACInit</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/e6e1463a-5a26-4b83-85e0-a639d384a199">CSecureChannelServer Class</a>



<a href="https://msdn.microsoft.com/92161bf3-8e2f-4b4a-a09a-98e33637df27">CSecureChannelServer::MACInit</a>



<a href="https://msdn.microsoft.com/6cb49f6b-e303-4840-9343-9891e75e07a4">Message Authentication</a>
 

 

