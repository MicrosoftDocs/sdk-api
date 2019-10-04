---
UID: NC:fwpmu.IPSEC_KEY_MANAGER_DICTATE_KEY0
title: IPSEC_KEY_MANAGER_DICTATE_KEY0 (fwpmu.h)
author: windows-sdk-content
description: Used by the Trusted Intermediary Agent (TIA) to dictate keys for the SA being negotiated.
old-location: fwp\ipsec_key_manager_dictate_key0.htm
tech.root: fwp
ms.assetid: A69E44FF-A58D-426B-BD59-8EB4B5A63B66
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IPSEC_KEY_MANAGER_DICTATE_KEY0, IPSEC_KEY_MANAGER_DICTATE_KEY0 function, IPSEC_KEY_MANAGER_DICTATE_KEY0 function pointer [Filtering], fwp.ipsec_key_dictate_key0, fwp.ipsec_key_manager_dictate_key0, fwpmu/IPSEC_KEY_MANAGER_DICTATE_KEY0
ms.topic: callback
f1_keywords: 
 - "fwpmu/IPSEC_KEY_MANAGER_DICTATE_KEY0"
dev_langs:
 - c++
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - Fwpmu.h
api_name:
 - IPSEC_KEY_MANAGER_DICTATE_KEY0
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
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

Type: <b><a href="https://docs.microsoft.com/windows/desktop/api/ipsectypes/ns-ipsectypes-ipsec_sa_details1_">IPSEC_SA_DETAILS1</a>*</b>

Information about the inbound SA.


#### - outboundSa [in, out]

Type: <b><a href="https://docs.microsoft.com/windows/desktop/api/ipsectypes/ns-ipsectypes-ipsec_sa_details1_">IPSEC_SA_DETAILS1</a>*</b>

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
A Windows Filtering Platform (WFP) specific error. See <a href="https://docs.microsoft.com/windows/desktop/FWP/wfp-error-codes">WFP Error Codes</a> for details.

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



Call <a href="https://docs.microsoft.com/windows/desktop/api/fwpmu/nf-fwpmu-ipseckeymanageraddandregister0">IPsecKeyManagerAddAndRegister0</a> to invoke this function pointer. If the weight specified in <a href="https://docs.microsoft.com/windows/desktop/api/fwpmu/nc-fwpmu-ipsec_key_manager_key_dictation_check0">IPSEC_KEY_MANAGER_KEY_DICTATION_CHECK0</a> for a TIA is higher than that of any peer, <b>IPSEC_KEY_MANAGER_DICTATE_KEY0</b> will be invoked.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/fwpmu/nc-fwpmu-ipsec_key_manager_key_dictation_check0">IPSEC_KEY_MANAGER_KEY_DICTATION_CHECK0</a>



<a href="https://docs.microsoft.com/windows/desktop/api/ipsectypes/ns-ipsectypes-ipsec_sa_details1_">IPSEC_SA_DETAILS1</a>



<a href="https://docs.microsoft.com/windows/desktop/api/fwpmu/nf-fwpmu-ipseckeymanageraddandregister0">IPsecKeyManagerAddAndRegister0</a>



<a href="https://docs.microsoft.com/windows/desktop/FWP/fwp-functions">WFP  Functions</a>
 

 

