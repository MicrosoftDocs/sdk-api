---
UID: NF:scserver.CSecureChannelServer.MACUpdate
title: CSecureChannelServer::MACUpdate
author: windows-sdk-content
description: The MACUpdate method updates the message authentication code (MAC) value with a parameter value.
old-location: wmdm\csecurechannelserver_macupdate.htm
old-project: WMDM
ms.assetid: f8b5548d-ffd5-4dc3-8d08-61a65841a997
ms.author: windowssdkdev
ms.date: 05/22/2018
ms.keywords: CSecureChannelServer interface [windows Media Device Manager],MACUpdate method, CSecureChannelServer.MACUpdate, CSecureChannelServer::MACUpdate, CSecureChannelServerMACUpdate, MACUpdate, MACUpdate method [windows Media Device Manager], MACUpdate method [windows Media Device Manager],CSecureChannelServer interface, scserver/CSecureChannelServer::MACUpdate, wmdm.csecurechannelserver_macupdate
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: scserver.h
req.include-header: 
req.target-type: Windows
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
tech.root: 
req.typenames: SCHEDULE_HEADER, *PSCHEDULE_HEADER
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mssachlp.lib
 - mssachlp.dll
api_name:
 - CSecureChannelServer.MACUpdate
product: Windows
targetos: Windows
req.lib: Mssachlp.lib
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
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
 

 

