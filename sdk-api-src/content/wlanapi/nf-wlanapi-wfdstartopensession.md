---
UID: NF:wlanapi.WFDStartOpenSession
title: WFDStartOpenSession function
author: windows-sdk-content
description: Starts an on-demand connection to a specific Wi-Fi Direct device, which has been previously paired through the Windows Pairing experience.
old-location: nwifi\wfdstartopensession.htm
old-project: NativeWiFi
ms.assetid: CF1FF7C2-31CD-4FAB-9891-0A72BEA3E9F1
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: WFDStartOpenSession, WFDStartOpenSession function [NativeWIFI], nwifi.wfdstartopensession, wlanapi/WFDStartOpenSession
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
 - WFDStartOpenSession
product: Windows
targetos: Windows
req.lib: Wlanapi.lib
req.dll: Wlanapi.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# WFDStartOpenSession function


## -description


The  <b>WFDStartOpenSession</b> function starts an on-demand connection to a specific Wi-Fi Direct device, which has been previously paired through the Windows Pairing experience.


## -parameters




### -param hClientHandle [in]

A client handle to the Wi-Fi Direct service. This handle was  obtained by a previous call to the <a href="https://msdn.microsoft.com/D89FAC10-BC33-44BE-ABC8-962241949281">WFDOpenHandle</a> function.


### -param pDeviceAddress [in]

A pointer to the target device’s Wi-Fi Direct device address. This is the MAC address of the target Wi-Fi device. 


### -param pvContext [in, optional]

An optional context pointer which is passed to the callback function specified in the <i>pfnCallback</i> parameter.


### -param pfnCallback [in]

A pointer to the callback function to be called once the <b>WFDStartOpenSession</b> request has completed.


### -param phSessionHandle [out]

A handle to this specific Wi-Fi Direct session.


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

This error is returned if the <i>hClientHandle</i> parameter is <b>NULL</b> or not valid. This error is also returned if the <i>pDeviceAddress</i> parameter is <b>NULL</b>, the <i>pfnCallback</i> parameter is <b>NULL</b>, or the <i>phSessionHandle</i> parameter is <b>NULL</b>. This value is also returned if the <i>dwClientVersion</i> parameter is not equal to <b>WFD_API_VERSION</b>.

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
<dt><b>ERROR_SERVICE_NOT_ACTIVE</b></dt>
</dl>
</td>
<td width="60%">
The service has not been started.

This error is returned if the WLAN AutoConfig Service is not running.

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



The <b>WFDStartOpenSession</b> function is part of Wi-Fi Direct, a new feature in Windows 8 and Windows Server 2012. Wi-Fi Direct is based on the development of the Wi-Fi Peer-to-Peer Technical Specification v1.1 by the Wi-Fi Alliance (see <a href="https://www.wi-fi.org/knowledge_center_overview.php?type=4">Wi-Fi Alliance Published Specifications</a>). The goal of the Wi-Fi Peer-to-Peer Technical Specification is to provide a solution for Wi-Fi device-to-device connectivity without the need for either a Wireless Access Point (wireless AP) to setup the connection or the use of the existing Wi-Fi adhoc (IBSS) mechanism. 



The  <b>WFDStartOpenSession</b> function starts an asynchronous operation to start an on-demand connection to  a specific Wi-Fi Direct device. The target Wi-Fi device must previously have been paired through the Windows Pairing experience. When the asynchronous operation completes, the callback function specified in the <i>pfnCallback</i> parameter is called.  

If the application attempts to close the handle to the Wi-Fi Direct service by calling the <a href="https://msdn.microsoft.com/A27C0AE1-1C51-4CAC-8929-63870ADB15A7">WFDCloseHandle</a> function before the <b>WFDStartOpenSession</b> function completes asynchronously, the <b>WFDCloseHandle</b> function will wait until the <b>WFDStartOpenSession</b> call is completed.




## -see-also




<a href="https://msdn.microsoft.com/0BE3DAED-C9B1-492B-BDFC-CB32BE23E700">WFDCancelOpenSession</a>



<a href="https://msdn.microsoft.com/A27C0AE1-1C51-4CAC-8929-63870ADB15A7">WFDCloseHandle</a>



<a href="https://msdn.microsoft.com/DEAF32C9-64A6-419A-A466-DE2313AE534C">WFDCloseSession</a>



<a href="https://msdn.microsoft.com/D89FAC10-BC33-44BE-ABC8-962241949281">WFDOpenHandle</a>



<a href="https://msdn.microsoft.com/D7BE8108-EF18-49FC-8B14-CED45B6C682B">WFDOpenLegacySession</a>



<a href="https://msdn.microsoft.com/696B7466-5ED0-4202-9AAF-CE2544C5A5B8">WFDUpdateDeviceVisibility</a>



<a href="https://msdn.microsoft.com/2CB91D70-920A-4D97-B96D-B264F59150AC">WFD_OPEN_SESSION_COMPLETE_CALLBACK</a>
 

 

