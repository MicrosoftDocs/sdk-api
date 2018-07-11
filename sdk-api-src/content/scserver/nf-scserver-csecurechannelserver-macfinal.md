---
UID: NF:scserver.CSecureChannelServer.MACFinal
title: CSecureChannelServer::MACFinal
author: windows-sdk-content
description: The MACFinal method releases the message authentication code (MAC) channel and retrieves a final MAC value.
old-location: wmdm\csecurechannelserver_macfinal.htm
old-project: WMDM
ms.assetid: 047340a5-5382-443e-a6d5-ecbcdfe9a210
ms.author: windowssdkdev
ms.date: 05/23/2018
ms.keywords: CSecureChannelServer interface [windows Media Device Manager],MACFinal method, CSecureChannelServer.MACFinal, CSecureChannelServer::MACFinal, CSecureChannelServerMACFinal, MACFinal, MACFinal method [windows Media Device Manager], MACFinal method [windows Media Device Manager],CSecureChannelServer interface, scserver/CSecureChannelServer::MACFinal, wmdm.csecurechannelserver_macfinal
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
 - CSecureChannelServer.MACFinal
product: Windows
targetos: Windows
req.lib: Mssachlp.lib
req.dll: 
req.irql: 
req.product: ADAM
---

# CSecureChannelServer::MACFinal


## -description



The <b>MACFinal</b> method releases the message authentication code (MAC) channel and retrieves a final MAC value.




## -parameters




### -param hMAC [in]

Handle to the MAC for the current parameter data. The handle is returned from the <b>MACInit</b> method. The handle is no longer valid after this method call.


### -param abData [out]

Pointer to an 8-byte buffer to receive the final MAC value for the current parameter data.


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
<td>A parameter is invalid.</td>
</tr>
<tr>
<td>E_FAIL</td>
<td>An unspecified error occurred.</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/e6e1463a-5a26-4b83-85e0-a639d384a199">CSecureChannelServer Class</a>



<a href="https://msdn.microsoft.com/92161bf3-8e2f-4b4a-a09a-98e33637df27">CSecureChannelServer::MACInit</a>



<a href="https://msdn.microsoft.com/f8b5548d-ffd5-4dc3-8d08-61a65841a997">CSecureChannelServer::MACUpdate</a>



<a href="https://msdn.microsoft.com/6cb49f6b-e303-4840-9343-9891e75e07a4">Message Authentication</a>
 

 

