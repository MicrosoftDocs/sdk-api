---
UID: NF:winfax.FaxSetRoutingInfoA
title: FaxSetRoutingInfoA function (winfax.h)
description: A fax management application calls the FaxSetRoutingInfo function to modify the routing information for a fax routing method that is associated with a specific fax device. (ANSI)
helpviewer_keywords: ["FaxSetRoutingInfoA", "winfax/FaxSetRoutingInfoA"]
old-location: fax\_mfax_faxsetroutinginfo.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxlegacy_66i7.htm
ms.date: 12/05/2018
ms.keywords: FaxSetRoutingInfo, FaxSetRoutingInfo function [Fax Service], FaxSetRoutingInfoA, FaxSetRoutingInfoW, _mfax_faxsetroutinginfo, fax._mfax_faxsetroutinginfo, winfax/FaxSetRoutingInfo, winfax/FaxSetRoutingInfoA, winfax/FaxSetRoutingInfoW
req.header: winfax.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: FaxSetRoutingInfoW (Unicode) and FaxSetRoutingInfoA (ANSI)
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
 - FaxSetRoutingInfoA
 - winfax/FaxSetRoutingInfoA
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
 - FaxSetRoutingInfo
 - FaxSetRoutingInfoA
 - FaxSetRoutingInfoW
---

# FaxSetRoutingInfoA function


## -description

A fax management application calls the <b>FaxSetRoutingInfo</b> function to modify the routing information for a fax routing method that is associated with a specific fax device.

## -parameters

### -param FaxPortHandle [in]

Type: <b>HANDLE</b>

Specifies a fax port handle returned by a call to the <a href="/previous-versions/windows/desktop/api/winfax/nc-winfax-pfaxopenport">FaxOpenPort</a> function.

### -param RoutingGuid [in]

Type: <b>LPCTSTR</b>

Pointer to a constant null-terminated character string that specifies the GUID that uniquely identifies the fax routing method of interest. 

                    

For information about fax routing methods, see <a href="/previous-versions/windows/desktop/fax/-mfax-about-the-fax-routing-extension-api">About the Fax Routing Extension API</a>. For information about the relationship between routing methods and GUIDs, see <a href="/previous-versions/windows/desktop/fax/-mfax-fax-routing-methods">Fax Routing Methods</a>.

### -param RoutingInfoBuffer [in]

Type: <b>const BYTE*</b>

Pointer to a buffer that contains the fax routing information. The routing data is typically provided by the fax service administration application, a MMC snap-in component.

### -param RoutingInfoBufferSize [in]

Type: <b>DWORD</b>

Pointer to a <b>DWORD</b> variable that contains the size of the buffer, in bytes, pointed to by the <i>RoutingInfoBuffer</i> parameter.

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
Access is denied. <a href="/previous-versions/windows/desktop/fax/-mfax-specific-fax-access-rights">FAX_PORT_SET</a> access is required.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_PARAMETER</b></dt>
</dl>
</td>
<td width="60%">
One or more of the parameters are <b>NULL</b>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_DATA</b></dt>
</dl>
</td>
<td width="60%">
The <i>RoutingGuid</i> parameter is invalid.

</td>
</tr>
</table>

## -remarks

The fax service administration application, an MMC snap-in component that manages the specified fax routing method, typically calls the <b>FaxSetRoutingInfo</b> function. This is because the format of the routing data is unavailable to the fax client application. The routing data is relevant only to the exported fax routing method and the method's administration application.

To obtain a valid port handle to specify in the <i>FaxPortHandle</i> parameter of the <b>FaxSetRoutingInfo</b> function, call the <a href="/previous-versions/windows/desktop/api/winfax/nc-winfax-pfaxopenport">FaxOpenPort</a> function.

The <a href="/previous-versions/windows/desktop/api/winfax/nf-winfax-faxenumglobalroutinginfoa">FaxEnumGlobalRoutingInfo</a> function retrieves routing information that applies globally to the fax server, such as routing priority. An application can modify global data with a call to the <a href="/previous-versions/windows/desktop/api/winfax/nf-winfax-faxsetglobalroutinginfoa">FaxSetGlobalRoutingInfo</a> function.

For more information, see <a href="/previous-versions/windows/desktop/fax/-mfax-managing-fax-routing-data">Managing Fax Routing Data</a>.





> [!NOTE]
> The winfax.h header defines FaxSetRoutingInfo as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/api/winfax/ns-winfax-fax_global_routing_infoa">FAX_GLOBAL_ROUTING_INFO</a>



<a href="/previous-versions/windows/desktop/fax/-mfax-fax-service-client-api-functions">Fax Service Client API Functions</a>



<a href="/previous-versions/windows/desktop/fax/-mfax-fax-service-client-api-for-windows-2000">Fax Service Client API for Windows 2000</a>



<a href="/previous-versions/windows/desktop/api/winfax/nf-winfax-faxenumglobalroutinginfoa">FaxEnumGlobalRoutingInfo</a>



<a href="/previous-versions/windows/desktop/api/winfax/nf-winfax-faxenumroutingmethodsa">FaxEnumRoutingMethods</a>



<a href="/previous-versions/windows/desktop/api/winfax/nf-winfax-faxgetroutinginfoa">FaxGetRoutingInfo</a>



<a href="/previous-versions/windows/desktop/api/winfax/nc-winfax-pfaxopenport">FaxOpenPort</a>



<a href="/previous-versions/windows/desktop/api/winfax/nf-winfax-faxsetglobalroutinginfoa">FaxSetGlobalRoutingInfo</a>
