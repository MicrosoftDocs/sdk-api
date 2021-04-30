---
UID: NF:winfax.FaxRegisterRoutingExtensionW
title: FaxRegisterRoutingExtensionW function (winfax.h)
description: The FaxRegisterRoutingExtension function registers a fax routing extension DLL with the fax service. The function configures the fax service registry to use the new routing extension DLL.
helpviewer_keywords: ["FaxRegisterRoutingExtension","FaxRegisterRoutingExtension function [Fax Service]","FaxRegisterRoutingExtensionW","_mfax_faxregisterroutingextension","fax._mfax_faxregisterroutingextension","winfax/FaxRegisterRoutingExtension"]
old-location: fax\_mfax_faxregisterroutingextension.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxlegacy_4q3y.htm
ms.date: 12/05/2018
ms.keywords: FaxRegisterRoutingExtension, FaxRegisterRoutingExtension function [Fax Service], FaxRegisterRoutingExtensionW, _mfax_faxregisterroutingextension, fax._mfax_faxregisterroutingextension, winfax/FaxRegisterRoutingExtension
req.header: winfax.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
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
 - FaxRegisterRoutingExtensionW
 - winfax/FaxRegisterRoutingExtensionW
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
 - FaxRegisterRoutingExtension
---

# FaxRegisterRoutingExtensionW function


## -description

The <b>FaxRegisterRoutingExtension</b> function registers a fax routing extension DLL with the fax service. The function configures the fax service registry to use the new routing extension DLL.

## -parameters

### -param FaxHandle [in]

Type: <b>HANDLE</b>

Specifies a fax server handle returned by a call to the <a href="/previous-versions/windows/desktop/api/winfax/nf-winfax-faxconnectfaxservera">FaxConnectFaxServer</a> function.

### -param ExtensionName [in]

Type: <b>LPCWSTR</b>

Specifies a fax server handle returned by a call to the <a href="/previous-versions/windows/desktop/api/winfax/nf-winfax-faxconnectfaxservera">FaxConnectFaxServer</a> function.

### -param FriendlyName [in]

Type: <b>LPCWSTR</b>

Pointer to a constant null-terminated Unicode character string to associate with the fax routing extension DLL. This is the routing extension's user-friendly name, suitable for display.

### -param ImageName [in]

Type: <b>LPCWSTR</b>

Pointer to a constant null-terminated Unicode character string that specifies the full path and file name for the fax routing extension DLL. The path can include valid environment variables, for example, %SYSTEMDRIVE% and %SYSTEMROOT%.

### -param CallBack [in]

Type: <b>PFAX_ROUTING_INSTALLATION_CALLBACK</b>

Pointer to a <a href="/windows/desktop/api/winfax/nc-winfax-pfax_routing_installation_callbackw">FaxRoutingInstallationCallback</a> function that installs a fax routing method for the specified fax routing extension DLL. The <b>FaxRegisterRoutingExtension</b> function calls the <b>FaxRoutingInstallationCallback</b> function multiple times, until it returns a value of zero, indicating that all routing methods in the fax routing extension DLL have been registered.

### -param Context [in]

Type: <b>LPVOID</b>

Pointer to a variable that contains application-specific context information or an application-defined value. <b>FaxRegisterRoutingExtension</b> passes this data to the <a href="/windows/desktop/api/winfax/nc-winfax-pfax_routing_installation_callbackw">FaxRoutingInstallationCallback</a> function.

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
At least one parameter to the <a href="/windows/desktop/api/winfax/nf-winfax-faxregisterroutingextensionw">FaxRegisterRoutingExtension</a> function is <b>NULL</b>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_FUNCTION</b></dt>
</dl>
</td>
<td width="60%">
The <i>FaxHandle</i> specifies a remote fax server connection.

</td>
</tr>
</table>

## -remarks

<b>FaxRegisterRoutingExtension</b> calls the <a href="/windows/desktop/api/winfax/nc-winfax-pfax_routing_installation_callbackw">FaxRoutingInstallationCallback</a> function once for each fax routing method in the fax routing extension DLL.

Because the <b>FaxRegisterRoutingExtension</b> function modifies the registry, the user, generally a system administrator, must have write access to the <b>HKEY_LOCAL_MACHINE</b> registry key.

<div class="alert"><b>Note</b>  <b>FaxRegisterRoutingExtension</b> has only Unicode and local versions.</div>
<div> </div>
All parameters to the <b>FaxRegisterRoutingExtension</b> function are required.

You must restart the fax service to use a fax routing method exported by a fax routing extension you install using <b>FaxRegisterRoutingExtension</b>.

For more information about the steps required to register with the fax service, see <a href="/previous-versions/windows/desktop/fax/-mfax-registration-of-a-fax-routing-extension">Registration of a Fax Routing Extension</a>.

## -see-also

<a href="/previous-versions/windows/desktop/fax/-mfax-fax-service-client-api-functions">Fax Service Client API Functions</a>



<a href="/previous-versions/windows/desktop/fax/-mfax-fax-service-client-api-for-windows-2000">Fax Service Client API for Windows 2000</a>



<a href="/previous-versions/windows/desktop/api/winfax/nf-winfax-faxconnectfaxservera">FaxConnectFaxServer</a>



<a href="/windows/desktop/api/winfax/nc-winfax-pfax_routing_installation_callbackw">FaxRoutingInstallationCallback</a>