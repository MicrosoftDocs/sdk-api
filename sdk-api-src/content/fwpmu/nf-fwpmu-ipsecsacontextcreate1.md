---
UID: NF:fwpmu.IPsecSaContextCreate1
title: IPsecSaContextCreate1 function
author: windows-driver-content
description: Creates an IPsec security association (SA) context.
old-location: fwp\ipsecsacontextcreate1.htm
old-project: FWP
ms.assetid: b0eab185-fae2-4133-b3f2-22d609cb94d1
ms.author: windowsdriverdev
ms.date: 5/8/2018
ms.keywords: IPsecSaContextCreate1, IPsecSaContextCreate1 function [Filtering], fwp.ipsecsacontextcreate1, fwpmu/IPsecSaContextCreate1
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
req.typenames: FWPM_VSWITCH_EVENT_SUBSCRIPTION0
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	Fwpuclnt.dll
api_name:
-	IPsecSaContextCreate1
product: Windows
targetos: Windows
req.lib: Fwpuclnt.lib
req.dll: Fwpuclnt.dll
req.irql: 
req.product: Internet Explorer 5
---

# IPsecSaContextCreate1 function


## -description


The <b>IPsecSaContextCreate1</b> function creates an IPsec security association (SA) context.
<div class="alert"><b>Note</b>  <b>IPsecSaContextCreate1</b> is the specific implementation of IPsecSaContextCreate used in Windows 7 and later. See <a href="https://msdn.microsoft.com/FBDF53E5-F7DE-4DEB-AC18-6D2BB59FE670">WFP Version-Independent Names and Targeting Specific Versions of Windows</a> for more information. For Windows Vista, <a href="https://msdn.microsoft.com/50b85c07-2e21-4c89-928b-8954348b9aba">IPsecSaContextCreate0</a> is available.</div><div> </div>

## -parameters




### -param engineHandle [in]

Type: <b>HANDLE</b>

Handle for an open session to the filter engine. Call <a href="https://msdn.microsoft.com/library/windows/hardware/ff550075">FwpmEngineOpen0</a> to open a session to the filter engine.


### -param outboundTraffic [in]

Type: <b>const <a href="https://msdn.microsoft.com/5be2da29-73d6-4381-8bde-3a3945ea7b5a">IPSEC_TRAFFIC1</a>*</b>

The outbound traffic of the SA.


### -param virtualIfTunnelInfo [in, optional]

Type: <b>const <a href="https://msdn.microsoft.com/91af0790-865f-44f5-b6c8-fd048bf99125">IPSEC_VIRTUAL_IF_TUNNEL_INFO0</a>*</b>

Details related to virtual interface tunneling.


### -param inboundFilterId [out, optional]

Type: <b>UINT64*</b>

 Optional filter identifier of the cached inbound filter corresponding to the <i>outboundTraffic</i> parameter specified by the caller. Base filtering engine (BFE) may cache the inbound filter identifier and return the cached value, if available. Caller must handle the case when BFE does not have a cached value, in which case this parameter will be set to 0.


### -param id [out]

Type: <b>UINT64*</b>

The identifier of the  IPsec SA context.


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
The IPsec SA context was created successfully.

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

This function cannot be called from within a dynamic session. The call will fail with <b>FWP_E_DYNAMIC_SESSION_IN_PROGRESS</b>. See <a href="https://msdn.microsoft.com/2625ef9a-0e62-4e21-ba93-047965d0d782">Object Management</a> for more information about dynamic sessions.

The caller needs <a href="https://msdn.microsoft.com/77f0a1ac-3e99-4cba-a7c6-b8747f35cd0c">FWPM_ACTRL_ADD</a> access to the IPsec security associations database. See <a href="https://msdn.microsoft.com/936ad5f0-d5cd-47ed-b9e5-a7d82a4da603">Access Control</a> for more information.




## -see-also




<a href="https://msdn.microsoft.com/5be2da29-73d6-4381-8bde-3a3945ea7b5a">IPSEC_TRAFFIC1</a>



<a href="https://msdn.microsoft.com/91af0790-865f-44f5-b6c8-fd048bf99125">IPSEC_VIRTUAL_IF_TUNNEL_INFO0</a>
 

 

