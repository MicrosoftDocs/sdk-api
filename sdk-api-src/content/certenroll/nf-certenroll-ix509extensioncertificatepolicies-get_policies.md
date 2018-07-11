---
UID: NF:certenroll.IX509ExtensionCertificatePolicies.get_Policies
title: IX509ExtensionCertificatePolicies::get_Policies
author: windows-sdk-content
description: Retrieves a collection of certificate policies.
old-location: security\ix509extensioncertificatepolicies_policies_property.htm
old-project: seccertenroll
ms.assetid: eefb515d-62dc-4ad7-b0c4-c65a4da5742e
ms.author: windowssdkdev
ms.date: 05/11/2018
ms.keywords: IX509ExtensionCertificatePolicies interface [Security],Policies property, IX509ExtensionCertificatePolicies.Policies, IX509ExtensionCertificatePolicies.get_Policies, IX509ExtensionCertificatePolicies::Policies, IX509ExtensionCertificatePolicies::get_Policies, Policies property [Security], Policies property [Security],IX509ExtensionCertificatePolicies interface, certenroll/IX509ExtensionCertificatePolicies::Policies, certenroll/IX509ExtensionCertificatePolicies::get_Policies, get_Policies, security.ix509extensioncertificatepolicies_policies_property
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: X509RequestType
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - CertEnroll.dll
api_name:
 - IX509ExtensionCertificatePolicies.Policies
 - IX509ExtensionCertificatePolicies.get_Policies
product: Windows
targetos: Windows
req.lib: 
req.dll: CertEnroll.dll
req.irql: 
---

# IX509ExtensionCertificatePolicies::get_Policies


## -description


The <b>Policies</b> property retrieves a collection of certificate policies.

This property is read-only.


## -parameters


## -remarks



Call the <a href="https://msdn.microsoft.com/3134c668-afe6-447b-9f0e-8c21df36e131">InitializeEncode</a> method or the <a href="https://msdn.microsoft.com/bd542fbd-4cba-4584-9a14-b22cf0ae5705">InitializeDecode</a> method to initialize the collection.  You can also call the <a href="https://msdn.microsoft.com/library/windows/hardware/mt158256">Critical</a> property to specify and retrieve a Boolean value that identifies whether the extension is critical, and you can call the <a href="https://msdn.microsoft.com/d3508bfe-e323-4075-9c82-d9b53b8f54aa">ObjectId</a> property to retrieve the <a href="https://msdn.microsoft.com/e6be8932-015e-4058-b249-1671b3fea521">object identifier</a> (OID) associated with the extension.




## -see-also




<a href="https://msdn.microsoft.com/d35d155c-fb81-4d7e-b5c9-82ac5af4b79e">IX509ExtensionCertificatePolicies</a>
 

 

