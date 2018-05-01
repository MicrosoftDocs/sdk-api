---
UID: NF:ras.RasGetProjectionInfoW
title: RasGetProjectionInfoW function
author: windows-driver-content
description: The RasGetProjectionInfo function obtains information about a remote access projection operation for a specified remote access component protocol.
old-location: rras\rasgetprojectioninfo.htm
old-project: RRAS
ms.assetid: 97ae09c3-588a-4dd2-9756-ddcd5fa37f51
ms.author: windowsdriverdev
ms.date: 4/16/2018
ms.keywords: RASP_Amb, RASP_PppCcp, RASP_PppIp, RASP_PppIpv6, RASP_PppIpx, RASP_PppLcp, RASP_PppNbf, RASP_Slip, RasGetProjectionInfo, RasGetProjectionInfo function [RAS], RasGetProjectionInfoA, RasGetProjectionInfoW, _ras_rasgetprojectioninfo, ras/RasGetProjectionInfo, ras/RasGetProjectionInfoA, ras/RasGetProjectionInfoW, rras.rasgetprojectioninfo
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
req.unicode-ansi: RasGetProjectionInfoW (Unicode) and RasGetProjectionInfoA (ANSI)
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
-	Ext-MS-Win-ras-rasapi32-l1-1-0.dll
-	Ext-MS-Win-ras-rasapi32-l1-1-1.dll
api_name:
-	RasGetProjectionInfo
-	RasGetProjectionInfoA
-	RasGetProjectionInfoW
product: Windows
targetos: Windows
req.lib: Rasapi32.lib
req.dll: Rasapi32.dll
req.irql: 
req.product: Rights Management Services client 1.0 SP2 or later
---

# RasGetProjectionInfoW function


## -description


The 
<b>RasGetProjectionInfo</b> function obtains information about a remote access projection operation for a specified remote access component protocol.


## -parameters




### -param

TBD




#### - hrasconn [in]

Handle to the remote access connection of interest. An application obtains a RAS connection handle from the 
<a href="https://msdn.microsoft.com/579a9038-8216-4948-a065-fd45b97da73a">RasDial</a> or 
<a href="https://msdn.microsoft.com/b581cfbf-a55e-4f56-89cd-168aa23af550">RasEnumConnections</a> function.


#### - lpcb [in, out]

Pointer to a variable that, on input, specifies the size, in bytes, of the buffer pointed to by <i>lpprojection</i>. 




On output, this variable receives the size, in bytes, of the <i>lpprojection</i> buffer.


#### - lpprojection [out]

Pointer to a buffer that receives the information specified by the <i>rasprojection</i> parameter. The information is in a structure appropriate to the <i>rasprojection</i> value. 



<table>
<tr>
<th>rasprojection value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="RASP_Amb"></a><a id="rasp_amb"></a><a id="RASP_AMB"></a><dl>
<dt><b>RASP_Amb</b></dt>
</dl>
</td>
<td width="60%">

<a href="https://msdn.microsoft.com/87f95e61-be95-4f42-b556-901516b364d6">RASAMB</a>


<div class="alert"><b>Note</b>  Supported on Windows 2000 or earlier.</div>
<div> </div>
</td>
</tr>
<tr>
<td width="40%"><a id="RASP_PppCcp"></a><a id="rasp_pppccp"></a><a id="RASP_PPPCCP"></a><dl>
<dt><b>RASP_PppCcp</b></dt>
</dl>
</td>
<td width="60%">

<a href="https://msdn.microsoft.com/1ce6bbaf-c042-4c6e-a7c6-f3e8aa933789">RASPPPCCP</a>


<div class="alert"><b>Note</b>  Supported on Windows 2000 or later.</div>
<div> </div>
</td>
</tr>
<tr>
<td width="40%"><a id="RASP_PppIp"></a><a id="rasp_pppip"></a><a id="RASP_PPPIP"></a><dl>
<dt><b>RASP_PppIp</b></dt>
</dl>
</td>
<td width="60%">

<a href="https://msdn.microsoft.com/bc2f4a40-a0bc-46f1-af98-b60be418eb0e">RASPPPIP</a>


</td>
</tr>
<tr>
<td width="40%"><a id="RASP_PppIpv6"></a><a id="rasp_pppipv6"></a><a id="RASP_PPPIPV6"></a><dl>
<dt><b>RASP_PppIpv6</b></dt>
</dl>
</td>
<td width="60%">

<a href="https://msdn.microsoft.com/553b654c-ee1d-4a12-9740-6375a62a5bde">RASPPPIPV6</a>


<div class="alert"><b>Note</b>  Supported on Windows Vista or later.</div>
<div> </div>
</td>
</tr>
<tr>
<td width="40%"><a id="RASP_PppIpx"></a><a id="rasp_pppipx"></a><a id="RASP_PPPIPX"></a><dl>
<dt><b>RASP_PppIpx</b></dt>
</dl>
</td>
<td width="60%">

<a href="https://msdn.microsoft.com/db38d723-80d1-4107-9cd4-2b055649608c">RASPPPIPX</a>


<div class="alert"><b>Note</b>  Not supported on 64-bit Microsoft Windows.</div>
<div> </div>
</td>
</tr>
<tr>
<td width="40%"><a id="RASP_PppLcp"></a><a id="rasp_ppplcp"></a><a id="RASP_PPPLCP"></a><dl>
<dt><b>RASP_PppLcp</b></dt>
</dl>
</td>
<td width="60%">

<a href="https://msdn.microsoft.com/f6aaff96-1fb0-412e-b470-14d841f99c45">RASPPPLCP</a>


<div class="alert"><b>Note</b>  Supported on Windows 2000 or later.</div>
<div> </div>
</td>
</tr>
<tr>
<td width="40%"><a id="RASP_PppNbf"></a><a id="rasp_pppnbf"></a><a id="RASP_PPPNBF"></a><dl>
<dt><b>RASP_PppNbf</b></dt>
</dl>
</td>
<td width="60%">

<a href="https://msdn.microsoft.com/262cfc78-a0b9-4fb4-bfc0-ba1f1192a435">RASPPPNBF</a>


<div class="alert"><b>Note</b>  Supported on Windows 2000 or earlier.</div>
<div> </div>
</td>
</tr>
<tr>
<td width="40%"><a id="RASP_Slip"></a><a id="rasp_slip"></a><a id="RASP_SLIP"></a><dl>
<dt><b>RASP_Slip</b></dt>
</dl>
</td>
<td width="60%">

<a href="https://msdn.microsoft.com/74c7d250-ddb1-4d89-a840-b26613c8fcd6">RASPSLIP</a>


<div class="alert"><b>Note</b>  Supported on Windows Server 2003 or earlier.</div>
<div> </div>
</td>
</tr>
</table>
 


#### - rasprojection [in]

Specifies the 
<a href="https://msdn.microsoft.com/589fc4b0-16f0-4728-ad8d-7a91d7b52fba">RASPROJECTION</a> enumerated type value that identifies the protocol of interest.
					


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
<dt><b>ERROR_BUFFER_TOO_SMALL</b></dt>
</dl>
</td>
<td width="60%">
The buffer pointed to by <i>lpprojection</i> is not large enough to contain the requested information.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_HANDLE</b></dt>
</dl>
</td>
<td width="60%">
The <i>hrasconn</i> parameter is not a valid handle.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_PARAMETER</b></dt>
</dl>
</td>
<td width="60%">
One of the parameters is invalid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_SIZE</b></dt>
</dl>
</td>
<td width="60%">
The <b>dwSize</b> member of the structure pointed to by <i>lpprojection</i> specifies an invalid size.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_PROTOCOL_NOT_CONFIGURED</b></dt>
</dl>
</td>
<td width="60%">
The control protocol for which information was requested neither succeeded nor failed, because the connection's phone-book entry did not require that an attempt to negotiate the protocol be made. This is a RAS error code.

</td>
</tr>
</table>
 




## -remarks



Remote access projection is the process whereby a remote access server and a remote client negotiate network protocol-specific information. A remote access server uses this network protocol-specific information to represent a remote client on the network.

Remote access projection information is not available until the operating system has executed the 
<a href="https://msdn.microsoft.com/579a9038-8216-4948-a065-fd45b97da73a">RasDial</a>
<a href="https://msdn.microsoft.com/42047265-1b0f-4449-842c-e860b8fb6728">RASCS_Projected</a> state on the remote access connection. If 
<b>RasGetProjectionInfo</b> is called prior to the <b>RASCS_Projected</b> state, it returns <b>ERROR_PROJECTION_NOT_COMPLETE</b>.

The NetBEUI protocol and authentication message blocks (AMB) are only supported on Windows 2000 and earlier versions of Windows.




## -see-also




<a href="https://msdn.microsoft.com/87f95e61-be95-4f42-b556-901516b364d6">RASAMB</a>



<a href="https://msdn.microsoft.com/1ce6bbaf-c042-4c6e-a7c6-f3e8aa933789">RASPPPCCP</a>



<a href="https://msdn.microsoft.com/bc2f4a40-a0bc-46f1-af98-b60be418eb0e">RASPPPIP</a>



<a href="https://msdn.microsoft.com/553b654c-ee1d-4a12-9740-6375a62a5bde">RASPPPIPV6</a>



<a href="https://msdn.microsoft.com/db38d723-80d1-4107-9cd4-2b055649608c">RASPPPIPX</a>



<a href="https://msdn.microsoft.com/f6aaff96-1fb0-412e-b470-14d841f99c45">RASPPPLCP</a>



<a href="https://msdn.microsoft.com/262cfc78-a0b9-4fb4-bfc0-ba1f1192a435">RASPPPNBF</a>



<a href="https://msdn.microsoft.com/589fc4b0-16f0-4728-ad8d-7a91d7b52fba">RASPROJECTION</a>



<a href="https://msdn.microsoft.com/74c7d250-ddb1-4d89-a840-b26613c8fcd6">RASPSLIP</a>



<a href="https://msdn.microsoft.com/579a9038-8216-4948-a065-fd45b97da73a">RasDial</a>



<a href="https://msdn.microsoft.com/b581cfbf-a55e-4f56-89cd-168aa23af550">RasEnumConnections</a>



<a href="https://msdn.microsoft.com/5016fa0b-72eb-484e-b8d7-af9de2e25689">Remote Access Service (RAS) Overview</a>



<a href="https://msdn.microsoft.com/5883a77a-6af8-47a8-bb28-6ef60a5aa2f1">Remote Access Service Functions</a>
 

 

