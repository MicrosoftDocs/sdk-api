---
UID: NF:certenroll.ICspInformation.get_IsSoftwareDevice
title: ICspInformation::get_IsSoftwareDevice (certenroll.h)
description: Retrieves a Boolean value that specifies whether the provider is implemented in software.
helpviewer_keywords: ["ICspInformation interface [Security]","IsSoftwareDevice property","ICspInformation.IsSoftwareDevice","ICspInformation.get_IsSoftwareDevice","ICspInformation::IsSoftwareDevice","ICspInformation::get_IsSoftwareDevice","IsSoftwareDevice property [Security]","IsSoftwareDevice property [Security]","ICspInformation interface","certenroll/ICspInformation::IsSoftwareDevice","certenroll/ICspInformation::get_IsSoftwareDevice","get_IsSoftwareDevice","security.icspinformation_issoftwaredevice_property"]
old-location: security\icspinformation_issoftwaredevice_property.htm
tech.root: security
ms.assetid: 50f78dcc-4d32-40c9-8153-f0b6ac72c03b
ms.date: 12/05/2018
ms.keywords: ICspInformation interface [Security],IsSoftwareDevice property, ICspInformation.IsSoftwareDevice, ICspInformation.get_IsSoftwareDevice, ICspInformation::IsSoftwareDevice, ICspInformation::get_IsSoftwareDevice, IsSoftwareDevice property [Security], IsSoftwareDevice property [Security],ICspInformation interface, certenroll/ICspInformation::IsSoftwareDevice, certenroll/ICspInformation::get_IsSoftwareDevice, get_IsSoftwareDevice, security.icspinformation_issoftwaredevice_property
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ICspInformation::get_IsSoftwareDevice
 - certenroll/ICspInformation::get_IsSoftwareDevice
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - CertEnroll.dll
api_name:
 - ICspInformation.IsSoftwareDevice
 - ICspInformation.get_IsSoftwareDevice
---

# ICspInformation::get_IsSoftwareDevice


## -description

The <b>IsSoftwareDevice</b> property retrieves a Boolean value that specifies whether the provider is implemented in software.

This property is read-only.

## -parameters

## -remarks

This property only specifies whether a provider is implemented in software. Because a provider can be implemented in both hardware and software, you cannot assume that a value of true for the <b>IsSoftwareDevice</b> property indicates that there is no hardware component. You must also examine the <a href="/windows/desktop/api/certenroll/nf-certenroll-icspinformation-get_ishardwaredevice">IsHardwareDevice</a> property. The following Microsoft providers return true for the <b>IsSoftwareDevice</b> property:<ul>
<li>Microsoft Software Key Storage Provider</li>
<li>Microsoft Smart Card Key Storage Provider</li>
<li>Microsoft Base Cryptographic Provider v1.0</li>
<li>Microsoft Base DSS and Diffie-Hellman Cryptographic Provider</li>
<li>Microsoft Base DSS Cryptographic Provider</li>
<li>Microsoft Base Smart Card Crypto Provider</li>
<li>Microsoft DH Schannel Cryptographic Provider</li>
<li>Microsoft Enhanced Cryptographic Provider v1.0</li>
<li>Microsoft Enhanced DSS and Diffie-Hellman Cryptographic Provider</li>
<li>Microsoft Enhanced RSA and AES Cryptographic Provider</li>
<li>Microsoft RSA Schannel Cryptographic Provider</li>
<li>Microsoft Strong Cryptographic Provider</li>
</ul>


The Microsoft Smart Card Key Storage Provider and the Microsoft Base Smart Card Crypto Provider also return true for the <a href="/windows/desktop/api/certenroll/nf-certenroll-icspinformation-get_ishardwaredevice">IsHardwareDevice</a> property. The Certificate Enrollment service assumes a smart card provider if both the <b>IsHardwareDevice</b> and <b>IsSoftwareDevice</b> properties are set, or if the <a href="/windows/desktop/api/certenroll/nf-certenroll-icspinformation-get_isremovable">IsRemovable</a> property is set.

## -see-also

<a href="/windows/desktop/api/certenroll/nn-certenroll-icspinformation">ICspInformation</a>