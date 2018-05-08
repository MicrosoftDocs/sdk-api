---
UID: NS:wincrypt._CERT_POLICY_ID
title: "_CERT_POLICY_ID"
author: windows-driver-content
description: The CERT_POLICY_ID structure contains a list of certificate policies that the certificate expressly supports, together with optional qualifier information pertaining to these policies.
old-location: security\cert_policy_id.htm
old-project: SecCrypto
ms.assetid: d0a8989c-3a32-4093-9db3-0811049b6601
ms.author: windowsdriverdev
ms.date: 4/30/2018
ms.keywords: "*PCERT_POLICY_ID, CERT_POLICY_ID, CERT_POLICY_ID structure [Security], PCERT_POLICY_ID, PCERT_POLICY_ID structure pointer [Security], _CERT_POLICY_ID, _crypto2_cert_policy_id, security.cert_policy_id, wincrypt/CERT_POLICY_ID, wincrypt/PCERT_POLICY_ID"
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: wincrypt.h
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
req.typenames: CERT_POLICY_ID, *PCERT_POLICY_ID
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Wincrypt.h
api_name:
-	CERT_POLICY_ID
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
---

# _CERT_POLICY_ID structure


## -description


The <b>CERT_POLICY_ID</b> structure contains a list of certificate policies that the certificate expressly supports, together with optional qualifier information pertaining to these policies.

<b>CERT_POLICY_ID</b> is a component of 
<a href="https://msdn.microsoft.com/f949c8e5-055d-4919-abcc-441880ccce56">CERT_KEY_USAGE_RESTRICTION_INFO</a>.


## -struct-fields




### -field cCertPolicyElementId

Number of elements in the <b>rgpszCertPolicyElementId</b> array.
					


### -field rgpszCertPolicyElementId

Array of pointers to policy element identifier strings.


## -see-also




<a href="https://msdn.microsoft.com/f949c8e5-055d-4919-abcc-441880ccce56">CERT_KEY_USAGE_RESTRICTION_INFO</a>
 

 

