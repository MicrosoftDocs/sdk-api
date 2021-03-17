---
UID: NF:certenroll.ICspInformation.get_IsSmartCard
title: ICspInformation::get_IsSmartCard (certenroll.h)
description: Retrieves a Boolean value that specifies whether the provider is a smart card provider.
helpviewer_keywords: ["ICspInformation interface [Security]","IsSmartCard property","ICspInformation.IsSmartCard","ICspInformation.get_IsSmartCard","ICspInformation::IsSmartCard","ICspInformation::get_IsSmartCard","IsSmartCard property [Security]","IsSmartCard property [Security]","ICspInformation interface","certenroll/ICspInformation::IsSmartCard","certenroll/ICspInformation::get_IsSmartCard","get_IsSmartCard","security.icspinformation_issmartcard_property"]
old-location: security\icspinformation_issmartcard_property.htm
tech.root: security
ms.assetid: cfb88e17-39bb-4b4f-9eb3-3691376f8285
ms.date: 12/05/2018
ms.keywords: ICspInformation interface [Security],IsSmartCard property, ICspInformation.IsSmartCard, ICspInformation.get_IsSmartCard, ICspInformation::IsSmartCard, ICspInformation::get_IsSmartCard, IsSmartCard property [Security], IsSmartCard property [Security],ICspInformation interface, certenroll/ICspInformation::IsSmartCard, certenroll/ICspInformation::get_IsSmartCard, get_IsSmartCard, security.icspinformation_issmartcard_property
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
 - ICspInformation::get_IsSmartCard
 - certenroll/ICspInformation::get_IsSmartCard
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
 - ICspInformation.IsSmartCard
 - ICspInformation.get_IsSmartCard
---

# ICspInformation::get_IsSmartCard


## -description

The <b>IsSmartCard</b> property retrieves a Boolean value that specifies whether the provider is a smart card provider.

This property is read-only.

## -parameters

## -remarks

A smart card provider is typically identified by the <a href="/windows/desktop/api/certenroll/nf-certenroll-icspinformation-get_ishardwaredevice">IsHardwareDevice</a> property and the <a href="/windows/desktop/api/certenroll/nf-certenroll-icspinformation-get_issoftwaredevice">IsSoftwareDevice</a> property being set or the <a href="/windows/desktop/api/certenroll/nf-certenroll-icspinformation-get_isremovable">IsRemovable</a> property being set.

## -see-also

<a href="/windows/desktop/api/certenroll/nn-certenroll-icspinformation">ICspInformation</a>