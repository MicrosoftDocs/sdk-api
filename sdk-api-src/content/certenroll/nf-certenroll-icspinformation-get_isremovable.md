---
UID: NF:certenroll.ICspInformation.get_IsRemovable
title: ICspInformation::get_IsRemovable (certenroll.h)
description: Retrieves a Boolean value that specifies whether the token that contains the key can be removed.
helpviewer_keywords: ["ICspInformation interface [Security]","IsRemovable property","ICspInformation.IsRemovable","ICspInformation.get_IsRemovable","ICspInformation::IsRemovable","ICspInformation::get_IsRemovable","IsRemovable property [Security]","IsRemovable property [Security]","ICspInformation interface","certenroll/ICspInformation::IsRemovable","certenroll/ICspInformation::get_IsRemovable","get_IsRemovable","security.icspinformation_isremovable_property"]
old-location: security\icspinformation_isremovable_property.htm
tech.root: security
ms.assetid: ee67670b-80a9-4637-a5ed-84d3430853ea
ms.date: 12/05/2018
ms.keywords: ICspInformation interface [Security],IsRemovable property, ICspInformation.IsRemovable, ICspInformation.get_IsRemovable, ICspInformation::IsRemovable, ICspInformation::get_IsRemovable, IsRemovable property [Security], IsRemovable property [Security],ICspInformation interface, certenroll/ICspInformation::IsRemovable, certenroll/ICspInformation::get_IsRemovable, get_IsRemovable, security.icspinformation_isremovable_property
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
 - ICspInformation::get_IsRemovable
 - certenroll/ICspInformation::get_IsRemovable
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
 - ICspInformation.IsRemovable
 - ICspInformation.get_IsRemovable
---

# ICspInformation::get_IsRemovable


## -description

The <b>IsRemovable</b> property retrieves a Boolean value that specifies whether the token that contains the key can be removed.

This property is read-only.

## -parameters

## -remarks

Operator cards and  smart cards are examples of removable tokens that can contain keys. For example, the following providers return true for this property value:<ul>
<li>Microsoft Smart Card Key Storage Provider</li>
<li>Microsoft Base Smart Card Crypto Provider</li>
</ul>


The Certificate Enrollment service assumes that a provider is a smart card provider if both the <a href="/windows/desktop/api/certenroll/nf-certenroll-icspinformation-get_ishardwaredevice">IsHardwareDevice</a> and <a href="/windows/desktop/api/certenroll/nf-certenroll-icspinformation-get_issoftwaredevice">IsSoftwareDevice</a> properties are set, or if the <b>IsRemovable</b> property is set.

## -see-also

<a href="/windows/desktop/api/certenroll/nn-certenroll-icspinformation">ICspInformation</a>