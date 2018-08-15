---
UID: NF:wlanapi.WFDCloseHandle
title: WFDCloseHandle function
author: windows-sdk-content
description: Closes a handle to the Wi-Fi Direct service.
old-location: nwifi\wfdclosehandle.htm
old-project: nativewifi
ms.assetid: A27C0AE1-1C51-4CAC-8929-63870ADB15A7
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: WFDCloseHandle, WFDCloseHandle function [NativeWIFI], nwifi.wfdclosehandle, wlanapi/WFDCloseHandle
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: wlanapi.h
req.include-header: 
req.redist: 
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
 - WFDCloseHandle
product: Windows
targetos: Windows
req.lib: Wlanapi.lib
req.dll: Wlanapi.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# WFDCloseHandle function


## -description


The <b>WFDCloseHandle</b> function closes a handle to the Wi-Fi Direct service.


## -parameters




### -param hClientHandle [in]

A client handle to the Wi-Fi Direct service. This handle was  obtained by a previous call to the <a href="https://msdn.microsoft.com/D89FAC10-BC33-44BE-ABC8-962241949281">WFDOpenHandle</a> function.


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

This error is returned if the handle specified in the <i>hClientHandle</i>  parameter was not found in the handle table.

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

This error is returned if the <i>hClientHandle</i> parameter is <b>NULL</b> or not valid.

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



The <b>WFDCloseHandle</b> function is part of Wi-Fi Direct, a new feature in Windows 8 and Windows Server 2012. Wi-Fi Direct is based on the development of the Wi-Fi Peer-to-Peer Technical Specification v1.1 by the Wi-Fi Alliance (see <a href="https://www.wi-fi.org/knowledge_center_overview.php?type=4">Wi-Fi Alliance Published Specifications</a>). The goal of the Wi-Fi Peer-to-Peer Technical Specification is to provide a solution for Wi-Fi device-to-device connectivity without the need for either a Wireless Access Point (wireless AP) to setup the connection or the use of the existing Wi-Fi adhoc (IBSS) mechanism. 



In order to use Wi-Fi Direct, an application must first obtain a handle to the Wi-Fi Direct service by calling the <a href="https://msdn.microsoft.com/D89FAC10-BC33-44BE-ABC8-962241949281">WFDOpenHandle</a> function. The Wi-Fi Direct (WFD) handle returned by the  <b>WFDOpenHandle</b> function is used for subsequent calls made to the Wi-Fi Direct service. Once an application is done using the Wi-Fi Direct service, the application should call the <b>WFDCloseHandle</b> function to signal to the Wi-Fi Direct service that the application is done using the service. This allows the  Wi-Fi Direct service  to release resources used by the application.




## -see-also




<a href="https://msdn.microsoft.com/0BE3DAED-C9B1-492B-BDFC-CB32BE23E700">WFDCancelOpenSession</a>



<a href="https://msdn.microsoft.com/DEAF32C9-64A6-419A-A466-DE2313AE534C">WFDCloseSession</a>



<a href="https://msdn.microsoft.com/D89FAC10-BC33-44BE-ABC8-962241949281">WFDOpenHandle</a>



<a href="https://msdn.microsoft.com/D7BE8108-EF18-49FC-8B14-CED45B6C682B">WFDOpenLegacySession</a>



<a href="https://msdn.microsoft.com/CF1FF7C2-31CD-4FAB-9891-0A72BEA3E9F1">WFDStartOpenSession</a>



<a href="https://msdn.microsoft.com/696B7466-5ED0-4202-9AAF-CE2544C5A5B8">WFDUpdateDeviceVisibility</a>



<a href="https://msdn.microsoft.com/2CB91D70-920A-4D97-B96D-B264F59150AC">WFD_OPEN_SESSION_COMPLETE_CALLBACK</a>
 

 

