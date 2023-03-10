---
UID: NF:certenroll.ICspInformation.get_IsHardwareDevice
title: ICspInformation::get_IsHardwareDevice (certenroll.h)
description: Retrieves a Boolean value that determines whether the provider is implemented in a hardware device.
helpviewer_keywords: ["ICspInformation interface [Security]","IsHardwareDevice property","ICspInformation.IsHardwareDevice","ICspInformation.get_IsHardwareDevice","ICspInformation::IsHardwareDevice","ICspInformation::get_IsHardwareDevice","IsHardwareDevice property [Security]","IsHardwareDevice property [Security]","ICspInformation interface","certenroll/ICspInformation::IsHardwareDevice","certenroll/ICspInformation::get_IsHardwareDevice","get_IsHardwareDevice","security.icspinformation_ishardwaredevice_property"]
old-location: security\icspinformation_ishardwaredevice_property.htm
tech.root: security
ms.assetid: d69ade8c-3b74-4391-9048-6511f3d7e9fa
ms.date: 12/05/2018
ms.keywords: ICspInformation interface [Security],IsHardwareDevice property, ICspInformation.IsHardwareDevice, ICspInformation.get_IsHardwareDevice, ICspInformation::IsHardwareDevice, ICspInformation::get_IsHardwareDevice, IsHardwareDevice property [Security], IsHardwareDevice property [Security],ICspInformation interface, certenroll/ICspInformation::IsHardwareDevice, certenroll/ICspInformation::get_IsHardwareDevice, get_IsHardwareDevice, security.icspinformation_ishardwaredevice_property
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
 - ICspInformation::get_IsHardwareDevice
 - certenroll/ICspInformation::get_IsHardwareDevice
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
 - ICspInformation.IsHardwareDevice
 - ICspInformation.get_IsHardwareDevice
---

# ICspInformation::get_IsHardwareDevice


## -description

The <b>IsHardwareDevice</b> property retrieves a Boolean value that determines whether the provider is implemented in a hardware device.

This property is read-only.

## -parameters

## -remarks

This property only specifies whether a provider is implemented in hardware. Because a provider can be implemented in both hardware and software, you cannot assume that a value of true for this property  indicates that there is no software component. You must also examine the <a href="/windows/desktop/api/certenroll/nf-certenroll-icspinformation-get_issoftwaredevice">IsSoftwareDevice</a> property. The following providers return true for the <b>IsHardwareDevice</b> property:<ul>
<li>Microsoft Smart Card Key Storage Provider</li>
<li>Microsoft Base Smart Card Crypto Provider</li>
</ul>


Both of these providers also return true for the <a href="/windows/desktop/api/certenroll/nf-certenroll-icspinformation-get_issoftwaredevice">IsSoftwareDevice</a> property. The Certificate Enrollment service assumes that a provider is a smart card provider if both the <b>IsHardwareDevice</b> and <b>IsSoftwareDevice</b> properties are set, or if the <a href="/windows/desktop/api/certenroll/nf-certenroll-icspinformation-get_isremovable">IsRemovable</a> property is set.

## -see-also

<a href="/windows/desktop/api/certenroll/nn-certenroll-icspinformation">ICspInformation</a>