---
UID: NF:fwpmu.IPsecSaContextGetById0
title: IPsecSaContextGetById0 function
author: windows-sdk-content
description: Retrieves an IPsec security association (SA) context.
old-location: fwp\ipsecsacontextgetbyid0.htm
tech.root: fwp
ms.assetid: a5bfd0e6-0113-4953-954c-d58e9cda91f0
ms.author: windowssdkdev
ms.date: 10/05/2018
ms.keywords: IPsecSaContextGetById0, IPsecSaContextGetById0 function [Filtering], fwp.ipsecsacontextgetbyid0, fwpmu/IPsecSaContextGetById0
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
 - IPsecSaContextGetById0
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IPsecSaContextGetById0 function


## -description


The <b>IPsecSaContextGetById0</b> function retrieves an IPsec security association (SA) context.
<div class="alert"><b>Note</b>  <b>IPsecSaContextGetById0</b> is the specific implementation of IPsecSaContextGetById used in Windows Vista. See <a href="https://msdn.microsoft.com/FBDF53E5-F7DE-4DEB-AC18-6D2BB59FE670">WFP Version-Independent Names and Targeting Specific Versions of Windows</a> for more information. For Windows 7 and later, <a href="https://msdn.microsoft.com/b3b3c513-3148-49ea-9a35-5c3ab6999961">IPsecSaContextGetById1</a> is available.</div><div> </div>

## -parameters




### -param engineHandle [in]

Type: <b>HANDLE</b>

Handle for an open session to the filter engine. Call <a href="https://msdn.microsoft.com/5165f219-f3e0-4e84-915b-75912aab02b7">FwpmEngineOpen0</a> to open a session to the filter engine.


### -param id [in]

Type: <b>UINT64</b>

A runtime identifier for the SA context. This identifier was received from the system when the application called <a href="https://msdn.microsoft.com/50b85c07-2e21-4c89-928b-8954348b9aba">IPsecSaContextCreate0</a>.


### -param saContext [out]

Type: <b><a href="https://msdn.microsoft.com/1cf191f0-5052-40f6-8665-747ae3f38fb1">IPSEC_SA_CONTEXT0</a>**</b>

Address of the IPsec SA context.


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
The IPsec SA context was successfully retrieved.

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



The caller must free the returned object, <i>saContext</i>,  by a call to <a href="https://msdn.microsoft.com/ba9f8c1e-f75c-4bf0-b68b-e21a358575fc">FwpmFreeMemory0</a>.

The caller needs <a href="https://msdn.microsoft.com/77f0a1ac-3e99-4cba-a7c6-b8747f35cd0c">FWPM_ACTRL_READ</a> access to the IPsec security associations database. See <a href="https://msdn.microsoft.com/936ad5f0-d5cd-47ed-b9e5-a7d82a4da603">Access Control</a> for more information.




## -see-also




<a href="https://msdn.microsoft.com/1cf191f0-5052-40f6-8665-747ae3f38fb1">IPSEC_SA_CONTEXT0</a>



<a href="https://msdn.microsoft.com/50b85c07-2e21-4c89-928b-8954348b9aba">IPsecSaContextCreate0</a>
 

 

