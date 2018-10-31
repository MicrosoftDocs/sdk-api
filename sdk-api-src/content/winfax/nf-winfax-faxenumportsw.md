---
UID: NF:winfax.FaxEnumPortsW
title: FaxEnumPortsW function
author: windows-sdk-content
description: The FaxEnumPorts function enumerates all fax devices currently attached to the fax server to which the client has connected. The function returns detailed information for each fax port to the fax client application.
old-location: fax\_mfax_faxenumports.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxlegacy_0ir7.htm
ms.author: windowssdkdev
ms.date: 10/26/2018
ms.keywords: FaxEnumPorts, FaxEnumPorts function [Fax Service], FaxEnumPortsA, FaxEnumPortsW, _mfax_faxenumports, fax._mfax_faxenumports, winfax/FaxEnumPorts, winfax/FaxEnumPortsA, winfax/FaxEnumPortsW
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
req.unicode-ansi: FaxEnumPortsW (Unicode) and FaxEnumPortsA (ANSI)
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
 - FaxEnumPorts
 - FaxEnumPortsA
 - FaxEnumPortsW
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# FaxEnumPortsW function


## -description


The <b>FaxEnumPorts</b> function enumerates all fax devices currently attached to the fax server to which the client has connected. The function returns detailed information for each fax port to the fax client application.


## -parameters




### -param FaxHandle [in]

Type: <b>HANDLE</b>

Specifies a fax server handle returned by a call to the <a href="https://msdn.microsoft.com/en-us/library/ms691482(v=VS.85).aspx">FaxConnectFaxServer</a> function.


### -param PortInfo [out]

Type: <b>PFAX_PORT_INFO*</b>

Pointer to the address of a buffer to receive an array of <a href="https://msdn.microsoft.com/en-us/library/ms692359(v=VS.85).aspx">FAX_PORT_INFO</a> structures. Each structure describes one fax port. The data includes, among other items, the permanent line identifier, and the current status and capability of the port. For information about memory allocation, see the following Remarks section.


### -param PortsReturned [out]

Type: <b>LPDWORD</b>

Pointer to a <b>DWORD</b> variable to receive the number of <a href="https://msdn.microsoft.com/en-us/library/ms692359(v=VS.85).aspx">FAX_PORT_INFO</a> structures the function returns in the <i>PortInfo</i> parameter.


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
Access is denied. <a href="https://msdn.microsoft.com/en-us/library/ms692302(v=VS.85).aspx">FAX_JOB_QUERY</a> access is required.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_PARAMETER</b></dt>
</dl>
</td>
<td width="60%">
One or all of the <i>PortsReturned</i>, <i>PortInfo</i>, or <i>FaxHandle</i> parameters are <b>NULL</b>.

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



The <b>FaxEnumPorts</b> function returns a list of fax jobs on the fax server of interest, as well as information available about each job. A fax administration application typically calls this function to display the fax job queue for administrative or query purposes. For more information, see <a href="https://msdn.microsoft.com/en-us/library/ms691821(v=VS.85).aspx">Managing Fax Jobs</a>.

The <b>FaxEnumPorts</b> function allocates the memory required for the <a href="https://msdn.microsoft.com/en-us/library/ms690762(v=VS.85).aspx">FAX_JOB_ENTRY</a> buffer array pointed to by the <i>JobEntry</i> parameter. An application must call the <a href="https://msdn.microsoft.com/en-us/library/ms692846(v=VS.85).aspx">FaxFreeBuffer</a> function to deallocate the resources associated with this parameter. For more information, see <a href="https://msdn.microsoft.com/en-us/library/ms690878(v=VS.85).aspx">Freeing Fax Resources</a>.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/ms690762(v=VS.85).aspx">FAX_JOB_ENTRY</a>



<a href="https://msdn.microsoft.com/en-us/library/ms691947(v=VS.85).aspx">Fax Service Client API Functions</a>



<a href="https://msdn.microsoft.com/en-us/library/ms692829(v=VS.85).aspx">Fax Service Client API for Windows 2000</a>



<a href="https://msdn.microsoft.com/en-us/library/ms691482(v=VS.85).aspx">FaxConnectFaxServer</a>



<a href="https://msdn.microsoft.com/en-us/library/ms692846(v=VS.85).aspx">FaxFreeBuffer</a>



<a href="https://msdn.microsoft.com/en-us/library/ms692186(v=VS.85).aspx">FaxGetJob</a>
 

 

