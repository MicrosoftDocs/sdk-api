---
UID: NF:winfax.FaxSetConfigurationW
title: FaxSetConfigurationW function
author: windows-sdk-content
description: A fax client application calls the FaxSetConfiguration function to change the global configuration settings for the fax server to which the client has connected.
old-location: fax\_mfax_faxsetconfiguration.htm
old-project: Fax
ms.assetid: VS|fax|~\fax\faxlegacy_8iwe.htm
ms.author: windowssdkdev
ms.date: 08/03/2018
ms.keywords: FaxSetConfiguration, FaxSetConfiguration function [Fax Service], FaxSetConfigurationA, FaxSetConfigurationW, _mfax_faxsetconfiguration, fax._mfax_faxsetconfiguration, winfax/FaxSetConfiguration, winfax/FaxSetConfigurationA, winfax/FaxSetConfigurationW
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
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
tech.root: 
req.typenames: EVT_VARIANT, *PEVT_VARIANT
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
product: Windows
targetos: Windows
req.lib: WinFax.lib
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
---

# FaxSetConfigurationW function


## -description


A fax client application calls the <b>FaxSetConfiguration</b> function to change the global configuration settings for the fax server to which the client has connected. The configuration data can include, among other items, retransmission, branding, archive and cover page settings; discount rate periods; and the status of the fax server queue.


## -parameters




### -param FaxHandle [in]

Type: <b>HANDLE</b>

Specifies a fax server handle returned by a call to the <a href="https://msdn.microsoft.com/8705fb04-1047-4f83-ada9-898024ce719c">FaxConnectFaxServer</a> function.


### -param FaxConfig [in]

Type: <b>const <a href="https://msdn.microsoft.com/94b09265-a53c-47a2-8b24-bccb662b21c6">FAX_CONFIGURATION</a>*</b>

Pointer to a <a href="https://msdn.microsoft.com/94b09265-a53c-47a2-8b24-bccb662b21c6">FAX_CONFIGURATION</a> structure. The structure contains data to modify the current fax server configuration settings.


## -returns



Type: <b>BOOL</b>

If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>. GetLastError can return one of the following errors.

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
Access is denied. <a href="https://msdn.microsoft.com/7d6ff208-33e4-42b2-ae21-76ec8ff58809">FAX_CONFIG_SET</a> access is required.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_ACCESS_DENIED</b></dt>
</dl>
</td>
<td width="60%">
Access is denied. <a href="https://msdn.microsoft.com/7d6ff208-33e4-42b2-ae21-76ec8ff58809">FAX_PORT_QUERY</a> access is required.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_PARAMETER</b></dt>
</dl>
</td>
<td width="60%">
The <i>FaxConfig</i> parameter is <b>NULL</b>, or the <b>SizeOfStruct</b> member of the specified <a href="https://msdn.microsoft.com/94b09265-a53c-47a2-8b24-bccb662b21c6">FAX_CONFIGURATION</a> structure is not equal to <b>sizeof(FAX_CONFIGURATION)</b>.

</td>
</tr>
</table>
 




## -remarks



A fax administration application typically calls the <b>FaxSetConfiguration</b> function to administer the global configuration settings for a fax server. To query the settings, an application can call the <a href="https://msdn.microsoft.com/c29f0eaf-39a5-45e2-afb9-010494552969">FaxGetConfiguration</a> function. For more information, see <a href="https://msdn.microsoft.com/49416909-d475-4c76-ae2a-bd3c39611b32">Fax Server Configuration Management</a>.




## -see-also




<a href="https://msdn.microsoft.com/94b09265-a53c-47a2-8b24-bccb662b21c6">FAX_CONFIGURATION</a>



<a href="https://msdn.microsoft.com/b076b5ba-09af-4312-90c1-27abd0b859df">Fax Service Client API Functions</a>



<a href="https://msdn.microsoft.com/cbc79dc5-d0ca-418d-8572-64b0a582056f">Fax Service Client API for Windows 2000</a>



<a href="https://msdn.microsoft.com/8705fb04-1047-4f83-ada9-898024ce719c">FaxConnectFaxServer</a>



<a href="https://msdn.microsoft.com/c29f0eaf-39a5-45e2-afb9-010494552969">FaxGetConfiguration</a>
 

 

