---
UID: NF:ras.RasConnectionNotificationA
title: RasConnectionNotificationA function
author: windows-sdk-content
description: The RasConnectionNotification function specifies an event object that the system sets to the signaled state when a RAS connection is created or terminated.
old-location: rras\rasconnectionnotification.htm
tech.root: rras
ms.assetid: 7bbf928e-9b62-44fc-9d57-6c80f89865f0
ms.author: windowssdkdev
ms.date: 10/24/2018
ms.keywords: RASCN_BandwidthAdded, RASCN_BandwidthRemoved, RASCN_Connection, RASCN_Disconnection, RasConnectionNotification, RasConnectionNotification function [RAS], RasConnectionNotificationA, RasConnectionNotificationW, _ras_rasconnectionnotification, ras/RasConnectionNotification, ras/RasConnectionNotificationA, ras/RasConnectionNotificationW, rras.rasconnectionnotification
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: ras.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: RasConnectionNotificationW (Unicode) and RasConnectionNotificationA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Rasapi32.lib
req.dll: Rasapi32.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Rasapi32.dll
 - Ext-MS-Win-ras-rasapi32-l1-1-0.dll
 - Ext-MS-Win-ras-rasapi32-l1-1-1.dll
api_name:
 - RasConnectionNotification
 - RasConnectionNotificationA
 - RasConnectionNotificationW
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# RasConnectionNotificationA function


## -description


The 
<b>RasConnectionNotification</b> function specifies an event object that the system sets to the signaled state when a RAS connection is created or terminated.


## -parameters




### -param arg1

TBD


### -param arg2

TBD


### -param arg3

TBD




#### - [in]

A handle to the RAS connection that receives the notifications. This can be a handle returned by the 
<a href="https://msdn.microsoft.com/579a9038-8216-4948-a065-fd45b97da73a">RasDial</a> or 
<a href="https://msdn.microsoft.com/b581cfbf-a55e-4f56-89cd-168aa23af550">RasEnumConnections</a> function. If this parameter is <b>INVALID_HANDLE_VALUE</b>, notifications are received for all RAS connections on the local client.


#### - dwFlags [in]

Specifies the RAS event that causes the system to signal the event object specified by the <i>hEvent</i> parameter. This parameter is a combination of the following values. 



<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="RASCN_Connection"></a><a id="rascn_connection"></a><a id="RASCN_CONNECTION"></a><dl>
<dt><b>RASCN_Connection</b></dt>
</dl>
</td>
<td width="60%">
If <i>hrasconn</i> is <b>INVALID_HANDLE_VALUE</b>, <i>hEvent</i> is signaled when any RAS connection is created.

</td>
</tr>
<tr>
<td width="40%"><a id="RASCN_Disconnection"></a><a id="rascn_disconnection"></a><a id="RASCN_DISCONNECTION"></a><dl>
<dt><b>RASCN_Disconnection</b></dt>
</dl>
</td>
<td width="60%">
<i>hEvent</i> is signaled when the <i>hrasconn</i> connection is terminated. If <i>hrasconn</i> is a multilink connection, the event is signaled when all subentries are disconnected. If <i>hrasconn</i> is <b>INVALID_HANDLE_VALUE</b>, the event is signaled when any RAS connection is terminated.

</td>
</tr>
<tr>
<td width="40%"><a id="RASCN_BandwidthAdded"></a><a id="rascn_bandwidthadded"></a><a id="RASCN_BANDWIDTHADDED"></a><dl>
<dt><b>RASCN_BandwidthAdded</b></dt>
</dl>
</td>
<td width="60%">
<b>Windows NT:  </b>If <i>hrasconn</i> is a handle to a combined multilink connection, <i>hEvent</i> is signaled when a subentry is connected.

</td>
</tr>
<tr>
<td width="40%"><a id="RASCN_BandwidthRemoved"></a><a id="rascn_bandwidthremoved"></a><a id="RASCN_BANDWIDTHREMOVED"></a><dl>
<dt><b>RASCN_BandwidthRemoved</b></dt>
</dl>
</td>
<td width="60%">
<b>Windows NT:  </b>If <i>hrasconn</i> is a handle to a combined multilink connection, <i>hEvent</i> is signaled when a subentry is disconnected.

</td>
</tr>
</table>
 


#### - hEvent [in]

Specifies the handle of an event object. Use the 
<a href="_win32_createevent">CreateEvent</a> function to create an event object.


## -returns



If the function succeeds, the return value is <b>ERROR_SUCCESS</b>.

If the function fails, the return value is a non-zero error code from <a href="https://msdn.microsoft.com/1fa41438-7c93-4e9c-851c-652fba23da4f">Routing and Remote Access Error Codes</a> or Winerror.h.




## -remarks



To determine when the event object is signaled, use any of the 
<a href="_win32_wait_functions">wait functions</a>.

When the event is signaled, use other RAS functions, such as 
<a href="https://msdn.microsoft.com/b581cfbf-a55e-4f56-89cd-168aa23af550">RasEnumConnections</a>, to get more information about the RAS connection that was created or terminated.




## -see-also




<a href="_win32_createevent">CreateEvent</a>



<a href="https://msdn.microsoft.com/b581cfbf-a55e-4f56-89cd-168aa23af550">RasEnumConnections</a>



<a href="https://msdn.microsoft.com/5016fa0b-72eb-484e-b8d7-af9de2e25689">Remote Access Service (RAS) Overview</a>



<a href="https://msdn.microsoft.com/5883a77a-6af8-47a8-bb28-6ef60a5aa2f1">Remote Access Service Functions</a>
 

 

