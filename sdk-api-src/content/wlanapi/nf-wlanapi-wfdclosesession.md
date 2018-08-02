---
UID: NF:wlanapi.WFDCloseSession
title: WFDCloseSession function
author: windows-sdk-content
description: Closes a session after a previously successful call to the WFDStartOpenSession function.
old-location: nwifi\wfdclosesession.htm
old-project: NativeWiFi
ms.assetid: DEAF32C9-64A6-419A-A466-DE2313AE534C
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: WFDCloseSession, WFDCloseSession function [NativeWIFI], nwifi.wfdclosesession, wlanapi/WFDCloseSession
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: wlanapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
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
req.typenames: WL_DISPLAY_PAGES, *PWL_DISPLAY_PAGES
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - wlanapi.dll
api_name:
 - WFDCloseSession
product: Windows
targetos: Windows
req.lib: Wlanapi.lib
req.dll: Wlanapi.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# WFDCloseSession function


## -description


The  <b>WFDCloseSession</b> function closes a session after a previously successful call to the <a href="https://msdn.microsoft.com/CF1FF7C2-31CD-4FAB-9891-0A72BEA3E9F1">WFDStartOpenSession</a> function.


## -parameters




### -param hSessionHandle [in]

A session handle to a Wi-Fi Direct session. This is a session handle previously returned by the <a href="https://msdn.microsoft.com/CF1FF7C2-31CD-4FAB-9891-0A72BEA3E9F1">WFDStartOpenSession</a> function.


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
<dt><b>ERROR_INVALID_STATE</b></dt>
</dl>
</td>
<td width="60%">
The group or resource is not in the correct state to perform the requested operation.

This error is returned if the Wi-Fi Direct service is disabled by group policy on a domain.

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



The <b>WFDCloseSession</b> function is part of Wi-Fi Direct, a new feature in Windows 8 and Windows Server 2012. Wi-Fi Direct is based on the development of the Wi-Fi Peer-to-Peer Technical Specification v1.1 by the Wi-Fi Alliance (see <a href="https://www.wi-fi.org/knowledge_center_overview.php?type=4">Wi-Fi Alliance Published Specifications</a>). The goal of the Wi-Fi Peer-to-Peer Technical Specification is to provide a solution for Wi-Fi device-to-device connectivity without the need for either a Wireless Access Point (wireless AP) to setup the connection or the use of the existing Wi-Fi adhoc (IBSS) mechanism. 



The  <b>WFDCloseSession</b> function queues a future work item to close the session, so disconnection may not be immediate.



Calling the  <b>WFDCloseSession</b> function  while a <a href="https://msdn.microsoft.com/CF1FF7C2-31CD-4FAB-9891-0A72BEA3E9F1">WFDStartOpenSession</a> call is pending will not close the session.


It is the responsibility of the caller to pass the <b>WFDCloseSession</b> function a handle in the <i>hSessionHandle </i>parameter that was returned from a successful asynchronous call to the <a href="https://msdn.microsoft.com/CF1FF7C2-31CD-4FAB-9891-0A72BEA3E9F1">WFDStartOpenSession</a> function.



Calling the  <b>WFDCloseSession</b> function with a handle that was valid and has become invalid will yield undefined results.





## -see-also




<a href="https://msdn.microsoft.com/0BE3DAED-C9B1-492B-BDFC-CB32BE23E700">WFDCancelOpenSession</a>



<a href="https://msdn.microsoft.com/A27C0AE1-1C51-4CAC-8929-63870ADB15A7">WFDCloseHandle</a>



<a href="https://msdn.microsoft.com/D89FAC10-BC33-44BE-ABC8-962241949281">WFDOpenHandle</a>



<a href="https://msdn.microsoft.com/D7BE8108-EF18-49FC-8B14-CED45B6C682B">WFDOpenLegacySession</a>



<a href="https://msdn.microsoft.com/CF1FF7C2-31CD-4FAB-9891-0A72BEA3E9F1">WFDStartOpenSession</a>



<a href="https://msdn.microsoft.com/696B7466-5ED0-4202-9AAF-CE2544C5A5B8">WFDUpdateDeviceVisibility</a>



<a href="https://msdn.microsoft.com/2CB91D70-920A-4D97-B96D-B264F59150AC">WFD_OPEN_SESSION_COMPLETE_CALLBACK</a>
 

 

