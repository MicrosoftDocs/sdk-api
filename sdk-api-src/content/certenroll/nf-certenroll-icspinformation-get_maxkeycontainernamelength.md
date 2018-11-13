---
UID: NF:certenroll.ICspInformation.get_MaxKeyContainerNameLength
title: ICspInformation::get_MaxKeyContainerNameLength
author: windows-sdk-content
description: Retrieves the maximum supported length for the name of the private key container associated with the provider.
old-location: security\icspinformation_maxkeycontainernamelength_property.htm
tech.root: SecCertEnroll
ms.assetid: 2508786f-0892-4ece-bbef-bd8ed9c81eee
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: ICspInformation interface [Security],MaxKeyContainerNameLength property, ICspInformation.MaxKeyContainerNameLength, ICspInformation.get_MaxKeyContainerNameLength, ICspInformation::MaxKeyContainerNameLength, ICspInformation::get_MaxKeyContainerNameLength, MaxKeyContainerNameLength property [Security], MaxKeyContainerNameLength property [Security],ICspInformation interface, certenroll/ICspInformation::MaxKeyContainerNameLength, certenroll/ICspInformation::get_MaxKeyContainerNameLength, get_MaxKeyContainerNameLength, security.icspinformation_maxkeycontainernamelength_property
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
 - ICspInformation.MaxKeyContainerNameLength
 - ICspInformation.get_MaxKeyContainerNameLength
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ICspInformation::get_MaxKeyContainerNameLength


## -description


The <b>MaxKeyContainerNameLength</b> property retrieves the maximum supported length for the name of the private key container associated with the provider.

This property is read-only.


## -parameters


## -remarks



The key container name can be specified and retrieved by calling the <a href="https://msdn.microsoft.com/1d56fa7e-8113-461d-a4f0-ebc048fbcb49">ContainerName</a> property on the <a href="https://msdn.microsoft.com/72612ea4-ed45-46ac-9dad-614a9a754d83">IX509PrivateKey</a> interface. The values associated with the providers distributed by Microsoft are listed in the following table. Some of these providers may not be included on all operating systems and others may be included instead.<table>
<tr>
<th>Provider</th>
<th>MaxKeyContainerNameLength value</th>
</tr>
<tr>
<td>Microsoft Software Key Storage Provider</td>
<td>261</td>
</tr>
<tr>
<td>Microsoft Smart Card Key Storage Provider</td>
<td>40</td>
</tr>
<tr>
<td>Microsoft Base Cryptographic Provider v1.0</td>
<td>261</td>
</tr>
<tr>
<td>Microsoft Base DSS and Diffie-Hellman Cryptographic Provider</td>
<td>261</td>
</tr>
<tr>
<td>Microsoft Base DSS Cryptographic Provider</td>
<td>261</td>
</tr>
<tr>
<td>Microsoft Base Smart Card Crypto Provider</td>
<td>40</td>
</tr>
<tr>
<td>Microsoft DH Schannel Cryptographic Provider</td>
<td>261</td>
</tr>
<tr>
<td>Microsoft Enhanced Cryptographic Provider v1.0</td>
<td>261</td>
</tr>
<tr>
<td>Microsoft Enhanced DSS and Diffie-Hellman Cryptographic Provider</td>
<td>261</td>
</tr>
<tr>
<td>Microsoft Enhanced RSA and AES Cryptographic Provider</td>
<td>261</td>
</tr>
<tr>
<td>Microsoft RSA Schannel Cryptographic Provider</td>
<td>261</td>
</tr>
<tr>
<td>Microsoft Strong Cryptographic Provider</td>
<td>261</td>
</tr>
</table>
 






## -see-also




<a href="https://msdn.microsoft.com/e337ae2c-6f86-4025-8d31-47bc5d8a4ca8">ICspInformation</a>
 

 

