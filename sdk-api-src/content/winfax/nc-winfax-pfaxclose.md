---
UID: NC:winfax.PFAXCLOSE
title: PFAXCLOSE (winfax.h)
description: The FaxClose function closes fax handles
helpviewer_keywords: ["FaxCloseA","FaxCloseW","PFAXCLOSE","PFAXCLOSE callback","PFAXCLOSE callback function [Fax Service]","_mfax_faxclose","fax._mfax_faxclose","winfax/FaxCloseA","winfax/FaxCloseW","winfax/PFAXCLOSE"]
old-location: fax\_mfax_faxclose.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxlegacy_5h2d.htm
ms.date: 12/05/2018
ms.keywords: FaxCloseA, FaxCloseW, PFAXCLOSE, PFAXCLOSE callback, PFAXCLOSE callback function [Fax Service], _mfax_faxclose, fax._mfax_faxclose, winfax/FaxCloseA, winfax/FaxCloseW, winfax/PFAXCLOSE
req.header: winfax.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: FaxCloseW (Unicode) and FaxCloseA (ANSI)
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
 - PFAXCLOSE
 - winfax/PFAXCLOSE
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
 - PFAXCLOSE
 - FaxCloseA
 - FaxCloseW
---

# PFAXCLOSE callback function


## -description

The <b>FaxClose</b> function closes the following types of fax handles:


<ul>
<li>A fax server handle returned by a call to the <a href="/previous-versions/windows/desktop/api/winfax/nf-winfax-faxconnectfaxservera">FaxConnectFaxServer</a> function</li>
<li>A fax port handle returned by a call to the <a href="/previous-versions/windows/desktop/api/winfax/nc-winfax-pfaxopenport">FaxOpenPort</a> function</li>
</ul>

## -parameters

### -param FaxHandle [in]

Type: <b>HANDLE</b>

Specifies the fax handle to close. This value can be a fax server handle returned by a call to the <a href="/previous-versions/windows/desktop/api/winfax/nf-winfax-faxconnectfaxservera">FaxConnectFaxServer</a> function, or a fax port handle returned by a call to the <a href="/previous-versions/windows/desktop/api/winfax/nc-winfax-pfaxopenport">FaxOpenPort</a> function.

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
<dt><b>ERROR_INVALID_HANDLE</b></dt>
</dl>
</td>
<td width="60%">
The <i>FaxHandle</i> parameter is invalid.

</td>
</tr>
</table>

## -remarks

A fax client application must call the <b>FaxClose</b> function as the last function before it terminates. The <a href="/windows/desktop/api/handleapi/nf-handleapi-closehandle">CloseHandle</a> function cannot close the handle to a fax server or a fax port.

When the <b>FaxClose</b> function closes a handle allocated by the <a href="/previous-versions/windows/desktop/api/winfax/nf-winfax-faxconnectfaxservera">FaxConnectFaxServer</a> function, the function disconnects the calling application from the specified fax server.

A fax client application continues to receive fax events from the fax service after the application successfully calls the <b>FaxClose</b> function to close a fax server handle. This permits the fax service to shut down and conserve system resources when the service has been idle for an extended period. If you keep the handle to the fax server open, the fax service does not shut down.

For more information, see <a href="/previous-versions/windows/desktop/fax/-mfax-enabling-an-application-to-receive-notifications-of-fax-events">Enabling an Application to Receive Notifications of Fax Events</a>, <a href="/previous-versions/windows/desktop/fax/-mfax-connecting-to-a-fax-server">Connecting to a Fax Server</a> and <a href="/previous-versions/windows/desktop/fax/-mfax-disconnecting-from-a-fax-server">Disconnecting from a Fax Server</a>, and <a href="/previous-versions/windows/desktop/api/winfax/nc-winfax-pfaxinitializeeventqueue">FaxInitializeEventQueue</a>.

## -see-also

<a href="/previous-versions/windows/desktop/fax/-mfax-fax-service-client-api-functions">Fax Service Client API Functions</a>



<a href="/previous-versions/windows/desktop/fax/-mfax-fax-service-client-api-for-windows-2000">Fax Service Client API for Windows 2000</a>



<a href="/previous-versions/windows/desktop/api/winfax/nf-winfax-faxconnectfaxservera">FaxConnectFaxServer</a>



<a href="/previous-versions/windows/desktop/api/winfax/nc-winfax-pfaxopenport">FaxOpenPort</a>