---
UID: NF:winfax.FaxGetPortW
title: FaxGetPortW function
author: windows-sdk-content
description: The FaxGetPort function returns information for a specified fax port to a fax client application.
old-location: fax\_mfax_faxgetport.htm
old-project: Fax
ms.assetid: VS|fax|~\fax\faxlegacy_3910.htm
ms.author: windowssdkdev
ms.date: 08/03/2018
ms.keywords: FaxGetPort, FaxGetPort function [Fax Service], FaxGetPortA, FaxGetPortW, _mfax_faxgetport, fax._mfax_faxgetport, winfax/FaxGetPort, winfax/FaxGetPortA, winfax/FaxGetPortW
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
req.unicode-ansi: FaxGetPortW (Unicode) and FaxGetPortA (ANSI)
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
 - FaxGetPort
 - FaxGetPortA
 - FaxGetPortW
product: Windows
targetos: Windows
req.lib: WinFax.lib
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
---

# FaxGetPortW function


## -description


The <b>FaxGetPort</b> function returns information for a specified fax port to a fax client application. The data includes, among other items, the permanent line identifier, the current status and capability of the port, and the transmitting and called station identifiers.
        


## -parameters




### -param FaxPortHandle [in]

Type: <b>HANDLE</b>

Specifies a fax port handle returned by a call to the <a href="https://msdn.microsoft.com/9010d651-3259-40b2-91bf-de0a841207c1">FaxOpenPort</a> function.


### -param PortInfo [out]

Type: <b>PFAX_PORT_INFO*</b>

Pointer to the address of a buffer to receive a <a href="https://msdn.microsoft.com/a1772290-7f78-49f2-a1e6-d312247995e4">FAX_PORT_INFO</a> structure. The structure describes one fax port. For information about memory allocation, see the following Remarks section.


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
One or both of the <i>PortInfo</i> or <i>FaxPortHandle</i> parameters are <b>NULL</b>.

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
<dt><b>ERROR_NOT_ENOUGH_MEMORY</b></dt>
</dl>
</td>
<td width="60%">
An error occurred during memory allocation.

</td>
</tr>
</table>
 




## -remarks



The application must call the <a href="https://msdn.microsoft.com/9010d651-3259-40b2-91bf-de0a841207c1">FaxOpenPort</a> function and specify the <b>PORT_OPEN_QUERY</b> access level before calling the <b>FaxGetPort</b> function.

A fax administration application typically calls the <b>FaxGetPort</b> function to query a device associated with the fax server.

To obtain a valid port handle to specify in the <i>FaxPortHandle</i> parameter, call the <a href="https://msdn.microsoft.com/9010d651-3259-40b2-91bf-de0a841207c1">FaxOpenPort</a> function.

The <b>FaxGetPort</b> function allocates the memory required for the <a href="https://msdn.microsoft.com/a1772290-7f78-49f2-a1e6-d312247995e4">FAX_PORT_INFO</a> buffer pointed to by the <i>PortInfo</i> parameter. An application must call the <a href="https://msdn.microsoft.com/9a7eedc8-e00f-40e8-a9f4-8e919012ed47">FaxFreeBuffer</a> function to deallocate the resources associated with this parameter.

For more information, see <a href="https://msdn.microsoft.com/784fdc0e-c664-4ea9-8a4f-0a0cd89c0d81">Fax Device Management</a> and <a href="https://msdn.microsoft.com/a8371d98-8a66-484a-9179-4894ae0a7dfc">Freeing Fax Resources</a>.




## -see-also




<a href="https://msdn.microsoft.com/a1772290-7f78-49f2-a1e6-d312247995e4">FAX_PORT_INFO</a>



<a href="https://msdn.microsoft.com/b076b5ba-09af-4312-90c1-27abd0b859df">Fax Service Client API Functions</a>



<a href="https://msdn.microsoft.com/cbc79dc5-d0ca-418d-8572-64b0a582056f">Fax Service Client API for Windows 2000</a>



<a href="https://msdn.microsoft.com/7bd33e6f-09ff-449b-ac22-b79a14e5d928">FaxEnumPorts</a>



<a href="https://msdn.microsoft.com/9a7eedc8-e00f-40e8-a9f4-8e919012ed47">FaxFreeBuffer</a>



<a href="https://msdn.microsoft.com/9010d651-3259-40b2-91bf-de0a841207c1">FaxOpenPort</a>



<a href="https://msdn.microsoft.com/32558e1f-c961-4fdc-806b-9544be4f95ee">FaxSetPort</a>
 

 

