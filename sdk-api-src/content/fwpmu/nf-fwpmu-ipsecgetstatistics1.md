---
UID: NF:fwpmu.IPsecGetStatistics1
title: IPsecGetStatistics1 function
author: windows-sdk-content
description: Retrieves Internet Protocol Security (IPsec) statistics.
old-location: fwp\ipsecgetstatistics1_func.htm
tech.root: fwp
ms.assetid: cb95167c-224f-4c78-a0a2-8268f766aa05
ms.author: windowssdkdev
ms.date: 10/12/2018
ms.keywords: IPsecGetStatistics1, IPsecGetStatistics1 function [Filtering], fwp.ipsecgetstatistics1_func, fwpmu/IPsecGetStatistics1
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: fwpmu.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
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
 - IPsecGetStatistics1
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IPsecGetStatistics1 function


## -description


The <b>IPsecGetStatistics1</b> function retrieves Internet Protocol Security (IPsec) statistics.
<div class="alert"><b>Note</b>  <b>IPsecGetStatistics1</b> is the specific implementation of IPsecGetStatistics used in Windows 7 and later. See <a href="https://msdn.microsoft.com/FBDF53E5-F7DE-4DEB-AC18-6D2BB59FE670">WFP Version-Independent Names and Targeting Specific Versions of Windows</a> for more information. For Windows Vista, <a href="https://msdn.microsoft.com/f33aad79-bc42-4f75-bc24-5d9838c02745">IPsecGetStatistics0</a> is available.</div><div> </div>

## -parameters




### -param engineHandle [in]

Type: <b>HANDLE</b>

Handle for an open session to the filter engine. Call <a href="https://msdn.microsoft.com/5165f219-f3e0-4e84-915b-75912aab02b7">FwpmEngineOpen0</a> to open a session to the filter engine.


### -param ipsecStatistics [out]

Type: <b><a href="https://msdn.microsoft.com/d61d8eb5-1b0b-419e-a248-58541db8906b">IPSEC_STATISTICS1</a>*</b>

Top-level object of IPsec statistics organization.


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
The IPsec statistics were successfully retrieved.

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



This function cannot be called from within a transaction. It will fail with
<b>FWP_E_TXN_IN_PROGRESS</b>. See <a href="https://msdn.microsoft.com/2625ef9a-0e62-4e21-ba93-047965d0d782">Object Management</a> for more information about transactions.

The caller needs <a href="https://msdn.microsoft.com/77f0a1ac-3e99-4cba-a7c6-b8747f35cd0c">FWPM_ACTRL_READ_STATS</a> access to the IPsec security associations database. See <a href="https://msdn.microsoft.com/936ad5f0-d5cd-47ed-b9e5-a7d82a4da603">Access Control</a> for more information.




## -see-also




<a href="https://msdn.microsoft.com/d61d8eb5-1b0b-419e-a248-58541db8906b">IPSEC_STATISTICS1</a>
 

 

