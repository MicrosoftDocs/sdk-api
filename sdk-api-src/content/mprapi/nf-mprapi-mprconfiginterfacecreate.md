---
UID: NF:mprapi.MprConfigInterfaceCreate
title: MprConfigInterfaceCreate function
author: windows-sdk-content
description: The MprConfigInterfaceCreate function creates a router interface in the specified router configuration.
old-location: rras\mprconfiginterfacecreate.htm
tech.root: RRAS
ms.assetid: e368aa3c-bb80-49ed-a1da-39777dada960
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: MprConfigInterfaceCreate, MprConfigInterfaceCreate function [RAS], _mpr_mprconfiginterfacecreate, mprapi/MprConfigInterfaceCreate, rras.mprconfiginterfacecreate
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: mprapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
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
req.lib: Mprapi.lib
req.dll: Mprapi.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Mprapi.dll
api_name:
 - MprConfigInterfaceCreate
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- 
: 
- MprConfigInterfaceCreate
: 
---

# MprConfigInterfaceCreate function


## -description


The 
<b>MprConfigInterfaceCreate</b> function creates a router interface in the specified router configuration.


## -parameters




### -param hMprConfig [in]

Handle to the router configuration. Obtain this handle by calling 
<a href="https://msdn.microsoft.com/40029088-191d-49b1-88d3-79ffb2da0eef">MprConfigServerConnect</a>.


### -param dwLevel [in]

A DWORD value that describes the format in which the information is structured in the <i>lpbBuffer</i> parameter. Acceptable values for <i>dwLevel</i> include 0, 1, 2, and 3, as listed in the following table.

<table>
<tr>
<th>Value</th>
<th>Structure Format</th>
</tr>
<tr>
<td>0</td>
<td>
<a href="https://msdn.microsoft.com/b204c10e-ccce-4d62-a7a9-75cf4fe1d9ba">MPR_INTERFACE_0</a>
</td>
</tr>
<tr>
<td>1</td>
<td>
<a href="https://msdn.microsoft.com/90a3da46-7dd1-428b-ab72-d5defa710225">MPR_INTERFACE_1</a>
</td>
</tr>
<tr>
<td>2</td>
<td>
<a href="https://msdn.microsoft.com/486f3526-2b0e-4f08-bb85-3aebf10cd52e">MPR_INTERFACE_2</a>
</td>
</tr>
<tr>
<td>3</td>
<td>Windows Server 2008 or later: <a href="https://msdn.microsoft.com/d761a9cf-7b56-48ad-b98b-60fc99d0d8ba">MPR_INTERFACE_3</a>
</td>
</tr>
</table>
 


### -param lpbBuffer [in]

A pointer  to a 
<a href="https://msdn.microsoft.com/b204c10e-ccce-4d62-a7a9-75cf4fe1d9ba">MPR_INTERFACE_0</a>, 
<a href="https://msdn.microsoft.com/90a3da46-7dd1-428b-ab72-d5defa710225">MPR_INTERFACE_1</a>,  
<a href="https://msdn.microsoft.com/486f3526-2b0e-4f08-bb85-3aebf10cd52e">MPR_INTERFACE_2</a>, or  <a href="https://msdn.microsoft.com/d761a9cf-7b56-48ad-b98b-60fc99d0d8ba">MPR_INTERFACE_3</a> structure. The <i>dwLevel</i> parameter indicates the type of structure.
						
					


### -param phRouterInterface [out]

Pointer to a handle variable. This variable receives a handle to the interface configuration.


## -returns



If the function succeeds, the return value is NO_ERROR.

If the function fails, the return value is one of the following error codes.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_PARAMETER</b></dt>
</dl>
</td>
<td width="60%">
At least one of the following is true: 




<ul>
<li><i>hMprConfig</i> is <b>NULL</b></li>
<li><i>dwLevel</i> is not 0, 1, 2, or 3.</li>
<li><i>lpbBuffer</i> is <b>NULL</b></li>
<li><i>phRouterInterface</i> is <b>NULL</b></li>
</ul>
</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_NOT_ENOUGH_MEMORY</b></dt>
</dl>
</td>
<td width="60%">
Insufficient resources to complete the operation.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>Other</b></dt>
</dl>
</td>
<td width="60%">
Use 
<a href="https://msdn.microsoft.com/en-us/library/ms679351(v=VS.85).aspx">FormatMessage</a> to retrieve the system error message that corresponds to the error code returned.

</td>
</tr>
</table>
 




## -remarks



The 
<a href="https://msdn.microsoft.com/c9590ebe-7e49-4ad1-bd9b-0d9c51938bc4">MprAdminInterfaceCreate</a> function supports the 
<a href="https://msdn.microsoft.com/486f3526-2b0e-4f08-bb85-3aebf10cd52e">MPR_INTERFACE_2</a> structure. However, 
<b>MprConfigInterfaceCreate</b> does not. In order to create a demand-dial interface that is persistent after a reboot, call 
<b>MprAdminInterfaceCreate</b> with 
<b>MPR_INTERFACE_2</b>, then call 
<b>MprConfigInterfaceCreate</b> with 
<a href="https://msdn.microsoft.com/b204c10e-ccce-4d62-a7a9-75cf4fe1d9ba">MPR_INTERFACE_0</a> or 
<a href="https://msdn.microsoft.com/90a3da46-7dd1-428b-ab72-d5defa710225">MPR_INTERFACE_1</a>.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/ms679351(v=VS.85).aspx">FormatMessage</a>



<a href="https://msdn.microsoft.com/1777f742-8037-40d9-8279-b4bb89ea6f0d">MprConfigInterfaceDelete</a>



<a href="https://msdn.microsoft.com/40029088-191d-49b1-88d3-79ffb2da0eef">MprConfigServerConnect</a>



<a href="https://msdn.microsoft.com/fb65885c-7c3b-4c90-9516-388f09703c90">Router Configuration Functions</a>



<a href="https://msdn.microsoft.com/352505a9-616a-4d47-9857-f88d345333fd">Router Management Reference</a>
 

 

