---
UID: NF:winfax.FaxEnableRoutingMethodW
title: FaxEnableRoutingMethodW function (winfax.h)
description: The FaxEnableRoutingMethod function enables or disables a fax routing method for a specific fax device. A fax administration application typically calls this function for device management. (Unicode)
helpviewer_keywords: ["FaxEnableRoutingMethod", "FaxEnableRoutingMethod function [Fax Service]", "FaxEnableRoutingMethodW", "_mfax_faxenableroutingmethod", "fax._mfax_faxenableroutingmethod", "winfax/FaxEnableRoutingMethod", "winfax/FaxEnableRoutingMethodW"]
old-location: fax\_mfax_faxenableroutingmethod.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxlegacy_9ov8.htm
ms.date: 12/05/2018
ms.keywords: FaxEnableRoutingMethod, FaxEnableRoutingMethod function [Fax Service], FaxEnableRoutingMethodA, FaxEnableRoutingMethodW, _mfax_faxenableroutingmethod, fax._mfax_faxenableroutingmethod, winfax/FaxEnableRoutingMethod, winfax/FaxEnableRoutingMethodA, winfax/FaxEnableRoutingMethodW
req.header: winfax.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: FaxEnableRoutingMethodW (Unicode) and FaxEnableRoutingMethodA (ANSI)
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
 - FaxEnableRoutingMethodW
 - winfax/FaxEnableRoutingMethodW
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
 - FaxEnableRoutingMethod
 - FaxEnableRoutingMethodA
 - FaxEnableRoutingMethodW
---

# FaxEnableRoutingMethodW function


## -description

The <b>FaxEnableRoutingMethod</b> function enables or disables a fax routing method for a specific fax device. A fax administration application typically calls this function for device management.

## -parameters

### -param FaxPortHandle [in]

Type: <b>HANDLE</b>

Specifies a fax port handle returned by a call to the <a href="/previous-versions/windows/desktop/api/winfax/nc-winfax-pfaxopenport">FaxOpenPort</a> function.

### -param RoutingGuid [in]

Type: <b>LPCTSTR</b>

Pointer to a constant null-terminated character string that specifies the GUID that uniquely identifies the fax routing method of interest. 

                    

For information about fax routing methods, see <a href="/previous-versions/windows/desktop/fax/-mfax-about-the-fax-routing-extension-api">About the Fax Routing Extension API</a>. For information about the relationship between routing methods and GUIDs, see <a href="/previous-versions/windows/desktop/fax/-mfax-fax-routing-methods">Fax Routing Methods</a>.

### -param Enabled [in]

Type: <b>BOOL</b>

Specifies a Boolean variable that indicates whether the application is enabling or disabling the fax routing method specified by the <i>RoutingGuid</i> parameter. If this parameter is <b>TRUE</b>, the application is enabling the routing method; if this parameter is <b>FALSE</b>, the application is disabling the routing method.

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
One or both of the <i>FaxPortHandle</i> or <i>RoutingGuid</i> parameters are <b>NULL</b>.

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
</table>

## -remarks

A fax client application can call the <b>FaxEnableRoutingMethod</b> function to enable a fax routing method for a particular fax device. It can also call the function to disable a routing method enabled by a prior call to <b>FaxEnableRoutingMethod</b> or by the fax service administration application. For more information, see <a href="/previous-versions/windows/desktop/fax/-mfax-managing-fax-routing-data">Managing Fax Routing Data</a>.

Call the <a href="/previous-versions/windows/desktop/api/winfax/nc-winfax-pfaxopenport">FaxOpenPort</a> function to obtain a valid port handle to specify in the <i>FaxPortHandle</i> parameter.





> [!NOTE]
> The winfax.h header defines FaxEnableRoutingMethod as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/previous-versions/windows/desktop/fax/-mfax-fax-service-client-api-functions">Fax Service Client API Functions</a>



<a href="/previous-versions/windows/desktop/fax/-mfax-fax-service-client-api-for-windows-2000">Fax Service Client API for Windows 2000</a>



<a href="/previous-versions/windows/desktop/api/winfax/nf-winfax-faxenumroutingmethodsa">FaxEnumRoutingMethods</a>



<a href="/previous-versions/windows/desktop/api/winfax/nc-winfax-pfaxopenport">FaxOpenPort</a>



<a href="/windows/desktop/api/faxroute/nc-faxroute-pfaxroutemethod">FaxRouteMethod</a>
