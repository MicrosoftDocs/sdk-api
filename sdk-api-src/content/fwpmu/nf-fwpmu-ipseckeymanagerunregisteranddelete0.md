---
UID: NF:fwpmu.IPsecKeyManagerUnregisterAndDelete0
title: IPsecKeyManagerUnregisterAndDelete0 function
author: windows-sdk-content
description: Unregisters a Trusted Intermediary Agent (TIA) which had previously been registered with IPsec.
old-location: fwp\ipseckeymanagerunregisteranddelete0.htm
old-project: fwp
ms.assetid: 6A200451-3528-4728-A2D1-643385BA23E6
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: IPsecKeyManagerUnregisterAndDelete0, IPsecKeyManagerUnregisterAndDelete0 function [Filtering], fwp.ipseckeymanagerunregisteranddelete0, fwpmu/IPsecKeyManagerUnregisterAndDelete0
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: fwpmu.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: FWPM_VSWITCH_EVENT_SUBSCRIPTION0
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Fwpuclnt.dll
api_name:
 - IPsecKeyManagerUnregisterAndDelete0
product: Windows
targetos: Windows
req.lib: Fwpuclnt.lib
req.dll: Fwpuclnt.dll
req.irql: 
req.product: Internet Explorer 5
---

# IPsecKeyManagerUnregisterAndDelete0 function


## -description


The <b>IPsecKeyManagerUnregisterAndDelete0</b> function unregisters a Trusted Intermediary Agent (TIA) which had previously been registered with IPsec.


## -parameters




### -param engineHandle [in]

Type: <b>HANDLE</b>

A handle for an open session to the filter engine. Call <a href="https://msdn.microsoft.com/library/windows/hardware/ff550075">FwpmEngineOpen0</a> to open a session to the filter engine.


### -param keyMgmtHandle [in]

Type: <b>HANDLE</b>

Address of the previously created registration.


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
The TIA was successfully unregistered.

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
 




## -see-also




<a href="https://msdn.microsoft.com/26a69710-9981-40a4-8b1e-dca709624ead">WFP  Functions</a>
 

 

