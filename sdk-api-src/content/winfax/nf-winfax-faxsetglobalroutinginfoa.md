---
UID: NF:winfax.FaxSetGlobalRoutingInfoA
title: FaxSetGlobalRoutingInfoA function (winfax.h)
description: A fax management application calls the FaxSetGlobalRoutingInfo function to modify fax routing method data, such as routing priority, that applies globally to the fax server. (ANSI)
helpviewer_keywords: ["FaxSetGlobalRoutingInfoA", "winfax/FaxSetGlobalRoutingInfoA"]
old-location: fax\_mfax_faxsetglobalroutinginfo.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxlegacy_3jlb.htm
ms.date: 12/05/2018
ms.keywords: FaxSetGlobalRoutingInfo, FaxSetGlobalRoutingInfo function [Fax Service], FaxSetGlobalRoutingInfoA, FaxSetGlobalRoutingInfoW, _mfax_faxsetglobalroutinginfo, fax._mfax_faxsetglobalroutinginfo, winfax/FaxSetGlobalRoutingInfo, winfax/FaxSetGlobalRoutingInfoA, winfax/FaxSetGlobalRoutingInfoW
req.header: winfax.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: FaxSetGlobalRoutingInfoW (Unicode) and FaxSetGlobalRoutingInfoA (ANSI)
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
 - FaxSetGlobalRoutingInfoA
 - winfax/FaxSetGlobalRoutingInfoA
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
 - FaxSetGlobalRoutingInfo
 - FaxSetGlobalRoutingInfoA
 - FaxSetGlobalRoutingInfoW
---

# FaxSetGlobalRoutingInfoA function


## -description

A fax management application calls the <b>FaxSetGlobalRoutingInfo</b> function to modify fax routing method data, such as routing priority, that applies globally to the fax server.

## -parameters

### -param FaxHandle [in]

Type: <b>HANDLE</b>

Specifies a fax server handle returned by a call to the <a href="/previous-versions/windows/desktop/api/winfax/nf-winfax-faxconnectfaxservera">FaxConnectFaxServer</a> function.

### -param RoutingInfo [in]

Type: <b>const <a href="/windows/desktop/api/winfax/ns-winfax-fax_global_routing_infoa">FAX_GLOBAL_ROUTING_INFO</a>*</b>

Pointer to a buffer that contains a <a href="/windows/desktop/api/winfax/ns-winfax-fax_global_routing_infoa">FAX_GLOBAL_ROUTING_INFO</a> structure.

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
Access is denied. <a href="/previous-versions/windows/desktop/fax/-mfax-specific-fax-access-rights">FAX_CONFIG_SET</a> access is required.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_DATA</b></dt>
</dl>
</td>
<td width="60%">
The <b>Guid</b> member of the specified <a href="/windows/desktop/api/winfax/ns-winfax-fax_global_routing_infoa">FAX_GLOBAL_ROUTING_INFO</a> structure does not correspond to an installed fax routing method.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_PARAMETER</b></dt>
</dl>
</td>
<td width="60%">
One or both of the <i>FaxHandle</i> or <i>RoutingInfo</i> parameters are invalid.

</td>
</tr>
</table>

## -remarks

An application such as the fax service administration application, a Microsoft Management Console (MMC) snap-in component that manages the specified fax routing method, typically calls the <b>FaxSetGlobalRoutingInfo</b> function.

To retrieve the current global configuration, call the <a href="/previous-versions/windows/desktop/api/winfax/nf-winfax-faxenumglobalroutinginfoa">FaxEnumGlobalRoutingInfo</a> function. Call the <a href="/previous-versions/windows/desktop/api/winfax/nf-winfax-faxenumroutingmethodsa">FaxEnumRoutingMethods</a> function to enumerate the fax routing methods associated with a particular device. For more information, see <a href="/previous-versions/windows/desktop/fax/-mfax-managing-fax-routing-data">Managing Fax Routing Data</a>.





> [!NOTE]
> The winfax.h header defines FaxSetGlobalRoutingInfo as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/api/winfax/ns-winfax-fax_global_routing_infoa">FAX_GLOBAL_ROUTING_INFO</a>



<a href="/previous-versions/windows/desktop/fax/-mfax-fax-service-client-api-functions">Fax Service Client API Functions</a>



<a href="/previous-versions/windows/desktop/fax/-mfax-fax-service-client-api-for-windows-2000">Fax Service Client API for Windows 2000</a>



<a href="/previous-versions/windows/desktop/api/winfax/nf-winfax-faxenumglobalroutinginfoa">FaxEnumGlobalRoutingInfo</a>



<a href="/previous-versions/windows/desktop/api/winfax/nf-winfax-faxenumroutingmethodsa">FaxEnumRoutingMethods</a>
