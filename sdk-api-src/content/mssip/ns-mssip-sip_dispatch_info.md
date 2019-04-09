---
UID: NS:mssip.SIP_DISPATCH_INFO_
title: SIP_DISPATCH_INFO (mssip.h)
author: windows-sdk-content
description: Contains a set of function pointers assigned by the CryptSIPLoad function that your application uses to perform subject interface package (SIP) operations.
old-location: security\sip_dispatch_info.htm
tech.root: SecCrypto
ms.assetid: d34b5081-0af8-4dcc-8133-a91d0603d419
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: "*LPSIP_DISPATCH_INFO, PSIP_DISPATCH_INFO, PSIP_DISPATCH_INFO structure pointer [Security], SIP_DISPATCH_INFO, SIP_DISPATCH_INFO structure [Security], mssip/PSIP_DISPATCH_INFO, mssip/SIP_DISPATCH_INFO, security.sip_dispatch_info"
ms.topic: struct
req.header: mssip.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
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
 - HeaderDef
api_location:
 - Mssip.h
api_name:
 - SIP_DISPATCH_INFO
product: Windows
targetos: Windows
req.typenames: SIP_DISPATCH_INFO, *LPSIP_DISPATCH_INFO
req.redist: 
---

# SIP_DISPATCH_INFO structure


## -description


The <b>SIP_DISPATCH_INFO</b> structure contains a set of function pointers assigned by the <a href="https://msdn.microsoft.com/3378ecee-bd5d-45e5-9a1f-a3734d086782">CryptSIPLoad</a> function that your application uses to perform <a href="https://msdn.microsoft.com/3e9d7672-2314-45c8-8178-5a0afcfd0c50">subject interface package</a> (SIP) operations.


## -struct-fields




### -field cbSize

The size, in bytes, of this structure.


### -field hSIP

This member is reserved and must be set to <b>NULL</b>.


### -field pfGet

A pointer to the function that retrieves the signed data for the subject. The signature for this function pointer is described in <a href="https://msdn.microsoft.com/e3fabaa7-2dda-4c6c-8d1a-3ee5363e10b5">CryptSIPGetSignedDataMsg</a>.


### -field pfPut

A pointer to the function that stores the signed data for the subject. The signature for this function pointer is described in <a href="https://msdn.microsoft.com/731f64bf-49f0-4799-b84a-9ca04292aa91">CryptSIPPutSignedDataMsg</a>.


### -field pfCreate

A pointer to the function that returns a <a href="https://msdn.microsoft.com/d34b599b-fe49-47c4-bb52-73ee14d73253">SIP_INDIRECT_DATA</a>  structure that contains the subject data. This structure contains the hash of the target. The signature for this function pointer is described in <a href="https://msdn.microsoft.com/bb4ecc95-972f-415c-9722-59b00a27cddc">CryptSIPCreateIndirectData</a>.


### -field pfVerify

A pointer to the function that verifies the <a href="https://msdn.microsoft.com/d34b599b-fe49-47c4-bb52-73ee14d73253">SIP_INDIRECT_DATA</a>  structure that contains the subject data. This structure contains the hash of the target. The signature for this function pointer is described in <a href="https://msdn.microsoft.com/137b8858-a31f-4ef6-96bd-c5e26ae7b3e8">CryptSIPVerifyIndirectData</a>.


### -field pfRemove

A pointer to the function that removes the signed data for the subject. The signature for this function pointer is described in <a href="https://msdn.microsoft.com/c3ea46bb-931a-4ca6-93f5-db7e07b4cb7a">CryptSIPRemoveSignedDataMsg</a>.


## -remarks



Your application must initialize this structure to binary zeros and set <b>cbSize</b> to <code>sizeof(SIP_DISPATCH_INFO)</code> by calling the <a href="http://go.microsoft.com/fwlink/p/?linkid=106519">memset</a> function before calling the <a href="https://msdn.microsoft.com/3378ecee-bd5d-45e5-9a1f-a3734d086782">CryptSIPLoad</a> function. Your application can use the function pointers in the returned <b>SIP_DISPATCH_INFO</b> structure to perform the necessary SIP operations.   The function pointers can point to functions exported by third party SIPs.




## -see-also




<a href="https://msdn.microsoft.com/bb4ecc95-972f-415c-9722-59b00a27cddc">CryptSIPCreateIndirectData</a>



<a href="https://msdn.microsoft.com/e3fabaa7-2dda-4c6c-8d1a-3ee5363e10b5">CryptSIPGetSignedDataMsg</a>



<a href="https://msdn.microsoft.com/731f64bf-49f0-4799-b84a-9ca04292aa91">CryptSIPPutSignedDataMsg</a>



<a href="https://msdn.microsoft.com/c3ea46bb-931a-4ca6-93f5-db7e07b4cb7a">CryptSIPRemoveSignedDataMsg</a>



<a href="https://msdn.microsoft.com/137b8858-a31f-4ef6-96bd-c5e26ae7b3e8">CryptSIPVerifyIndirectData</a>
 

 

