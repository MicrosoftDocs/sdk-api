---
UID: NF:fwpmu.FwpmIPsecTunnelDeleteByKey0
title: FwpmIPsecTunnelDeleteByKey0 function
author: windows-sdk-content
description: Removes an Internet Protocol Security (IPsec) tunnel mode policy from the system.
old-location: fwp\fwpmipsectunneldeletebykey0.htm
tech.root: fwp
ms.assetid: cbef853e-0d6e-420b-84a9-640f56614fe7
ms.author: windowssdkdev
ms.date: 10/10/2018
ms.keywords: FwpmIPsecTunnelDeleteByKey0, FwpmIPsecTunnelDeleteByKey0 function [Filtering], fwp.fwpmipsectunneldeletebykey0, fwpmu/FwpmIPsecTunnelDeleteByKey0
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
 - FwpmIPsecTunnelDeleteByKey0
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# FwpmIPsecTunnelDeleteByKey0 function


## -description


The <b>FwpmIPsecTunnelDeleteByKey0</b> function removes an Internet Protocol Security (IPsec) tunnel mode policy from the system.


## -parameters




### -param engineHandle [in]

Type: <b>HANDLE</b>

A handle for an open session to the filter engine. Call <a href="https://msdn.microsoft.com/5165f219-f3e0-4e84-915b-75912aab02b7">FwpmEngineOpen0</a> to open a session to the filter engine.


### -param key [in]

Type: <b>const GUID*</b>

Unique identifier of the IPsec tunnel.  This GUID was specified in the <b>providerContextKey</b> member of the <i>tunnelPolicy</i> parameter of the <a href="https://msdn.microsoft.com/6de989e0-c5e1-4147-b5da-23448a4af2c9">FwpmIPsecTunnelAdd0</a> function. 


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
The IPsec tunnel mode policy was successfully deleted.

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



This function cannot be called from within a read-only transaction. It will fail
with <b>FWP_E_INCOMPATIBLE_TXN</b>. See <a href="https://msdn.microsoft.com/2625ef9a-0e62-4e21-ba93-047965d0d782">Object Management</a> for more information about transactions.

<b>FwpmIPsecTunnelDeleteByKey0</b> is a specific implementation of FwpmIPsecTunnelDeleteByKey. See <a href="https://msdn.microsoft.com/FBDF53E5-F7DE-4DEB-AC18-6D2BB59FE670">WFP Version-Independent Names and Targeting Specific Versions of Windows</a>  for more information.




## -see-also




<a href="https://msdn.microsoft.com/6de989e0-c5e1-4147-b5da-23448a4af2c9">FwpmIPsecTunnelAdd0</a>
 

 

