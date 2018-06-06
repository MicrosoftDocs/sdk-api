---
UID: NF:winfax.FaxSetPortA
title: FaxSetPortA function
author: windows-sdk-content
description: A fax client application calls the FaxSetPort function to change the configuration of the fax port of interest.
old-location: fax\_mfax_faxsetport.htm
old-project: Fax
ms.assetid: VS|fax|~\fax\faxlegacy_5sac.htm
ms.author: windowssdkdev
ms.date: 05/21/2018
ms.keywords: FaxSetPort, FaxSetPort function [Fax Service], FaxSetPortA, FaxSetPortW, _mfax_faxsetport, fax._mfax_faxsetport, winfax/FaxSetPort, winfax/FaxSetPortA, winfax/FaxSetPortW
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
req.unicode-ansi: FaxSetPortW (Unicode) and FaxSetPortA (ANSI)
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
 - FaxSetPort
 - FaxSetPortA
 - FaxSetPortW
product: Windows
targetos: Windows
req.lib: WinFax.lib
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
---

# FaxSetPortA function


## -description


A fax client application calls the <b>FaxSetPort</b> function to change the configuration of the fax port of interest. The configuration data can include, among other items, the capability of the port, its priority, rings before answer, and the transmitting and called station identifiers..


## -parameters




### -param FaxPortHandle [in]

Type: <b>HANDLE</b>

Specifies a fax port handle returned by a call to the <a href="https://msdn.microsoft.com/9010d651-3259-40b2-91bf-de0a841207c1">FaxOpenPort</a> function.


### -param PortInfo [in]

Type: <b>const <a href="https://msdn.microsoft.com/a1772290-7f78-49f2-a1e6-d312247995e4">FAX_PORT_INFO</a>*</b>

Pointer to a <a href="https://msdn.microsoft.com/a1772290-7f78-49f2-a1e6-d312247995e4">FAX_PORT_INFO</a> structure. The structure contains data to modify the configuration of the specified fax port.


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
Access is denied. <a href="https://msdn.microsoft.com/7d6ff208-33e4-42b2-ae21-76ec8ff58809">FAX_PORT_SET</a> access is required.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_DEVICE_IN_USE</b></dt>
</dl>
</td>
<td width="60%">
The port indicated by the <i>FaxPortHandle</i> parameter is busy.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_PARAMETER</b></dt>
</dl>
</td>
<td width="60%">
One or both of the <i>FaxPortHandle</i> or <i>PortInfo</i> parameters are <b>NULL</b>.

</td>
</tr>
</table>
 




## -remarks



The application must call the <a href="https://msdn.microsoft.com/9010d651-3259-40b2-91bf-de0a841207c1">FaxOpenPort</a> function and specify the <b>PORT_OPEN_MODIFY</b> access level before calling the <b>FaxSetPort</b> function.

Only the following members of the <a href="https://msdn.microsoft.com/a1772290-7f78-49f2-a1e6-d312247995e4">FAX_PORT_INFO</a> structure can be set using this function: Flags, Rings, Priority, Tsid, and Csid

A fax administration application typically calls the <b>FaxSetPort</b> function to administer the fax devices associated with the fax server. To query the devices, call the <a href="https://msdn.microsoft.com/1cf89b9c-525d-42df-b3fa-4dda6f560fd6">FaxGetPort</a> function.

To obtain a valid port handle to specify in the <i>FaxPortHandle</i> parameter of the <b>FaxSetPort</b> function, call the <a href="https://msdn.microsoft.com/9010d651-3259-40b2-91bf-de0a841207c1">FaxOpenPort</a> function. For more information, see <a href="https://msdn.microsoft.com/784fdc0e-c664-4ea9-8a4f-0a0cd89c0d81">Fax Device Management</a>.




## -see-also




<a href="https://msdn.microsoft.com/a1772290-7f78-49f2-a1e6-d312247995e4">FAX_PORT_INFO</a>



<a href="https://msdn.microsoft.com/b076b5ba-09af-4312-90c1-27abd0b859df">Fax Service Client API Functions</a>



<a href="https://msdn.microsoft.com/cbc79dc5-d0ca-418d-8572-64b0a582056f">Fax Service Client API for Windows 2000</a>



<a href="https://msdn.microsoft.com/7bd33e6f-09ff-449b-ac22-b79a14e5d928">FaxEnumPorts</a>



<a href="https://msdn.microsoft.com/1cf89b9c-525d-42df-b3fa-4dda6f560fd6">FaxGetPort</a>



<a href="https://msdn.microsoft.com/9010d651-3259-40b2-91bf-de0a841207c1">FaxOpenPort</a>
 

 

