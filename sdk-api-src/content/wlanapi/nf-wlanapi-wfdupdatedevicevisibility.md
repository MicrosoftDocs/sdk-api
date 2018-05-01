---
UID: NF:wlanapi.WFDUpdateDeviceVisibility
title: WFDUpdateDeviceVisibility function
author: windows-driver-content
description: Updates device visibility for the Wi-Fi Direct device address for a given installed Wi-Fi Direct device node.
old-location: nwifi\wfdupdatedevicevisibility.htm
old-project: NativeWiFi
ms.assetid: 696B7466-5ED0-4202-9AAF-CE2544C5A5B8
ms.author: windowsdriverdev
ms.date: 4/13/2018
ms.keywords: WFDUpdateDeviceVisibility, WFDUpdateDeviceVisibility function [NativeWIFI], nwifi.wfdupdatedevicevisibility, wlanapi/WFDUpdateDeviceVisibility
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.typenames: WL_DISPLAY_PAGES, *PWL_DISPLAY_PAGES
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	wlanapi.dll
api_name:
-	WFDUpdateDeviceVisibility
product: Windows
targetos: Windows
req.lib: Wlanapi.lib
req.dll: Wlanapi.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# WFDUpdateDeviceVisibility function


## -description


The <b>WFDUpdateDeviceVisibility</b> function  updates device visibility for the Wi-Fi Direct device address for a given installed Wi-Fi Direct device node.


## -parameters




### -param pDeviceAddress

A pointer to the Wi-Fi Direct device address of the client device.

This device address must be obtained from a Device Node created as a result of the Inbox pairing experience. 


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
<dt><b>ERROR_INVALID_PARAMETER</b></dt>
</dl>
</td>
<td width="60%">
The parameter is incorrect. 

This error is returned if the  <i>pDeviceAddress</i> parameter is <b>NULL</b>. 

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_NOT_ENOUGH_MEMORY</b></dt>
</dl>
</td>
<td width="60%">
Not enough storage is available to process this command.

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



The <b>WFDUpdateDeviceVisibility</b> function is part of Wi-Fi Direct, a new feature in Windows 8 and Windows Server 2012. Wi-Fi Direct is based on the development of the Wi-Fi Peer-to-Peer Technical Specification v1.1 by the Wi-Fi Alliance (see <a href="https://www.wi-fi.org/knowledge_center_overview.php?type=4">Wi-Fi Alliance Published Specifications</a>). The goal of the Wi-Fi Peer-to-Peer Technical Specification is to provide a solution for Wi-Fi device-to-device connectivity without the need for either a Wireless Access Point (wireless AP) to setup the connection or the use of the existing Wi-Fi adhoc (IBSS) mechanism. 



The <b>WFDUpdateDeviceVisibility</b> function will perform a targeted Wi-Fi Direct discovery, and will update the DEVPKEY_WiFiDirect_IsVisibile property key on the device node for the given device.




## -see-also




<a href="https://msdn.microsoft.com/0BE3DAED-C9B1-492B-BDFC-CB32BE23E700">WFDCancelOpenSession</a>



<a href="https://msdn.microsoft.com/A27C0AE1-1C51-4CAC-8929-63870ADB15A7">WFDCloseHandle</a>



<a href="https://msdn.microsoft.com/DEAF32C9-64A6-419A-A466-DE2313AE534C">WFDCloseSession</a>



<a href="https://msdn.microsoft.com/D89FAC10-BC33-44BE-ABC8-962241949281">WFDOpenHandle</a>



<a href="https://msdn.microsoft.com/D7BE8108-EF18-49FC-8B14-CED45B6C682B">WFDOpenLegacySession</a>



<a href="https://msdn.microsoft.com/CF1FF7C2-31CD-4FAB-9891-0A72BEA3E9F1">WFDStartOpenSession</a>



<a href="https://msdn.microsoft.com/2CB91D70-920A-4D97-B96D-B264F59150AC">WFD_OPEN_SESSION_COMPLETE_CALLBACK</a>
 

 

