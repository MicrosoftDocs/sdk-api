---
UID: NF:ras.RasGetProjectionInfoA
title: RasGetProjectionInfoA function (ras.h)
description: The RasGetProjectionInfo function obtains information about a remote access projection operation for a specified remote access component protocol.
helpviewer_keywords: ["RASP_Amb", "RASP_PppCcp", "RASP_PppIp", "RASP_PppIpv6", "RASP_PppIpx", "RASP_PppLcp", "RASP_PppNbf", "RASP_Slip", "RasGetProjectionInfoA", "ras/RasGetProjectionInfoA"]
old-location: rras\rasgetprojectioninfo.htm
tech.root: RRAS
ms.assetid: 97ae09c3-588a-4dd2-9756-ddcd5fa37f51
ms.date: 12/05/2018
ms.keywords: RASP_Amb, RASP_PppCcp, RASP_PppIp, RASP_PppIpv6, RASP_PppIpx, RASP_PppLcp, RASP_PppNbf, RASP_Slip, RasGetProjectionInfo, RasGetProjectionInfo function [RAS], RasGetProjectionInfoA, RasGetProjectionInfoW, _ras_rasgetprojectioninfo, ras/RasGetProjectionInfo, ras/RasGetProjectionInfoA, ras/RasGetProjectionInfoW, rras.rasgetprojectioninfo
f1_keywords:
- ras/RasGetProjectionInfo
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
req.unicode-ansi: RasGetProjectionInfoW (Unicode) and RasGetProjectionInfoA (ANSI)
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
- ext-ms-win-ras-rasapi32-l1-1-2.dll
api_name:
- RasGetProjectionInfo
- RasGetProjectionInfoA
- RasGetProjectionInfoW
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# RasGetProjectionInfoA function


## -description


The 
<b>RasGetProjectionInfo</b> function obtains information about a remote access projection operation for a specified remote access component protocol.


## -parameters




### -param unnamedParam1 [in]

Handle to the remote access connection of interest. An application obtains a RAS connection handle from the 
<a href="/windows/desktop/api/ras/nf-ras-rasdiala">RasDial</a> or 
<a href="/windows/desktop/api/ras/nf-ras-rasenumconnectionsa">RasEnumConnections</a> function.


### -param unnamedParam2 [in]

Specifies the 
<a href="/previous-versions/windows/desktop/legacy/aa377648(v=vs.85)">RASPROJECTION</a> enumerated type value that identifies the protocol of interest.
					


### -param unnamedParam3 [out]

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

<a href="/previous-versions/windows/desktop/legacy/aa376720(v=vs.85)">RASAMB</a>


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

<a href="/previous-versions/windows/desktop/legacy/aa377620(v=vs.85)">RASPPPCCP</a>


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

<a href="/previous-versions/windows/desktop/legacy/aa377634(v=vs.85)">RASPPPIP</a>


</td>
</tr>
<tr>
<td width="40%"><a id="RASP_PppIpv6"></a><a id="rasp_pppipv6"></a><a id="RASP_PPPIPV6"></a><dl>
<dt><b>RASP_PppIpv6</b></dt>
</dl>
</td>
<td width="60%">

<a href="/previous-versions/windows/desktop/legacy/aa816540(v=vs.85)">RASPPPIPV6</a>


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

<a href="/previous-versions/windows/desktop/legacy/aa377623(v=vs.85)">RASPPPIPX</a>


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

<a href="/previous-versions/windows/desktop/legacy/aa377638(v=vs.85)">RASPPPLCP</a>


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

<a href="/previous-versions/windows/desktop/legacy/aa377642(v=vs.85)">RASPPPNBF</a>


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

<a href="/previous-versions/windows/desktop/legacy/aa377836(v=vs.85)">RASPSLIP</a>


<div class="alert"><b>Note</b>  Supported on Windows Server 2003 or earlier.</div>
<div> </div>
</td>
</tr>
</table>
 


### -param unnamedParam4 [in, out]

Pointer to a variable that, on input, specifies the size, in bytes, of the buffer pointed to by <i>lpprojection</i>. 




On output, this variable receives the size, in bytes, of the <i>lpprojection</i> buffer.


## -returns



If the function succeeds, the return value is <b>ERROR_SUCCESS</b>.

If the function fails, the return value is one of the following error codes or a value from <a href="/windows/desktop/RRAS/routing-and-remote-access-error-codes">Routing and Remote Access Error Codes</a> or Winerror.h.

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
<a href="/windows/desktop/api/ras/nf-ras-rasdiala">RasDial</a>
<a href="/previous-versions/windows/desktop/legacy/aa376727(v=vs.85)">RASCS_Projected</a> state on the remote access connection. If 
<b>RasGetProjectionInfo</b> is called prior to the <b>RASCS_Projected</b> state, it returns <b>ERROR_PROJECTION_NOT_COMPLETE</b>.

The NetBEUI protocol and authentication message blocks (AMB) are only supported on Windows 2000 and earlier versions of Windows.





> [!NOTE]
> The ras.h header defines RasGetProjectionInfo as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also




<a href="/previous-versions/windows/desktop/legacy/aa376720(v=vs.85)">RASAMB</a>



<a href="/previous-versions/windows/desktop/legacy/aa377620(v=vs.85)">RASPPPCCP</a>



<a href="/previous-versions/windows/desktop/legacy/aa377634(v=vs.85)">RASPPPIP</a>



<a href="/previous-versions/windows/desktop/legacy/aa816540(v=vs.85)">RASPPPIPV6</a>



<a href="/previous-versions/windows/desktop/legacy/aa377623(v=vs.85)">RASPPPIPX</a>



<a href="/previous-versions/windows/desktop/legacy/aa377638(v=vs.85)">RASPPPLCP</a>



<a href="/previous-versions/windows/desktop/legacy/aa377642(v=vs.85)">RASPPPNBF</a>



<a href="/previous-versions/windows/desktop/legacy/aa377648(v=vs.85)">RASPROJECTION</a>



<a href="/previous-versions/windows/desktop/legacy/aa377836(v=vs.85)">RASPSLIP</a>



<a href="/windows/desktop/api/ras/nf-ras-rasdiala">RasDial</a>



<a href="/windows/desktop/api/ras/nf-ras-rasenumconnectionsa">RasEnumConnections</a>



<a href="/windows/desktop/RRAS/about-remote-access-service">Remote Access Service (RAS) Overview</a>



<a href="/windows/desktop/RRAS/remote-access-service-functions">Remote Access Service Functions</a>
 

 
