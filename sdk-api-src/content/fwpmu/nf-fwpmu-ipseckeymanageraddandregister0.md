---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# IPsecKeyManagerAddAndRegister0 function


## -description


The <b>IPsecKeyManagerAddAndRegister0</b> function registers a Trusted Intermediary Agent (TIA) with IPsec.


## -parameters




### -param engineHandle [in]

Type: <b>HANDLE</b>

A handle for an open session to the filter engine. Call <a href="https://msdn.microsoft.com/library/windows/hardware/ff550075">FwpmEngineOpen0</a> to open a session to the filter engine.


### -param keyManager [in]

Type: <b>const <a href="https://msdn.microsoft.com/942F38AF-13F4-4A2E-A504-5085EC90E74C">IPSEC_KEY_MANAGER0</a>*</b>

The set of key management callbacks which IPsec will invoke.


### -param keyManagerCallbacks [in]

Type: <b>const <a href="https://msdn.microsoft.com/736ea54d-ca17-4cb5-bcb2-95b4377f321c">IPSEC_KEY_MANAGER_CALLBACKS0</a>*</b>

The set of callbacks which should be invoked by IPsec at various stages of SA negotiation.


### -param keyMgmtHandle [out]

Type: <b>HANDLE*</b>

Address of the newly created registration.


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
The TIA was successfully registered.

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
<tr>
<td width="40%">
<dl>
<dt><b>FWP_E_ALREADY_EXISTS</b></dt>
<dt>0x80320009L</dt>
</dl>
</td>
<td width="60%">
The TIA was not registered successfully because another TIA has already been registered to dictate keys.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>FWP_E_INVALID_INTERVAL</b></dt>
<dt>0x80320021L</dt>
</dl>
</td>
<td width="60%">
The TIA was not registered successfully because <i>keyDictationTimeoutHint</i> exceeded the maximum allowed value of 10 seconds.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>SEC_E_CANNOT_INSTALL</b></dt>
<dt>0x80090307L</dt>
</dl>
</td>
<td width="60%">
The TIA was not registered successfully because the binary image has not set the <b>IMAGE_DLLCHARACTERISTICS_FORCE_INTEGRITY</b> property.

</td>
</tr>
</table>
 




## -remarks



If the <b>IPSEC_KEY_MANAGER_FLAG_DICTATE_KEY</b> flag is set for <b>keyManager</b>, all three callback members of <b>keyManagerCallbacks</b> must be specified; otherwise, only the <b>keyNotify</b> callback should be specified

This function cannot be called from within a transaction. It will fail
with <b>FWP_E_TXN_IN_PROGRESS</b>. See <a href="https://msdn.microsoft.com/2625ef9a-0e62-4e21-ba93-047965d0d782">Object Management</a> for more information about transactions.




## -see-also




<a href="https://msdn.microsoft.com/942F38AF-13F4-4A2E-A504-5085EC90E74C">IPSEC_KEY_MANAGER0</a>



<a href="https://msdn.microsoft.com/736ea54d-ca17-4cb5-bcb2-95b4377f321c">IPSEC_KEY_MANAGER_CALLBACKS0</a>



<a href="https://msdn.microsoft.com/26a69710-9981-40a4-8b1e-dca709624ead">WFP  Functions</a>
 

 

