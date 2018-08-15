---
UID: NC:fwpmu.IPSEC_KEY_MANAGER_DICTATE_KEY0
title: IPSEC_KEY_MANAGER_DICTATE_KEY0
author: windows-sdk-content
description: Used by the Trusted Intermediary Agent (TIA) to dictate keys for the SA being negotiated.
old-location: fwp\ipsec_key_manager_dictate_key0.htm
old-project: fwp
ms.assetid: A69E44FF-A58D-426B-BD59-8EB4B5A63B66
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: IPSEC_KEY_MANAGER_DICTATE_KEY0, IPSEC_KEY_MANAGER_DICTATE_KEY0 function, IPSEC_KEY_MANAGER_DICTATE_KEY0 function pointer [Filtering], fwp.ipsec_key_dictate_key0, fwp.ipsec_key_manager_dictate_key0, fwpmu/IPSEC_KEY_MANAGER_DICTATE_KEY0
ms.prod: windows
ms.technology: windows-sdk
ms.topic: callback
req.header: fwpmu.h
req.include-header: 
req.redist: 
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
 - UserDefined
api_location:
 - Fwpmu.h
api_name:
 - IPSEC_KEY_MANAGER_DICTATE_KEY0
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Internet Explorer 5
---

# IPSEC_KEY_MANAGER_DICTATE_KEY0 callback function


## -description


The <b>IPSEC_KEY_MANAGER_DICTATE_KEY0</b> function is used by the Trusted Intermediary Agent (TIA) to dictate keys for the SA being negotiated.


## -parameters




### -param *inboundSaDetails


### -param *outboundSaDetails


### -param *keyingModuleGenKey








#### - generateRandomKey [out]

Type: <b>BOOL*</b>

True if the keying module should randomly generate keys in the event that the TIA is unable to supply keys; otherwise, false.


#### - inboundSa [in, out]

Type: <b><a href="https://msdn.microsoft.com/257e7ac0-9cb4-45aa-b7e5-107bb3483ab9">IPSEC_SA_DETAILS1</a>*</b>

Information about the inbound SA.


#### - outboundSa [in, out]

Type: <b><a href="https://msdn.microsoft.com/257e7ac0-9cb4-45aa-b7e5-107bb3483ab9">IPSEC_SA_DETAILS1</a>*</b>

Information about the outbound SA.


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
The keys were successfully dictated

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



Call <a href="https://msdn.microsoft.com/9606A611-6C55-4548-B9C4-688580338F08">IPsecKeyManagerAddAndRegister0</a> to invoke this function pointer. If the weight specified in <a href="https://msdn.microsoft.com/0B91B57C-6943-4702-8926-8ED2B7B3E48D">IPSEC_KEY_MANAGER_KEY_DICTATION_CHECK0</a> for a TIA is higher than that of any peer, <b>IPSEC_KEY_MANAGER_DICTATE_KEY0</b> will be invoked.




## -see-also




<a href="https://msdn.microsoft.com/0B91B57C-6943-4702-8926-8ED2B7B3E48D">IPSEC_KEY_MANAGER_KEY_DICTATION_CHECK0</a>



<a href="https://msdn.microsoft.com/257e7ac0-9cb4-45aa-b7e5-107bb3483ab9">IPSEC_SA_DETAILS1</a>



<a href="https://msdn.microsoft.com/9606A611-6C55-4548-B9C4-688580338F08">IPsecKeyManagerAddAndRegister0</a>



<a href="https://msdn.microsoft.com/26a69710-9981-40a4-8b1e-dca709624ead">WFP  Functions</a>
 

 

