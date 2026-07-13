---
UID: NF:winfax.FaxEnumRoutingMethodsA
title: FaxEnumRoutingMethodsA function (winfax.h)
description: The FaxEnumRoutingMethods function enumerates all fax routing methods for a specific fax device. The function returns information about each routing method to a fax client application. (ANSI)
helpviewer_keywords: ["FaxEnumRoutingMethodsA", "winfax/FaxEnumRoutingMethodsA"]
old-location: fax\_mfax_faxenumroutingmethods.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxlegacy_41gz.htm
ms.date: 12/05/2018
ms.keywords: FaxEnumRoutingMethods, FaxEnumRoutingMethods function [Fax Service], FaxEnumRoutingMethodsA, FaxEnumRoutingMethodsW, _mfax_faxenumroutingmethods, fax._mfax_faxenumroutingmethods, winfax/FaxEnumRoutingMethods, winfax/FaxEnumRoutingMethodsA, winfax/FaxEnumRoutingMethodsW
req.header: winfax.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: FaxEnumRoutingMethodsW (Unicode) and FaxEnumRoutingMethodsA (ANSI)
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
 - FaxEnumRoutingMethodsA
 - winfax/FaxEnumRoutingMethodsA
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
 - FaxEnumRoutingMethods
 - FaxEnumRoutingMethodsA
 - FaxEnumRoutingMethodsW
---

# FaxEnumRoutingMethodsA function


## -description

The <b>FaxEnumRoutingMethods</b> function enumerates all fax routing methods for a specific fax device. The function returns information about each routing method to a fax client application.

## -parameters

### -param FaxPortHandle [in]

Type: <b>HANDLE</b>

Specifies a fax port handle returned by a call to the <a href="/previous-versions/windows/desktop/api/winfax/nc-winfax-pfaxopenport">FaxOpenPort</a> function.

### -param RoutingMethod [out]

Type: <b>PFAX_ROUTING_METHOD*</b>

Pointer to the address of a buffer to receive an array of <a href="/windows/desktop/api/winfax/ns-winfax-fax_routing_methoda">FAX_ROUTING_METHOD</a> structures. Each structure contains information about one fax routing method. The data includes, among other items, the name of the DLL that exports the routing method, the GUID and function name that identify the routing method, and the method's user-friendly name. 

                    

For information about memory allocation, see the following Remarks section. For information about fax routing methods, see <a href="/previous-versions/windows/desktop/fax/-mfax-about-the-fax-routing-extension-api">About the Fax Routing Extension API</a>.

### -param MethodsReturned [out]

Type: <b>LPDWORD</b>

Pointer to a <b>DWORD</b> variable to receive the number of <a href="/windows/desktop/api/winfax/ns-winfax-fax_routing_methoda">FAX_ROUTING_METHOD</a> structures the <b>FaxEnumRoutingMethods</b> function returns in the <i>RoutingMethod</i> parameter.

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
<dt><b>ERROR_INVALID_PARAMETER</b></dt>
</dl>
</td>
<td width="60%">
One or all of the <i>MethodsReturned</i>, <i>RoutingMethod</i>, or <i>FaxPortHandle</i> parameters are <b>NULL</b>.

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

A fax administration application typically calls the <b>FaxEnumRoutingMethods</b> function to query the fax routing methods associated with a particular device. A call to the <a href="/previous-versions/windows/desktop/api/winfax/nf-winfax-faxsetroutinginfoa">FaxSetRoutingInfo</a> function changes the routing information for a particular fax routing method.

The <a href="/previous-versions/windows/desktop/api/winfax/nf-winfax-faxenumglobalroutinginfoa">FaxEnumGlobalRoutingInfo</a> function retrieves routing information that applies globally to the fax server, such as routing priority. An application can modify global data with a call to the <a href="/previous-versions/windows/desktop/api/winfax/nf-winfax-faxsetglobalroutinginfoa">FaxSetGlobalRoutingInfo</a> function.

The <b>FaxEnumRoutingMethods</b> function allocates the memory required for the <a href="/windows/desktop/api/winfax/ns-winfax-fax_routing_methoda">FAX_ROUTING_METHOD</a> buffer array pointed to by the <i>RoutingMethod</i> parameter. An application must call the <a href="/previous-versions/windows/desktop/api/winfax/nc-winfax-pfaxfreebuffer">FaxFreeBuffer</a> function to deallocate the resources associated with this parameter.

For more information, see <a href="/previous-versions/windows/desktop/fax/-mfax-fax-server-configuration-management">Fax Server Configuration Management</a> and <a href="/previous-versions/windows/desktop/fax/-mfax-freeing-fax-resources">Freeing Fax Resources</a>.





> [!NOTE]
> The winfax.h header defines FaxEnumRoutingMethods as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/api/winfax/ns-winfax-fax_global_routing_infoa">FAX_GLOBAL_ROUTING_INFO</a>



<a href="/windows/desktop/api/winfax/ns-winfax-fax_routing_methoda">FAX_ROUTING_METHOD</a>



<a href="/previous-versions/windows/desktop/fax/-mfax-fax-service-client-api-functions">Fax Service Client API Functions</a>



<a href="/previous-versions/windows/desktop/fax/-mfax-fax-service-client-api-for-windows-2000">Fax Service Client API for Windows 2000</a>



<a href="/previous-versions/windows/desktop/api/winfax/nf-winfax-faxenableroutingmethoda">FaxEnableRoutingMethod</a>



<a href="/previous-versions/windows/desktop/api/winfax/nf-winfax-faxenumglobalroutinginfoa">FaxEnumGlobalRoutingInfo</a>



<a href="/previous-versions/windows/desktop/api/winfax/nc-winfax-pfaxfreebuffer">FaxFreeBuffer</a>



<a href="/previous-versions/windows/desktop/api/winfax/nf-winfax-faxgetroutinginfoa">FaxGetRoutingInfo</a>



<a href="/previous-versions/windows/desktop/api/winfax/nc-winfax-pfaxopenport">FaxOpenPort</a>



<a href="/previous-versions/windows/desktop/api/winfax/nf-winfax-faxsetglobalroutinginfoa">FaxSetGlobalRoutingInfo</a>



<b>FaxSetRoutingInfo</b>
