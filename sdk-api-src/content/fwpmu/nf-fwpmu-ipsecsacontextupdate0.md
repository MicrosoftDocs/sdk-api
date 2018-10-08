---
UID: NF:fwpmu.IPsecSaContextUpdate0
title: IPsecSaContextUpdate0 function
author: windows-sdk-content
description: Updates an IPsec security association (SA) context.
old-location: fwp\ipsecsacontextupdate0.htm
tech.root: fwp
ms.assetid: ff19c7e6-569e-4bde-9a25-1661d50aea5e
ms.author: windowssdkdev
ms.date: 10/05/2018
ms.keywords: IPSEC_SA_BUNDLE_UPDATE_FLAGS, IPSEC_SA_BUNDLE_UPDATE_KEY_MODULE_STATE, IPSEC_SA_BUNDLE_UPDATE_MM_SA_ID, IPSEC_SA_BUNDLE_UPDATE_NAP_CONTEXT, IPSEC_SA_BUNDLE_UPDATE_PEER_V4_PRIVATE_ADDRESS, IPSEC_SA_DETAILS_UPDATE_TRAFFIC, IPSEC_SA_DETAILS_UPDATE_UDP_ENCAPSULATION, IPsecSaContextUpdate0, IPsecSaContextUpdate0 function [Filtering], fwp.ipsecsacontextupdate0, fwpmu/IPsecSaContextUpdate0
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
 - IPsecSaContextUpdate0
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IPsecSaContextUpdate0 function


## -description


The <b>IPsecSaContextUpdate0</b> function updates an IPsec security association (SA) context.


## -parameters




### -param engineHandle [in]

Type: <b>HANDLE</b>

Handle for an open session to the filter engine. Call <a href="https://msdn.microsoft.com/5165f219-f3e0-4e84-915b-75912aab02b7">FwpmEngineOpen0</a> to open a session to the filter engine.


### -param flags [in]

Type: <b>UINT32</b>

Flags indicating the specific field in the <a href="https://msdn.microsoft.com/a3e210a7-cd3a-42fc-b3a0-7df9ad6778af">IPSEC_SA_CONTEXT1</a> structure that is being updated.

Possible values:

<table>
<tr>
<th>IPsec SA flag</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="IPSEC_SA_DETAILS_UPDATE_TRAFFIC"></a><a id="ipsec_sa_details_update_traffic"></a><dl>
<dt><b>IPSEC_SA_DETAILS_UPDATE_TRAFFIC</b></dt>
</dl>
</td>
<td width="60%">
Updates the <b>traffic</b> member of the <a href="https://msdn.microsoft.com/257e7ac0-9cb4-45aa-b7e5-107bb3483ab9">IPSEC_SA_DETAILS1</a> structure.

</td>
</tr>
<tr>
<td width="40%"><a id="IPSEC_SA_DETAILS_UPDATE_UDP_ENCAPSULATION"></a><a id="ipsec_sa_details_update_udp_encapsulation"></a><dl>
<dt><b>IPSEC_SA_DETAILS_UPDATE_UDP_ENCAPSULATION</b></dt>
</dl>
</td>
<td width="60%">
Updates the <b>udpEncapsulation</b> member of the <a href="https://msdn.microsoft.com/257e7ac0-9cb4-45aa-b7e5-107bb3483ab9">IPSEC_SA_DETAILS1</a> structure.

</td>
</tr>
<tr>
<td width="40%"><a id="IPSEC_SA_BUNDLE_UPDATE_FLAGS"></a><a id="ipsec_sa_bundle_update_flags"></a><dl>
<dt><b>IPSEC_SA_BUNDLE_UPDATE_FLAGS</b></dt>
</dl>
</td>
<td width="60%">
Updates the <b>flags</b> member of the <a href="https://msdn.microsoft.com/491f43ca-07ce-460f-8c20-e5eb0f7bcac4">IPSEC_SA_BUNDLE1</a> structure.

</td>
</tr>
<tr>
<td width="40%"><a id="IPSEC_SA_BUNDLE_UPDATE_NAP_CONTEXT"></a><a id="ipsec_sa_bundle_update_nap_context"></a><dl>
<dt><b>IPSEC_SA_BUNDLE_UPDATE_NAP_CONTEXT</b></dt>
</dl>
</td>
<td width="60%">
Updates the <b>napContext</b> member of the <a href="https://msdn.microsoft.com/491f43ca-07ce-460f-8c20-e5eb0f7bcac4">IPSEC_SA_BUNDLE1</a> structure.

</td>
</tr>
<tr>
<td width="40%"><a id="IPSEC_SA_BUNDLE_UPDATE_KEY_MODULE_STATE"></a><a id="ipsec_sa_bundle_update_key_module_state"></a><dl>
<dt><b>IPSEC_SA_BUNDLE_UPDATE_KEY_MODULE_STATE</b></dt>
</dl>
</td>
<td width="60%">
Updates the <b>keyModuleState</b> member of the <a href="https://msdn.microsoft.com/491f43ca-07ce-460f-8c20-e5eb0f7bcac4">IPSEC_SA_BUNDLE1</a> structure.

</td>
</tr>
<tr>
<td width="40%"><a id="IPSEC_SA_BUNDLE_UPDATE_PEER_V4_PRIVATE_ADDRESS"></a><a id="ipsec_sa_bundle_update_peer_v4_private_address"></a><dl>
<dt><b>IPSEC_SA_BUNDLE_UPDATE_PEER_V4_PRIVATE_ADDRESS</b></dt>
</dl>
</td>
<td width="60%">
Updates the <b>peerV4PrivateAddress</b> member of the <a href="https://msdn.microsoft.com/491f43ca-07ce-460f-8c20-e5eb0f7bcac4">IPSEC_SA_BUNDLE1</a> structure.

</td>
</tr>
<tr>
<td width="40%"><a id="IPSEC_SA_BUNDLE_UPDATE_MM_SA_ID"></a><a id="ipsec_sa_bundle_update_mm_sa_id"></a><dl>
<dt><b>IPSEC_SA_BUNDLE_UPDATE_MM_SA_ID</b></dt>
</dl>
</td>
<td width="60%">
Updates the <b>mmSaId</b> member of the <a href="https://msdn.microsoft.com/491f43ca-07ce-460f-8c20-e5eb0f7bcac4">IPSEC_SA_BUNDLE1</a> structure.

</td>
</tr>
</table>
 


### -param newValues [in]

Type: <b>const <a href="https://msdn.microsoft.com/a3e210a7-cd3a-42fc-b3a0-7df9ad6778af">IPSEC_SA_CONTEXT1</a>*</b>

An inbound and outbound SA pair.


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
The IPsec SA context was updated successfully.

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



<b>IPsecSaContextUpdate0</b> is a specific implementation of IPsecSaContextUpdate. See <a href="https://msdn.microsoft.com/FBDF53E5-F7DE-4DEB-AC18-6D2BB59FE670">WFP Version-Independent Names and Targeting Specific Versions of Windows</a>  for more information.




## -see-also




<a href="https://msdn.microsoft.com/a3e210a7-cd3a-42fc-b3a0-7df9ad6778af">IPSEC_SA_CONTEXT1</a>
 

 

