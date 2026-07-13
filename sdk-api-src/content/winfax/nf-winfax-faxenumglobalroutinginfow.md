---
UID: NF:winfax.FaxEnumGlobalRoutingInfoW
title: FaxEnumGlobalRoutingInfoW function (winfax.h)
description: The FaxEnumGlobalRoutingInfo function enumerates all fax routing methods associated with a specific fax server. (Unicode)
helpviewer_keywords: ["FaxEnumGlobalRoutingInfo", "FaxEnumGlobalRoutingInfo function [Fax Service]", "FaxEnumGlobalRoutingInfoW", "_mfax_faxenumglobalroutinginfo", "fax._mfax_faxenumglobalroutinginfo", "winfax/FaxEnumGlobalRoutingInfo", "winfax/FaxEnumGlobalRoutingInfoW"]
old-location: fax\_mfax_faxenumglobalroutinginfo.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxlegacy_5zvz.htm
ms.date: 12/05/2018
ms.keywords: FaxEnumGlobalRoutingInfo, FaxEnumGlobalRoutingInfo function [Fax Service], FaxEnumGlobalRoutingInfoA, FaxEnumGlobalRoutingInfoW, _mfax_faxenumglobalroutinginfo, fax._mfax_faxenumglobalroutinginfo, winfax/FaxEnumGlobalRoutingInfo, winfax/FaxEnumGlobalRoutingInfoA, winfax/FaxEnumGlobalRoutingInfoW
req.header: winfax.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: FaxEnumGlobalRoutingInfoW (Unicode) and FaxEnumGlobalRoutingInfoA (ANSI)
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
 - FaxEnumGlobalRoutingInfoW
 - winfax/FaxEnumGlobalRoutingInfoW
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
 - FaxEnumGlobalRoutingInfo
 - FaxEnumGlobalRoutingInfoA
 - FaxEnumGlobalRoutingInfoW
---

# FaxEnumGlobalRoutingInfoW function


## -description

The <b>FaxEnumGlobalRoutingInfo</b> function enumerates all fax routing methods associated with a specific fax server. The function returns to the fax client application fax routing method information that applies globally to the server, such as routing priority.

## -parameters

### -param FaxHandle [in]

Type: <b>HANDLE</b>

Specifies a fax server handle returned by a call to the <a href="/previous-versions/windows/desktop/api/winfax/nf-winfax-faxconnectfaxservera">FaxConnectFaxServer</a> function.

### -param RoutingInfo [out]

Type: <b>PFAX_GLOBAL_ROUTING_INFO*</b>

Pointer to the address of a buffer to receive an array of <a href="/windows/desktop/api/winfax/ns-winfax-fax_global_routing_infoa">FAX_GLOBAL_ROUTING_INFO</a> structures. Each structure contains information about one fax routing method, as it pertains to the entire fax service. The data includes, among other items, the priority for the fax routing method, and the name of the DLL that exports the routing method. It also includes the GUID and function name that identify the routing method, and the method's user-friendly name. For information about memory allocation, see the following Remarks section.

### -param MethodsReturned [out]

Type: <b>LPDWORD</b>

Pointer to a DWORD variable to receive the number of <a href="/windows/desktop/api/winfax/ns-winfax-fax_global_routing_infoa">FAX_GLOBAL_ROUTING_INFO</a> structures the function returns in the <i>RoutingInfo</i> parameter. This number equals the total number of fax routing methods installed on the target server.

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
Access is denied. <a href="/previous-versions/windows/desktop/fax/-mfax-specific-fax-access-rights">FAX_CONFIG_QUERY</a> access is required.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_PARAMETER</b></dt>
</dl>
</td>
<td width="60%">
One or all of the <i>MethodsReturned</i>, <i>RoutingInfo</i> or <i>FaxHandle</i> parameters are <b>NULL</b>.

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

The <b>FaxEnumGlobalRoutingInfo</b> function retrieves fax routing method information, such as routing priority, that applies globally to the fax server. An application can modify global data by calling the <a href="/previous-versions/windows/desktop/api/winfax/nf-winfax-faxsetglobalroutinginfoa">FaxSetGlobalRoutingInfo</a> function.

An application can call the <a href="/previous-versions/windows/desktop/api/winfax/nf-winfax-faxenumroutingmethodsa">FaxEnumRoutingMethods</a> function to enumerate the fax routing methods associated with a particular device.

The <b>FaxEnumGlobalRoutingInfo</b> function allocates the memory required for the <a href="/windows/desktop/api/winfax/ns-winfax-fax_global_routing_infoa">FAX_GLOBAL_ROUTING_INFO</a> buffer array pointed to by the <i>RoutingInfo</i> parameter. An application must call the <a href="/previous-versions/windows/desktop/api/winfax/nc-winfax-pfaxfreebuffer">FaxFreeBuffer</a> function to deallocate the resources associated with this parameter. For more information, see <a href="/previous-versions/windows/desktop/fax/-mfax-freeing-fax-resources">Freeing Fax Resources</a> and <a href="/previous-versions/windows/desktop/fax/-mfax-managing-fax-routing-data">Managing Fax Routing Data</a>.





> [!NOTE]
> The winfax.h header defines FaxEnumGlobalRoutingInfo as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/api/winfax/ns-winfax-fax_global_routing_infoa">FAX_GLOBAL_ROUTING_INFO</a>



<a href="/previous-versions/windows/desktop/fax/-mfax-fax-service-client-api-functions">Fax Service Client API Functions</a>



<a href="/previous-versions/windows/desktop/fax/-mfax-fax-service-client-api-for-windows-2000">Fax Service Client API for Windows 2000</a>



<a href="/previous-versions/windows/desktop/api/winfax/nf-winfax-faxconnectfaxservera">FaxConnectFaxServer</a>



<a href="/previous-versions/windows/desktop/api/winfax/nf-winfax-faxenumroutingmethodsa">FaxEnumRoutingMethods</a>



<a href="/previous-versions/windows/desktop/api/winfax/nc-winfax-pfaxfreebuffer">FaxFreeBuffer</a>



<a href="/previous-versions/windows/desktop/api/winfax/nf-winfax-faxsetglobalroutinginfoa">FaxSetGlobalRoutingInfo</a>
