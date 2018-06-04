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

# WFDCancelOpenSession function


## -description


The  <b>WFDCancelOpenSession</b> function indicates that the application wants to cancel a pending <a href="https://msdn.microsoft.com/CF1FF7C2-31CD-4FAB-9891-0A72BEA3E9F1">WFDStartOpenSession</a> function that has not completed.


## -parameters




### -param hSessionHandle [in]

A session handle to a Wi-Fi Direct session to cancel. This is a session handle previously returned by the <a href="https://msdn.microsoft.com/CF1FF7C2-31CD-4FAB-9891-0A72BEA3E9F1">WFDStartOpenSession</a> function.


## -returns



If the function succeeds, the return value is ERROR_SUCCESS.

If the function fails, the return value may be one of the following return codes.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_HANDLE</b></dt>
</dl>
</td>
<td width="60%">
The handle is invalid. 

This error is returned if the handle specified in the <i>hSessionHandle</i>  parameter was not found in the handle table.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_PARAMETER</b></dt>
</dl>
</td>
<td width="60%">
The parameter is incorrect. 

This error is returned if the <i>hSessionHandle</i> parameter is <b>NULL</b> or not valid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>RPC_STATUS</b></dt>
</dl>
</td>
<td width="60%">
Various error codes.

</td>
</tr>
</table>
 




## -remarks



The <b>WFDCancelOpenSession</b> function is part of Wi-Fi Direct, a new feature in Windows 8 and Windows Server 2012. Wi-Fi Direct is based on the development of the Wi-Fi Peer-to-Peer Technical Specification v1.1 by the Wi-Fi Alliance (see <a href="https://www.wi-fi.org/knowledge_center_overview.php?type=4">Wi-Fi Alliance Published Specifications</a>). The goal of the Wi-Fi Peer-to-Peer Technical Specification is to provide a solution for Wi-Fi device-to-device connectivity without the need for either a Wireless Access Point (wireless AP) to setup the connection or the use of the existing Wi-Fi adhoc (IBSS) mechanism. 



A call to the <b>WFDCancelOpenSession</b> function notifies the Wi-Fi Direct service that the client requests a cancellation of this session. The <b>WFDCancelOpenSession</b> function does not modify the expected <a href="https://msdn.microsoft.com/CF1FF7C2-31CD-4FAB-9891-0A72BEA3E9F1">WFDStartOpenSession</a> behavior. The  callback function specified to the <b>WFDStartOpenSession</b> function will still be called, and the <b>WFDStartOpenSession</b> function may not be completed immediately.

It is the responsibility of the caller to pass the <b>WFDCancelOpenSession</b> function a handle in the <i>hSessionHandle </i>parameter that was returned from call to the <a href="https://msdn.microsoft.com/CF1FF7C2-31CD-4FAB-9891-0A72BEA3E9F1">WFDStartOpenSession</a> function.






## -see-also




<a href="https://msdn.microsoft.com/A27C0AE1-1C51-4CAC-8929-63870ADB15A7">WFDCloseHandle</a>



<a href="https://msdn.microsoft.com/DEAF32C9-64A6-419A-A466-DE2313AE534C">WFDCloseSession</a>



<a href="https://msdn.microsoft.com/D89FAC10-BC33-44BE-ABC8-962241949281">WFDOpenHandle</a>



<a href="https://msdn.microsoft.com/D7BE8108-EF18-49FC-8B14-CED45B6C682B">WFDOpenLegacySession</a>



<a href="https://msdn.microsoft.com/CF1FF7C2-31CD-4FAB-9891-0A72BEA3E9F1">WFDStartOpenSession</a>



<a href="https://msdn.microsoft.com/696B7466-5ED0-4202-9AAF-CE2544C5A5B8">WFDUpdateDeviceVisibility</a>



<a href="https://msdn.microsoft.com/2CB91D70-920A-4D97-B96D-B264F59150AC">WFD_OPEN_SESSION_COMPLETE_CALLBACK</a>
 

 

