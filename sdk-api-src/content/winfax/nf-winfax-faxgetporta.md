---
UID: NF:winfax.FaxGetPortA
title: FaxGetPortA function (winfax.h)
description: The FaxGetPort function returns information for a specified fax port to a fax client application. (ANSI)
helpviewer_keywords: ["FaxGetPortA", "winfax/FaxGetPortA"]
old-location: fax\_mfax_faxgetport.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxlegacy_3910.htm
ms.date: 12/05/2018
ms.keywords: FaxGetPort, FaxGetPort function [Fax Service], FaxGetPortA, FaxGetPortW, _mfax_faxgetport, fax._mfax_faxgetport, winfax/FaxGetPort, winfax/FaxGetPortA, winfax/FaxGetPortW
req.header: winfax.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: FaxGetPortW (Unicode) and FaxGetPortA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: WinFax.lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - FaxGetPortA
 - winfax/FaxGetPortA
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - LibDef
api_location:
 - WinFax.lib
 - WinFax.dll
api_name:
 - FaxGetPort
 - FaxGetPortA
 - FaxGetPortW
---

# FaxGetPortA function


## -description

The <b>FaxGetPort</b> function returns information for a specified fax port to a fax client application. The data includes, among other items, the permanent line identifier, the current status and capability of the port, and the transmitting and called station identifiers.

## -parameters

### -param FaxPortHandle [in]

Type: <b>HANDLE</b>

Specifies a fax port handle returned by a call to the <a href="/previous-versions/windows/desktop/api/winfax/nc-winfax-pfaxopenport">FaxOpenPort</a> function.

### -param PortInfo [out]

Type: <b>PFAX_PORT_INFO*</b>

Pointer to the address of a buffer to receive a <a href="/windows/desktop/api/winfax/ns-winfax-fax_port_infoa">FAX_PORT_INFO</a> structure. The structure describes one fax port. For information about memory allocation, see the following Remarks section.

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
<dt><b>ERROR_INVALID_PARAMETER</b></dt>
</dl>
</td>
<td width="60%">
One or both of the <i>PortInfo</i> or <i>FaxPortHandle</i> parameters are <b>NULL</b>.

</td>
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
</table>

## -remarks

The application must call the <a href="/previous-versions/windows/desktop/api/winfax/nc-winfax-pfaxopenport">FaxOpenPort</a> function and specify the <b>PORT_OPEN_QUERY</b> access level before calling the <b>FaxGetPort</b> function.

A fax administration application typically calls the <b>FaxGetPort</b> function to query a device associated with the fax server.

To obtain a valid port handle to specify in the <i>FaxPortHandle</i> parameter, call the <a href="/previous-versions/windows/desktop/api/winfax/nc-winfax-pfaxopenport">FaxOpenPort</a> function.

The <b>FaxGetPort</b> function allocates the memory required for the <a href="/windows/desktop/api/winfax/ns-winfax-fax_port_infoa">FAX_PORT_INFO</a> buffer pointed to by the <i>PortInfo</i> parameter. An application must call the <a href="/previous-versions/windows/desktop/api/winfax/nc-winfax-pfaxfreebuffer">FaxFreeBuffer</a> function to deallocate the resources associated with this parameter.

For more information, see <a href="/previous-versions/windows/desktop/fax/-mfax-fax-device-management">Fax Device Management</a> and <a href="/previous-versions/windows/desktop/fax/-mfax-freeing-fax-resources">Freeing Fax Resources</a>.





> [!NOTE]
> The winfax.h header defines FaxGetPort as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/api/winfax/ns-winfax-fax_port_infoa">FAX_PORT_INFO</a>



<a href="/previous-versions/windows/desktop/fax/-mfax-fax-service-client-api-functions">Fax Service Client API Functions</a>



<a href="/previous-versions/windows/desktop/fax/-mfax-fax-service-client-api-for-windows-2000">Fax Service Client API for Windows 2000</a>



<a href="/previous-versions/windows/desktop/api/winfax/nf-winfax-faxenumportsa">FaxEnumPorts</a>



<a href="/previous-versions/windows/desktop/api/winfax/nc-winfax-pfaxfreebuffer">FaxFreeBuffer</a>



<a href="/previous-versions/windows/desktop/api/winfax/nc-winfax-pfaxopenport">FaxOpenPort</a>



<a href="/previous-versions/windows/desktop/api/winfax/nf-winfax-faxsetporta">FaxSetPort</a>
