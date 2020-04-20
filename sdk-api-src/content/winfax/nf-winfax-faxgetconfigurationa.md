---
UID: NF:winfax.FaxGetConfigurationA
title: FaxGetConfigurationA function (winfax.h)
description: The FaxGetConfiguration function returns to a fax client application the global configuration settings for the fax server to which the client has connected.helpviewer_keywords: ["FaxGetConfiguration","FaxGetConfiguration function [Fax Service]","FaxGetConfigurationA","FaxGetConfigurationW","_mfax_faxgetconfiguration","fax._mfax_faxgetconfiguration","winfax/FaxGetConfiguration","winfax/FaxGetConfigurationA","winfax/FaxGetConfigurationW"]
old-location: fax\_mfax_faxgetconfiguration.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxlegacy_6nn2.htm
ms.date: 12/05/2018
ms.keywords: FaxGetConfiguration, FaxGetConfiguration function [Fax Service], FaxGetConfigurationA, FaxGetConfigurationW, _mfax_faxgetconfiguration, fax._mfax_faxgetconfiguration, winfax/FaxGetConfiguration, winfax/FaxGetConfigurationA, winfax/FaxGetConfigurationW
f1_keywords:
- winfax/FaxGetConfiguration
dev_langs:
- c++
req.header: winfax.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: FaxGetConfigurationW (Unicode) and FaxGetConfigurationA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: WinFax.lib
req.dll: 
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- LibDef
api_location:
- WinFax.lib
- WinFax.dll
api_name:
- FaxGetConfiguration
- FaxGetConfigurationA
- FaxGetConfigurationW
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# FaxGetConfigurationA function


## -description


The <b>FaxGetConfiguration</b> function returns to a fax client application the global configuration settings for the fax server to which the client has connected. The data includes, among other items, retransmission, branding, archive and cover page settings; discount rate periods; and the status of the fax server queue.


## -parameters




### -param FaxHandle [in]

Type: <b>HANDLE</b>

Specifies a fax server handle returned by a call to the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/winfax/nf-winfax-faxconnectfaxservera">FaxConnectFaxServer</a> function.


### -param FaxConfig [out]

Type: <b>PFAX_CONFIGURATION*</b>

Pointer to the address of a buffer to receive a <a href="https://docs.microsoft.com/windows/desktop/api/winfax/ns-winfax-fax_configurationa">FAX_CONFIGURATION</a> structure. The structure contains the current configuration settings for the fax server. For information about memory allocation, see the following Remarks section.


## -returns



Type: <b>BOOL</b>

If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call <a href="https://docs.microsoft.com/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>. GetLastError can return one of the following errors.

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
One or both of the <i>FaxConfig</i> or <i>FaxHandle</i> parameters are <b>NULL</b>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_ACCESS_DENIED</b></dt>
</dl>
</td>
<td width="60%">
Access is denied. <a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-specific-fax-access-rights">FAX_CONFIG_QUERY</a> access is required.

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



A fax administration application typically calls the <b>FaxGetConfiguration</b> function to display the global configuration settings for the fax server. To change the configuration settings, call the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/winfax/nf-winfax-faxsetconfigurationa">FaxSetConfiguration</a> function.

The <b>FaxGetConfiguration</b> function allocates the memory required for the <a href="https://docs.microsoft.com/windows/desktop/api/winfax/ns-winfax-fax_configurationa">FAX_CONFIGURATION</a> buffer pointed to by the <i>FaxConfig</i> parameter. An application must call the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/winfax/nc-winfax-pfaxfreebuffer">FaxFreeBuffer</a> function to deallocate the resources associated with this parameter.

For more information, see <a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-fax-server-configuration-management">Fax Server Configuration Management</a> and <a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-freeing-fax-resources">Freeing Fax Resources</a>.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/winfax/ns-winfax-fax_configurationa">FAX_CONFIGURATION</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-fax-service-client-api-functions">Fax Service Client API Functions</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-fax-service-client-api-for-windows-2000">Fax Service Client API for Windows 2000</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/winfax/nf-winfax-faxconnectfaxservera">FaxConnectFaxServer</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/winfax/nc-winfax-pfaxfreebuffer">FaxFreeBuffer</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/winfax/nf-winfax-faxsetconfigurationa">FaxSetConfiguration</a>
 

 

