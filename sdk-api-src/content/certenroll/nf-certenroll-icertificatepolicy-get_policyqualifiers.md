---
UID: NF:certenroll.ICertificatePolicy.get_PolicyQualifiers
title: ICertificatePolicy::get_PolicyQualifiers
author: windows-sdk-content
description: Retrieves a collection of optional policy qualifiers that can be applied to a certificate policy.
old-location: security\icertificatepolicy_policyqualifiers_property.htm
tech.root: SecCertEnroll
ms.assetid: 7955dfa1-70b2-4b6e-975f-c489a6284c5c
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: ICertificatePolicy interface [Security],PolicyQualifiers property, ICertificatePolicy.PolicyQualifiers, ICertificatePolicy.get_PolicyQualifiers, ICertificatePolicy::PolicyQualifiers, ICertificatePolicy::get_PolicyQualifiers, PolicyQualifiers property [Security], PolicyQualifiers property [Security],ICertificatePolicy interface, certenroll/ICertificatePolicy::PolicyQualifiers, certenroll/ICertificatePolicy::get_PolicyQualifiers, get_PolicyQualifiers, security.icertificatepolicy_policyqualifiers_property
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: certenroll.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
req.dll: CertEnroll.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - CertEnroll.dll
api_name:
 - ICertificatePolicy.PolicyQualifiers
 - ICertificatePolicy.get_PolicyQualifiers
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ICertificatePolicy::get_PolicyQualifiers


## -description


The <b>PolicyQualifiers</b> property retrieves a collection of optional policy qualifiers that can be applied to a certificate policy.

This property is read-only.


## -parameters


## -remarks



An empty <a href="https://msdn.microsoft.com/en-us/library/Aa376804(v=VS.85).aspx">IPolicyQualifiers</a> object is created when you call the <a href="https://msdn.microsoft.com/en-us/library/Aa375226(v=VS.85).aspx">Initialize</a> method. You can call the <b>PolicyQualifiers</b> property to retrieve this object and specify qualifying information for the policy. Policy qualifiers only apply if you are creating a <b>CertificatePolicies</b> extension. For more information, see the <a href="https://msdn.microsoft.com/en-us/library/Aa378121(v=VS.85).aspx">IX509ExtensionCertificatePolicies</a>.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Aa375214(v=VS.85).aspx">ICertificatePolicies</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa375225(v=VS.85).aspx">ICertificatePolicy</a>
 

 

