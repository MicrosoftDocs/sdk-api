---
UID: NF:ras.RasGetSubEntryHandleA
title: RasGetSubEntryHandleA function
author: windows-driver-content
description: The RasGetSubEntryHandle function retrieves a connection handle for a specified subentry of a multilink connection.
old-location: rras\rasgetsubentryhandle.htm
old-project: RRAS
ms.assetid: 020388b1-9965-4bd1-be7b-30f2127cb0fb
ms.author: windowsdriverdev
ms.date: 5/9/2018
ms.keywords: RasGetSubEntryHandle, RasGetSubEntryHandle function [RAS], RasGetSubEntryHandleA, RasGetSubEntryHandleW, _ras_rasgetsubentryhandle, ras/RasGetSubEntryHandle, ras/RasGetSubEntryHandleA, ras/RasGetSubEntryHandleW, rras.rasgetsubentryhandle
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
req.unicode-ansi: RasGetSubEntryHandleW (Unicode) and RasGetSubEntryHandleA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: RASPROJECTION_INFO_TYPE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	Rasapi32.dll
api_name:
-	RasGetSubEntryHandle
-	RasGetSubEntryHandleA
-	RasGetSubEntryHandleW
product: Windows
targetos: Windows
req.lib: Rasapi32.lib
req.dll: Rasapi32.dll
req.irql: 
req.product: Rights Management Services client 1.0 SP2 or later
---

# RasGetSubEntryHandleA function


## -description


The 
<b>RasGetSubEntryHandle</b> function retrieves a connection handle for a specified subentry of a multilink connection.


## -parameters




### -param

TBD




#### - dwSubEntry [in]

Specifies a valid subentry index for the phone-book entry.


#### - hRasConn [in]

Specifies the <b>HRASCONN</b> connection handle returned by the 
<a href="https://msdn.microsoft.com/579a9038-8216-4948-a065-fd45b97da73a">RasDial</a> function for a multilink phone-book entry.


#### - lphRasConn [out]

Pointer to the <b>HRASCONN</b> variable that receives a connection handle that represents the subentry connection.


## -returns



If the function succeeds, the return value is <b>ERROR_SUCCESS</b>.

If the function fails, the return value is one of the following error codes or a value from <a href="https://msdn.microsoft.com/1fa41438-7c93-4e9c-851c-652fba23da4f">Routing and Remote Access Error Codes</a> or Winerror.h.

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
<a href="https://msdn.microsoft.com/b5720ddf-c7ac-439e-97cb-62240122a775">RasHangUp</a>, 
<a href="https://msdn.microsoft.com/3b2a2f8d-b1ff-44d2-ba49-60877ca6c104">RasGetConnectStatus</a>, and 
<a href="https://msdn.microsoft.com/97ae09c3-588a-4dd2-9756-ddcd5fa37f51">RasGetProjectionInfo</a> functions. The projection information returned by 
<b>RasGetProjectionInfo</b> for a multilink entry is the same for the each of the subentry connection handles as it is for the main connection handle.

You can call 
<a href="https://msdn.microsoft.com/b5720ddf-c7ac-439e-97cb-62240122a775">RasHangUp</a> on the handle returned by 
<b>RasGetSubEntryHandle</b> to terminate a single link in a multi-link connection. However, you cannot use 
<a href="https://msdn.microsoft.com/3b2a2f8d-b1ff-44d2-ba49-60877ca6c104">RasGetConnectStatus</a> to determine if the link terminated; 
<b>RasGetConnectStatus</b> may not return ERROR_INVALID_HANDLE even though the link terminated successfully.




## -see-also




<a href="https://msdn.microsoft.com/579a9038-8216-4948-a065-fd45b97da73a">RasDial</a>



<a href="https://msdn.microsoft.com/3b2a2f8d-b1ff-44d2-ba49-60877ca6c104">RasGetConnectStatus</a>



<a href="https://msdn.microsoft.com/97ae09c3-588a-4dd2-9756-ddcd5fa37f51">RasGetProjectionInfo</a>



<a href="https://msdn.microsoft.com/b5720ddf-c7ac-439e-97cb-62240122a775">RasHangUp</a>



<a href="https://msdn.microsoft.com/5016fa0b-72eb-484e-b8d7-af9de2e25689">Remote Access Service (RAS) Overview</a>



<a href="https://msdn.microsoft.com/5883a77a-6af8-47a8-bb28-6ef60a5aa2f1">Remote Access Service Functions</a>
 

 

