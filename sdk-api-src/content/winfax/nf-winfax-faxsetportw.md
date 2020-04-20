---
UID: NF:winfax.FaxSetPortW
title: FaxSetPortW function (winfax.h)
description: A fax client application calls the FaxSetPort function to change the configuration of the fax port of interest.helpviewer_keywords: ["FaxSetPort","FaxSetPort function [Fax Service]","FaxSetPortA","FaxSetPortW","_mfax_faxsetport","fax._mfax_faxsetport","winfax/FaxSetPort","winfax/FaxSetPortA","winfax/FaxSetPortW"]
old-location: fax\_mfax_faxsetport.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxlegacy_5sac.htm
ms.date: 12/05/2018
ms.keywords: FaxSetPort, FaxSetPort function [Fax Service], FaxSetPortA, FaxSetPortW, _mfax_faxsetport, fax._mfax_faxsetport, winfax/FaxSetPort, winfax/FaxSetPortA, winfax/FaxSetPortW
f1_keywords:
- winfax/FaxSetPort
dev_langs:
- c++
req.header: winfax.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: FaxSetPortW (Unicode) and FaxSetPortA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: WinFax.lib
req.dll: 
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- LibDef
api_location:
- WinFax.lib
- WinFax.dll
api_name:
- FaxSetPort
- FaxSetPortA
- FaxSetPortW
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# FaxSetPortW function


## -description


A fax client application calls the <b>FaxSetPort</b> function to change the configuration of the fax port of interest. The configuration data can include, among other items, the capability of the port, its priority, rings before answer, and the transmitting and called station identifiers..


## -parameters




### -param FaxPortHandle [in]

Type: <b>HANDLE</b>

Specifies a fax port handle returned by a call to the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/winfax/nc-winfax-pfaxopenport">FaxOpenPort</a> function.


### -param PortInfo [in]

Type: <b>const <a href="https://docs.microsoft.com/windows/desktop/api/winfax/ns-winfax-fax_port_infoa">FAX_PORT_INFO</a>*</b>

Pointer to a <a href="https://docs.microsoft.com/windows/desktop/api/winfax/ns-winfax-fax_port_infoa">FAX_PORT_INFO</a> structure. The structure contains data to modify the configuration of the specified fax port.


## -returns



Type: <b>BOOL</b>

If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call <a href="https://docs.microsoft.com/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>. GetLastError can return one of the following errors.

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
Access is denied. <a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-specific-fax-access-rights">FAX_PORT_SET</a> access is required.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_DEVICE_IN_USE</b></dt>
</dl>
</td>
<td width="60%">
The port indicated by the <i>FaxPortHandle</i> parameter is busy.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_PARAMETER</b></dt>
</dl>
</td>
<td width="60%">
One or both of the <i>FaxPortHandle</i> or <i>PortInfo</i> parameters are <b>NULL</b>.

</td>
</tr>
</table>
 




## -remarks



The application must call the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/winfax/nc-winfax-pfaxopenport">FaxOpenPort</a> function and specify the <b>PORT_OPEN_MODIFY</b> access level before calling the <b>FaxSetPort</b> function.

Only the following members of the <a href="https://docs.microsoft.com/windows/desktop/api/winfax/ns-winfax-fax_port_infoa">FAX_PORT_INFO</a> structure can be set using this function: Flags, Rings, Priority, Tsid, and Csid

A fax administration application typically calls the <b>FaxSetPort</b> function to administer the fax devices associated with the fax server. To query the devices, call the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/winfax/nf-winfax-faxgetporta">FaxGetPort</a> function.

To obtain a valid port handle to specify in the <i>FaxPortHandle</i> parameter of the <b>FaxSetPort</b> function, call the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/winfax/nc-winfax-pfaxopenport">FaxOpenPort</a> function. For more information, see <a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-fax-device-management">Fax Device Management</a>.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/winfax/ns-winfax-fax_port_infoa">FAX_PORT_INFO</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-fax-service-client-api-functions">Fax Service Client API Functions</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-fax-service-client-api-for-windows-2000">Fax Service Client API for Windows 2000</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/winfax/nf-winfax-faxenumportsa">FaxEnumPorts</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/winfax/nf-winfax-faxgetporta">FaxGetPort</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/winfax/nc-winfax-pfaxopenport">FaxOpenPort</a>
 

 

