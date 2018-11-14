---
UID: NF:fwpmu.IPsecSaContextExpire0
title: IPsecSaContextExpire0 function
author: windows-sdk-content
description: Indicates that an IPsec security association (SA) context should be expired.
old-location: fwp\ipsecsacontextexpire0.htm
tech.root: fwp
ms.assetid: 7e249e61-ba40-4dd9-b675-c3c86e8dd1bf
ms.author: windowssdkdev
ms.date: 10/12/2018
ms.keywords: IPsecSaContextExpire0, IPsecSaContextExpire0 function [Filtering], fwp.ipsecsacontextexpire0, fwpmu/IPsecSaContextExpire0
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: fwpmu.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Fwpuclnt.lib
req.dll: Fwpuclnt.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Fwpuclnt.dll
api_name:
 - IPsecSaContextExpire0
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- 
: 
- IPsecSaContextExpire0
: 
---

# IPsecSaContextExpire0 function


## -description


The <b>IPsecSaContextExpire0</b> function indicates that an IPsec security association (SA) context should be expired.


## -parameters




### -param engineHandle [in]

Type: <b>HANDLE</b>

Handle for an open session to the filter engine. Call <a href="https://msdn.microsoft.com/5165f219-f3e0-4e84-915b-75912aab02b7">FwpmEngineOpen0</a> to open a session to the filter engine.


### -param id [in]

Type: <b>UINT64</b>

A runtime identifier for SA context. This identifier was received from the system when the application called <a href="https://msdn.microsoft.com/50b85c07-2e21-4c89-928b-8954348b9aba">IPsecSaContextCreate0</a>.


## -returns



Type: <b>DWORD</b>

<table>
<tr>
<th>Return code/value</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_SUCCESS</b></dt>
<dt>0</dt>
</dl>
</td>
<td width="60%">
The IPsec SA context was successfully expired.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>FWP_E_* error code</b></dt>
<dt>0x80320001—0x80320039</dt>
</dl>
</td>
<td width="60%">
A Windows Filtering Platform (WFP) specific error. See <a href="https://msdn.microsoft.com/11f3085a-f044-4a78-b47a-59b9086562bf">WFP Error Codes</a> for details.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>RPC_* error code</b></dt>
<dt>0x80010001—0x80010122</dt>
</dl>
</td>
<td width="60%">
Failure to communicate with the remote or local firewall engine.

</td>
</tr>
</table>
 




## -remarks



When an SA context is expired, the corresponding outbound SA gets deleted immediately, whereas the inbound SA deletion is postponed for a minute. This allows the processing of any inbound IPsec protected traffic that may still be on the wire.

The caller needs <a href="https://msdn.microsoft.com/f43bccce-0f8c-4732-b678-5fd3218a9f84">DELETE</a> access to the IPsec security associations database. See <a href="https://msdn.microsoft.com/936ad5f0-d5cd-47ed-b9e5-a7d82a4da603">Access Control</a> for more information.

<b>IPsecSaContextExpire0</b> is a specific implementation of IPsecSaContextExpire. See <a href="https://msdn.microsoft.com/FBDF53E5-F7DE-4DEB-AC18-6D2BB59FE670">WFP Version-Independent Names and Targeting Specific Versions of Windows</a>  for more information.




## -see-also




<a href="https://msdn.microsoft.com/50b85c07-2e21-4c89-928b-8954348b9aba">IPsecSaContextCreate0</a>
 

 

