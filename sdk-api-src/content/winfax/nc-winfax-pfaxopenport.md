---
UID: NC:winfax.PFAXOPENPORT
title: PFAXOPENPORT (winfax.h)
description: The FaxOpenPort function returns a fax port handle to a fax client application. The port handle is required when the application calls other fax client functions that facilitate device management and fax document routing.
helpviewer_keywords: ["FaxOpenPortA","FaxOpenPortW","PFAXOPENPORT","PFAXOPENPORT callback","PFAXOPENPORT callback function [Fax Service]","PORT_OPEN_MODIFY","PORT_OPEN_QUERY","_mfax_faxopenport","fax._mfax_faxopenport","winfax/FaxOpenPortA","winfax/FaxOpenPortW","winfax/PFAXOPENPORT"]
old-location: fax\_mfax_faxopenport.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxlegacy_15ro.htm
ms.date: 12/05/2018
ms.keywords: FaxOpenPortA, FaxOpenPortW, PFAXOPENPORT, PFAXOPENPORT callback, PFAXOPENPORT callback function [Fax Service], PORT_OPEN_MODIFY, PORT_OPEN_QUERY, _mfax_faxopenport, fax._mfax_faxopenport, winfax/FaxOpenPortA, winfax/FaxOpenPortW, winfax/PFAXOPENPORT
req.header: winfax.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: FaxOpenPortW (Unicode) and FaxOpenPortA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - PFAXOPENPORT
 - winfax/PFAXOPENPORT
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - Winfax.h
api_name:
 - PFAXOPENPORT
 - FaxOpenPortA
 - FaxOpenPortW
---

# PFAXOPENPORT callback function


## -description

The <b>FaxOpenPort</b> function returns a fax port handle to a fax client application. The port handle is required when the application calls other fax client functions that facilitate device management and fax document routing.

## -parameters

### -param FaxHandle [in]

Type: <b>HANDLE</b>

Specifies a fax server handle returned by a call to the <a href="/previous-versions/windows/desktop/api/winfax/nf-winfax-faxconnectfaxservera">FaxConnectFaxServer</a> function.

### -param DeviceId [in]

Type: <b>DWORD</b>

Specifies a <b>DWORD</b> variable that is the permanent line identifier for the receiving device. Call the <a href="/previous-versions/windows/desktop/api/winfax/nf-winfax-faxenumportsa">FaxEnumPorts</a> function to retrieve a valid value for this parameter. For more information, see the following Remarks section.

### -param Flags [in]

Type: <b>DWORD</b>

Specifies a <b>DWORD</b> variable that contains a set of bit flags that defines the access level for the port. This parameter can be one or more of the following values.



#### PORT_OPEN_QUERY

Port access level required to obtain a fax port handle. This access level is also required to call the <a href="/previous-versions/windows/desktop/api/winfax/nf-winfax-faxgetporta">FaxGetPort</a> function to query fax port information.



#### PORT_OPEN_MODIFY

Port access level required to change the configuration of a fax port with a call to the <a href="/previous-versions/windows/desktop/api/winfax/nf-winfax-faxgetporta">FaxGetPort</a> function. This access level also includes the access rights associated with the <a href="/previous-versions/windows/desktop/fax/-mfax-fax-port-access-levels">PORT_OPEN_QUERY</a> access level.

### -param FaxPortHandle [out]

Type: <b>LPHANDLE</b>

Pointer to a variable that receives a fax port handle that is required on subsequent calls to other fax client functions. If the fax server returns a <b>NULL</b> handle, it indicates an error.

## -returns

Type: <b>BOOL</b>

If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>. GetLastError can return one of the following errors.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_ACCESS_DENIED</b></dt>
</dl>
</td>
<td width="60%">
Access is denied. <a href="/previous-versions/windows/desktop/fax/-mfax-specific-fax-access-rights">FAX_PORT_QUERY</a> access is required.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_NOT_ENOUGH_MEMORY</b></dt>
</dl>
</td>
<td width="60%">
An error occurred during memory allocation.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_HANDLE</b></dt>
</dl>
</td>
<td width="60%">
The port has already been opened with <a href="/previous-versions/windows/desktop/fax/-mfax-fax-port-access-levels">PORT_OPEN_MODIFY</a> access.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_BAD_UNIT</b></dt>
</dl>
</td>
<td width="60%">
The <i>DeviceId</i> parameter is invalid.

</td>
</tr>
</table>

## -remarks

Call the <b>FaxOpenPort</b> function to obtain the handle to a fax port. Use the handle when you call the following functions:

<ul>
<li>
<a href="/previous-versions/windows/desktop/api/winfax/nf-winfax-faxsetporta">FaxSetPort</a> to change the configuration of the port</li>
<li>
<a href="/previous-versions/windows/desktop/api/winfax/nf-winfax-faxenumroutingmethodsa">FaxEnumRoutingMethods</a> to retrieve information about the fax routing methods associated with a device</li>
</ul>
The <a href="/previous-versions/windows/desktop/api/winfax/nf-winfax-faxenumportsa">FaxEnumPorts</a> function returns an array of <a href="/windows/desktop/api/winfax/ns-winfax-fax_port_infoa">FAX_PORT_INFO</a> structures. Each structure contains detailed information for one port, including a valid value to pass in the <i>DeviceId</i> parameter. An application should not save this device identifier in a persistent manner, because the identifier can change between function calls to the fax server.

For more information, see <a href="/previous-versions/windows/desktop/fax/-mfax-fax-ports">Fax Ports</a>, <a href="/previous-versions/windows/desktop/fax/-mfax-fax-device-management">Fax Device Management</a>, and <a href="/previous-versions/windows/desktop/fax/-mfax-managing-fax-routing-data">Managing Fax Routing Data</a>.

## -see-also

<a href="/windows/desktop/api/winfax/ns-winfax-fax_port_infoa">FAX_PORT_INFO</a>



<a href="/previous-versions/windows/desktop/fax/-mfax-fax-service-client-api-functions">Fax Service Client API Functions</a>



<a href="/previous-versions/windows/desktop/fax/-mfax-fax-service-client-api-for-windows-2000">Fax Service Client API for Windows 2000</a>



<a href="/previous-versions/windows/desktop/api/winfax/nf-winfax-faxconnectfaxservera">FaxConnectFaxServer</a>



<a href="/previous-versions/windows/desktop/api/winfax/nf-winfax-faxenumportsa">FaxEnumPorts</a>



<a href="/previous-versions/windows/desktop/api/winfax/nf-winfax-faxgetporta">FaxGetPort</a>



<a href="/previous-versions/windows/desktop/api/winfax/nc-winfax-pfaxinitializeeventqueue">FaxInitializeEventQueue</a>



<a href="/previous-versions/windows/desktop/api/winfax/nf-winfax-faxsetporta">FaxSetPort</a>