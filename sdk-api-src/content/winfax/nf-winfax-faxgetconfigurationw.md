---
UID: NF:winfax.FaxGetConfigurationW
title: FaxGetConfigurationW function
author: windows-sdk-content
description: The FaxGetConfiguration function returns to a fax client application the global configuration settings for the fax server to which the client has connected.
old-location: fax\_mfax_faxgetconfiguration.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxlegacy_6nn2.htm
ms.author: windowssdkdev
ms.date: 11/05/2018
ms.keywords: FaxGetConfiguration, FaxGetConfiguration function [Fax Service], FaxGetConfigurationA, FaxGetConfigurationW, _mfax_faxgetconfiguration, fax._mfax_faxgetconfiguration, winfax/FaxGetConfiguration, winfax/FaxGetConfigurationA, winfax/FaxGetConfigurationW
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# FaxGetConfigurationW function


## -description


The <b>FaxGetConfiguration</b> function returns to a fax client application the global configuration settings for the fax server to which the client has connected. The data includes, among other items, retransmission, branding, archive and cover page settings; discount rate periods; and the status of the fax server queue.


## -parameters




### -param FaxHandle [in]

Type: <b>HANDLE</b>

Specifies a fax server handle returned by a call to the <a href="https://msdn.microsoft.com/en-us/library/ms691482(v=VS.85).aspx">FaxConnectFaxServer</a> function.


### -param FaxConfig [out]

Type: <b>PFAX_CONFIGURATION*</b>

Pointer to the address of a buffer to receive a <a href="https://msdn.microsoft.com/en-us/library/ms690874(v=VS.85).aspx">FAX_CONFIGURATION</a> structure. The structure contains the current configuration settings for the fax server. For information about memory allocation, see the following Remarks section.


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
Access is denied. <a href="https://msdn.microsoft.com/en-us/library/ms692302(v=VS.85).aspx">FAX_CONFIG_QUERY</a> access is required.

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



A fax administration application typically calls the <b>FaxGetConfiguration</b> function to display the global configuration settings for the fax server. To change the configuration settings, call the <a href="https://msdn.microsoft.com/en-us/library/ms692787(v=VS.85).aspx">FaxSetConfiguration</a> function.

The <b>FaxGetConfiguration</b> function allocates the memory required for the <a href="https://msdn.microsoft.com/en-us/library/ms690874(v=VS.85).aspx">FAX_CONFIGURATION</a> buffer pointed to by the <i>FaxConfig</i> parameter. An application must call the <a href="https://msdn.microsoft.com/en-us/library/ms692846(v=VS.85).aspx">FaxFreeBuffer</a> function to deallocate the resources associated with this parameter.

For more information, see <a href="https://msdn.microsoft.com/en-us/library/ms691849(v=VS.85).aspx">Fax Server Configuration Management</a> and <a href="https://msdn.microsoft.com/en-us/library/ms690878(v=VS.85).aspx">Freeing Fax Resources</a>.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/ms690874(v=VS.85).aspx">FAX_CONFIGURATION</a>



<a href="https://msdn.microsoft.com/en-us/library/ms691947(v=VS.85).aspx">Fax Service Client API Functions</a>



<a href="https://msdn.microsoft.com/en-us/library/ms692829(v=VS.85).aspx">Fax Service Client API for Windows 2000</a>



<a href="https://msdn.microsoft.com/en-us/library/ms691482(v=VS.85).aspx">FaxConnectFaxServer</a>



<a href="https://msdn.microsoft.com/en-us/library/ms692846(v=VS.85).aspx">FaxFreeBuffer</a>



<a href="https://msdn.microsoft.com/en-us/library/ms692787(v=VS.85).aspx">FaxSetConfiguration</a>
 

 

