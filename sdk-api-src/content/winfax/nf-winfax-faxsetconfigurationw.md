---
UID: NF:winfax.FaxSetConfigurationW
title: FaxSetConfigurationW function (winfax.h)
description: A fax client application calls the FaxSetConfiguration function to change the global configuration settings for the fax server to which the client has connected. (Unicode)
helpviewer_keywords: ["FaxSetConfiguration", "FaxSetConfiguration function [Fax Service]", "FaxSetConfigurationW", "_mfax_faxsetconfiguration", "fax._mfax_faxsetconfiguration", "winfax/FaxSetConfiguration", "winfax/FaxSetConfigurationW"]
old-location: fax\_mfax_faxsetconfiguration.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxlegacy_8iwe.htm
ms.date: 12/05/2018
ms.keywords: FaxSetConfiguration, FaxSetConfiguration function [Fax Service], FaxSetConfigurationA, FaxSetConfigurationW, _mfax_faxsetconfiguration, fax._mfax_faxsetconfiguration, winfax/FaxSetConfiguration, winfax/FaxSetConfigurationA, winfax/FaxSetConfigurationW
req.header: winfax.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: FaxSetConfigurationW (Unicode) and FaxSetConfigurationA (ANSI)
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
 - FaxSetConfigurationW
 - winfax/FaxSetConfigurationW
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
 - FaxSetConfiguration
 - FaxSetConfigurationA
 - FaxSetConfigurationW
---

# FaxSetConfigurationW function


## -description

A fax client application calls the <b>FaxSetConfiguration</b> function to change the global configuration settings for the fax server to which the client has connected. The configuration data can include, among other items, retransmission, branding, archive and cover page settings; discount rate periods; and the status of the fax server queue.

## -parameters

### -param FaxHandle [in]

Type: <b>HANDLE</b>

Specifies a fax server handle returned by a call to the <a href="/previous-versions/windows/desktop/api/winfax/nf-winfax-faxconnectfaxservera">FaxConnectFaxServer</a> function.

### -param FaxConfig [in]

Type: <b>const <a href="/windows/desktop/api/winfax/ns-winfax-fax_configurationa">FAX_CONFIGURATION</a>*</b>

Pointer to a <a href="/windows/desktop/api/winfax/ns-winfax-fax_configurationa">FAX_CONFIGURATION</a> structure. The structure contains data to modify the current fax server configuration settings.

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
The <i>FaxConfig</i> parameter is <b>NULL</b>, or the <b>SizeOfStruct</b> member of the specified <a href="/windows/desktop/api/winfax/ns-winfax-fax_configurationa">FAX_CONFIGURATION</a> structure is not equal to <b>sizeof(FAX_CONFIGURATION)</b>.

</td>
</tr>
</table>

## -remarks

A fax administration application typically calls the <b>FaxSetConfiguration</b> function to administer the global configuration settings for a fax server. To query the settings, an application can call the <a href="/previous-versions/windows/desktop/api/winfax/nf-winfax-faxgetconfigurationa">FaxGetConfiguration</a> function. For more information, see <a href="/previous-versions/windows/desktop/fax/-mfax-fax-server-configuration-management">Fax Server Configuration Management</a>.





> [!NOTE]
> The winfax.h header defines FaxSetConfiguration as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/api/winfax/ns-winfax-fax_configurationa">FAX_CONFIGURATION</a>



<a href="/previous-versions/windows/desktop/fax/-mfax-fax-service-client-api-functions">Fax Service Client API Functions</a>



<a href="/previous-versions/windows/desktop/fax/-mfax-fax-service-client-api-for-windows-2000">Fax Service Client API for Windows 2000</a>



<a href="/previous-versions/windows/desktop/api/winfax/nf-winfax-faxconnectfaxservera">FaxConnectFaxServer</a>



<a href="/previous-versions/windows/desktop/api/winfax/nf-winfax-faxgetconfigurationa">FaxGetConfiguration</a>
