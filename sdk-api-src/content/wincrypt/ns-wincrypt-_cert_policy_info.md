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
 

 

