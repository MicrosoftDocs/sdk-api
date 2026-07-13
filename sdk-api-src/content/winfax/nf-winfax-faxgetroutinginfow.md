---
UID: NF:winfax.FaxGetRoutingInfoW
title: FaxGetRoutingInfoW function (winfax.h)
description: The FaxGetRoutingInfo function returns to a fax client application routing information for a fax routing method that is associated with a specific fax device. (Unicode)
helpviewer_keywords: ["FaxGetRoutingInfo", "FaxGetRoutingInfo function [Fax Service]", "FaxGetRoutingInfoW", "_mfax_faxgetroutinginfo", "fax._mfax_faxgetroutinginfo", "winfax/FaxGetRoutingInfo", "winfax/FaxGetRoutingInfoW"]
old-location: fax\_mfax_faxgetroutinginfo.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxlegacy_1pwv.htm
ms.date: 12/05/2018
ms.keywords: FaxGetRoutingInfo, FaxGetRoutingInfo function [Fax Service], FaxGetRoutingInfoA, FaxGetRoutingInfoW, _mfax_faxgetroutinginfo, fax._mfax_faxgetroutinginfo, winfax/FaxGetRoutingInfo, winfax/FaxGetRoutingInfoA, winfax/FaxGetRoutingInfoW
req.header: winfax.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: FaxGetRoutingInfoW (Unicode) and FaxGetRoutingInfoA (ANSI)
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
 - FaxGetRoutingInfoW
 - winfax/FaxGetRoutingInfoW
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
 - FaxGetRoutingInfo
 - FaxGetRoutingInfoA
 - FaxGetRoutingInfoW
---

# FaxGetRoutingInfoW function


## -description

The <b>FaxGetRoutingInfo</b> function returns to a fax client application routing information for a fax routing method that is associated with a specific fax device.

## -parameters

### -param FaxPortHandle [in]

Type: <b>HANDLE</b>

Specifies a fax port handle returned by a call to the <a href="/previous-versions/windows/desktop/api/winfax/nc-winfax-pfaxopenport">FaxOpenPort</a> function.

### -param RoutingGuid [in]

Type: <b>LPCTSTR</b>

Pointer to a constant null-terminated character string that specifies the GUID that uniquely identifies the fax routing method of interest.
                    
                    

For information about fax routing methods, see <a href="/previous-versions/windows/desktop/fax/-mfax-about-the-fax-routing-extension-api">About the Fax Routing Extension API</a>. For information about the relationship between routing methods and GUIDs, see <a href="/previous-versions/windows/desktop/fax/-mfax-fax-routing-methods">Fax Routing Methods</a>.

### -param RoutingInfoBuffer [out]

Type: <b>LPBYTE*</b>

Pointer to the address of a buffer to receive the fax routing information.

### -param RoutingInfoBufferSize [out]

Type: <b>LPDWORD</b>

Pointer to a <b>DWORD</b> variable to receive the size of the buffer, in bytes, pointed to by the <i>RoutingInfoBuffer</i> parameter.

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
One or all of the <i>RoutingGuid</i>, <i>RoutingInfoBuffer</i>, <i>RoutingInfoBufferSize</i>, or <i>FaxPortHandle</i> parameters are <b>NULL</b>.

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
<dt><b>ERROR_INVALID_DATA</b></dt>
</dl>
</td>
<td width="60%">
The <i>RoutingGuid</i> parameter is invalid.

</td>
</tr>
</table>

## -remarks

The fax service administration application, a Microsoft Management Console (MMC) snap-in component that manages the specified fax routing method, typically calls the <b>FaxGetRoutingInfo</b> function. This is because the format of the routing data is unavailable to a fax client application. The routing data is relevant only to the exported fax routing method and to the fax service administration application.

An application that manages a specific fax routing method can call the <b>FaxGetRoutingInfo</b> function to modify the routing information for the method on a specified fax device. To enumerate all fax routing methods associated with a device, call the <a href="/previous-versions/windows/desktop/api/winfax/nf-winfax-faxenumroutingmethodsa">FaxEnumRoutingMethods</a> function.

The <a href="/previous-versions/windows/desktop/api/winfax/nf-winfax-faxenumglobalroutinginfoa">FaxEnumGlobalRoutingInfo</a> function retrieves routing information that applies globally to the fax server, such as routing priority. An application can modify global data with a call to the <a href="/previous-versions/windows/desktop/api/winfax/nf-winfax-faxsetglobalroutinginfoa">FaxSetGlobalRoutingInfo</a> function.

The <b>FaxGetRoutingInfo</b> function allocates the memory required for the buffer pointed to by the <i>RoutingInfoBuffer</i> parameter. An application must call the <a href="/previous-versions/windows/desktop/api/winfax/nc-winfax-pfaxfreebuffer">FaxFreeBuffer</a> function to deallocate the resources associated with this parameter.

For more information, see <a href="/previous-versions/windows/desktop/fax/-mfax-managing-fax-routing-data">Managing Fax Routing Data</a> and <a href="/previous-versions/windows/desktop/fax/-mfax-freeing-fax-resources">Freeing Fax Resources</a>.





> [!NOTE]
> The winfax.h header defines FaxGetRoutingInfo as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/api/winfax/ns-winfax-fax_global_routing_infoa">FAX_GLOBAL_ROUTING_INFO</a>



<a href="/previous-versions/windows/desktop/fax/-mfax-fax-service-client-api-functions">Fax Service Client API Functions</a>



<a href="/previous-versions/windows/desktop/fax/-mfax-fax-service-client-api-for-windows-2000">Fax Service Client API for Windows 2000</a>



<a href="/previous-versions/windows/desktop/api/winfax/nf-winfax-faxenumglobalroutinginfoa">FaxEnumGlobalRoutingInfo</a>



<a href="/previous-versions/windows/desktop/api/winfax/nf-winfax-faxenumroutingmethodsa">FaxEnumRoutingMethods</a>



<a href="/previous-versions/windows/desktop/api/winfax/nc-winfax-pfaxfreebuffer">FaxFreeBuffer</a>



<a href="/previous-versions/windows/desktop/api/winfax/nc-winfax-pfaxopenport">FaxOpenPort</a>



<a href="/previous-versions/windows/desktop/api/winfax/nf-winfax-faxsetglobalroutinginfoa">FaxSetGlobalRoutingInfo</a>



<a href="/previous-versions/windows/desktop/api/winfax/nf-winfax-faxsetroutinginfoa">FaxSetRoutingInfo</a>
