---
UID: NF:ras.RasConnectionNotificationW
title: RasConnectionNotificationW function (ras.h)
description: The RasConnectionNotification function specifies an event object that the system sets to the signaled state when a RAS connection is created or terminated. (Unicode)
helpviewer_keywords: ["RASCN_BandwidthAdded", "RASCN_BandwidthRemoved", "RASCN_Connection", "RASCN_Disconnection", "RasConnectionNotification", "RasConnectionNotification function [RAS]", "RasConnectionNotificationW", "_ras_rasconnectionnotification", "ras/RasConnectionNotification", "ras/RasConnectionNotificationW", "rras.rasconnectionnotification"]
old-location: rras\rasconnectionnotification.htm
tech.root: RRAS
ms.assetid: 7bbf928e-9b62-44fc-9d57-6c80f89865f0
ms.date: 12/05/2018
ms.keywords: RASCN_BandwidthAdded, RASCN_BandwidthRemoved, RASCN_Connection, RASCN_Disconnection, RasConnectionNotification, RasConnectionNotification function [RAS], RasConnectionNotificationA, RasConnectionNotificationW, _ras_rasconnectionnotification, ras/RasConnectionNotification, ras/RasConnectionNotificationA, ras/RasConnectionNotificationW, rras.rasconnectionnotification
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - RasConnectionNotificationW
 - ras/RasConnectionNotificationW
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - ext-ms-win-ras-rasapi32-l1-1-2.dll
 - Rasapi32.dll
 - Ext-MS-Win-ras-rasapi32-l1-1-0.dll
 - Ext-MS-Win-ras-rasapi32-l1-1-1.dll
api_name:
 - RasConnectionNotification
 - RasConnectionNotificationA
 - RasConnectionNotificationW
---

# RasConnectionNotificationW function


## -description

The 
<b>RasConnectionNotification</b> function specifies an event object that the system sets to the signaled state when a RAS connection is created or terminated.

## -parameters

### -param unnamedParam1 [in]

A handle to the RAS connection that receives the notifications. This can be a handle returned by the 
<a href="/windows/desktop/api/ras/nf-ras-rasdiala">RasDial</a> or 
<a href="/windows/desktop/api/ras/nf-ras-rasenumconnectionsa">RasEnumConnections</a> function. If this parameter is <b>INVALID_HANDLE_VALUE</b>, notifications are received for all RAS connections on the local client.

### -param unnamedParam2 [in]

Specifies the handle of an event object. Use the 
<a href="/windows/desktop/api/synchapi/nf-synchapi-createeventa">CreateEvent</a> function to create an event object.

### -param unnamedParam3 [in]

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

## -returns

If the function succeeds, the return value is <b>ERROR_SUCCESS</b>.

If the function fails, the return value is a non-zero error code from <a href="/windows/desktop/RRAS/routing-and-remote-access-error-codes">Routing and Remote Access Error Codes</a> or Winerror.h.

## -remarks

To determine when the event object is signaled, use any of the 
<a href="/windows/desktop/Sync/wait-functions">wait functions</a>.

When the event is signaled, use other RAS functions, such as 
<a href="/windows/desktop/api/ras/nf-ras-rasenumconnectionsa">RasEnumConnections</a>, to get more information about the RAS connection that was created or terminated.





> [!NOTE]
> The ras.h header defines RasConnectionNotification as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/api/synchapi/nf-synchapi-createeventa">CreateEvent</a>



<a href="/windows/desktop/api/ras/nf-ras-rasenumconnectionsa">RasEnumConnections</a>



<a href="/windows/desktop/RRAS/about-remote-access-service">Remote Access Service (RAS) Overview</a>



<a href="/windows/desktop/RRAS/remote-access-service-functions">Remote Access Service Functions</a>
