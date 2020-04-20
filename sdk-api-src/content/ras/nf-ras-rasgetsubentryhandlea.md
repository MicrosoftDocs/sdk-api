---
UID: NF:ras.RasGetSubEntryHandleA
title: RasGetSubEntryHandleA function (ras.h)
description: The RasGetSubEntryHandle function retrieves a connection handle for a specified subentry of a multilink connection.helpviewer_keywords: ["RasGetSubEntryHandle","RasGetSubEntryHandle function [RAS]","RasGetSubEntryHandleA","RasGetSubEntryHandleW","_ras_rasgetsubentryhandle","ras/RasGetSubEntryHandle","ras/RasGetSubEntryHandleA","ras/RasGetSubEntryHandleW","rras.rasgetsubentryhandle"]
old-location: rras\rasgetsubentryhandle.htm
tech.root: RRAS
ms.assetid: 020388b1-9965-4bd1-be7b-30f2127cb0fb
ms.date: 12/05/2018
ms.keywords: RasGetSubEntryHandle, RasGetSubEntryHandle function [RAS], RasGetSubEntryHandleA, RasGetSubEntryHandleW, _ras_rasgetsubentryhandle, ras/RasGetSubEntryHandle, ras/RasGetSubEntryHandleA, ras/RasGetSubEntryHandleW, rras.rasgetsubentryhandle
f1_keywords:
- ras/RasGetSubEntryHandle
dev_langs:
- c++
req.header: ras.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: RasGetSubEntryHandleW (Unicode) and RasGetSubEntryHandleA (ANSI)
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
api_name:
- RasGetSubEntryHandle
- RasGetSubEntryHandleA
- RasGetSubEntryHandleW
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# RasGetSubEntryHandleA function


## -description


The 
<b>RasGetSubEntryHandle</b> function retrieves a connection handle for a specified subentry of a multilink connection.


## -parameters




### -param arg1 [in]

Specifies the <b>HRASCONN</b> connection handle returned by the 
<a href="https://docs.microsoft.com/windows/desktop/api/ras/nf-ras-rasdiala">RasDial</a> function for a multilink phone-book entry.


### -param arg2 [in]

Specifies a valid subentry index for the phone-book entry.


### -param arg3 [out]

Pointer to the <b>HRASCONN</b> variable that receives a connection handle that represents the subentry connection.


## -returns



If the function succeeds, the return value is <b>ERROR_SUCCESS</b>.

If the function fails, the return value is one of the following error codes or a value from <a href="https://docs.microsoft.com/windows/desktop/RRAS/routing-and-remote-access-error-codes">Routing and Remote Access Error Codes</a> or Winerror.h.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_HANDLE</b></dt>
</dl>
</td>
<td width="60%">
The <i>hRasConn</i> connection handle does not represent a connected phone-book entry.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_PORT_NOT_OPEN</b></dt>
</dl>
</td>
<td width="60%">
The <i>hRasConn</i> and <i>dwSubEntry</i> parameters are valid, but the specified subentry is not connected.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_NO_MORE_ITEMS</b></dt>
</dl>
</td>
<td width="60%">
The value specified by <i>dwSubEntry</i> exceeds the maximum number of subentries for the phone-book entry.

</td>
</tr>
</table>
 




## -remarks



The connection handle specified in the <i>hRasConn</i> parameter refers to the entire multilink connection, but the connection handle returned in the <i>*lphRasConn</i> parameter refers only to the subentry connection. Use the subentry connection handle in any function that accepts an <i>hRasConn</i> parameter, including the 
<a href="https://docs.microsoft.com/windows/desktop/api/ras/nf-ras-rashangupa">RasHangUp</a>, 
<a href="https://docs.microsoft.com/windows/desktop/api/ras/nf-ras-rasgetconnectstatusa">RasGetConnectStatus</a>, and 
<a href="https://docs.microsoft.com/windows/desktop/api/ras/nf-ras-rasgetprojectioninfoa">RasGetProjectionInfo</a> functions. The projection information returned by 
<b>RasGetProjectionInfo</b> for a multilink entry is the same for the each of the subentry connection handles as it is for the main connection handle.

You can call 
<a href="https://docs.microsoft.com/windows/desktop/api/ras/nf-ras-rashangupa">RasHangUp</a> on the handle returned by 
<b>RasGetSubEntryHandle</b> to terminate a single link in a multi-link connection. However, you cannot use 
<a href="https://docs.microsoft.com/windows/desktop/api/ras/nf-ras-rasgetconnectstatusa">RasGetConnectStatus</a> to determine if the link terminated; 
<b>RasGetConnectStatus</b> may not return ERROR_INVALID_HANDLE even though the link terminated successfully.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/ras/nf-ras-rasdiala">RasDial</a>



<a href="https://docs.microsoft.com/windows/desktop/api/ras/nf-ras-rasgetconnectstatusa">RasGetConnectStatus</a>



<a href="https://docs.microsoft.com/windows/desktop/api/ras/nf-ras-rasgetprojectioninfoa">RasGetProjectionInfo</a>



<a href="https://docs.microsoft.com/windows/desktop/api/ras/nf-ras-rashangupa">RasHangUp</a>



<a href="https://docs.microsoft.com/windows/desktop/RRAS/about-remote-access-service">Remote Access Service (RAS) Overview</a>



<a href="https://docs.microsoft.com/windows/desktop/RRAS/remote-access-service-functions">Remote Access Service Functions</a>
 

 

