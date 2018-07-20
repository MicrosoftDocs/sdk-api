---
UID: NS:wincrypt._CERT_POLICY_INFO
title: "_CERT_POLICY_INFO"
author: windows-sdk-content
description: The CERT_POLICY_INFO structure contains an object identifier (OID) specifying a policy and an optional array of policy qualifiers.
old-location: security\cert_policy_info.htm
old-project: seccrypto
ms.assetid: 0d6396fe-99f6-4f66-9f01-55582d24ddc1
ms.author: windowssdkdev
ms.date: 07/16/2018
ms.keywords: "*PCERT_POLICY_INFO, CERT_POLICY_INFO, CERT_POLICY_INFO structure [Security], PCERT_POLICY_INFO, PCERT_POLICY_INFO structure pointer [Security], _CERT_POLICY_INFO, _crypto2_cert_policy_info, security.cert_policy_info, wincrypt/CERT_POLICY_INFO, wincrypt/PCERT_POLICY_INFO"
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: CERT_POLICY_INFO, *PCERT_POLICY_INFO
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Wincrypt.h
api_name:
 - CERT_POLICY_INFO
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
---

# _CERT_POLICY_INFO structure


## -description


The <b>CERT_POLICY_INFO</b> structure contains an object identifier (OID) specifying a policy and an optional array of policy qualifiers.

The <b>CERT_POLICY_INFO</b> structure is a component of 
<a href="https://msdn.microsoft.com/cf5fafd9-6129-4f25-8d61-189b46585e57">CERT_POLICIES_INFO</a>.


## -struct-fields




### -field pszPolicyIdentifier

Object identifier (OID) string specifying the policy.
					


### -field cPolicyQualifier

Number of elements in the <b>rgPolicyQualifier</b> array.


### -field rgPolicyQualifier

Array of 
<a href="https://msdn.microsoft.com/86b1716d-541f-4e06-a824-01c22f0eba27">CERT_POLICY_QUALIFIER_INFO</a> structures.


## -see-also




<a href="https://msdn.microsoft.com/cf5fafd9-6129-4f25-8d61-189b46585e57">CERT_POLICIES_INFO</a>



<a href="https://msdn.microsoft.com/86b1716d-541f-4e06-a824-01c22f0eba27">CERT_POLICY_QUALIFIER_INFO</a>
 

 

