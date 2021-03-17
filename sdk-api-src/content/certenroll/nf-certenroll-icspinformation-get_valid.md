---
UID: NF:certenroll.ICspInformation.get_Valid
title: ICspInformation::get_Valid (certenroll.h)
description: Retrieves a Boolean value that specifies whether the provider is installed on the client computer.
helpviewer_keywords: ["ICspInformation interface [Security]","Valid property","ICspInformation.Valid","ICspInformation.get_Valid","ICspInformation::Valid","ICspInformation::get_Valid","Valid property [Security]","Valid property [Security]","ICspInformation interface","certenroll/ICspInformation::Valid","certenroll/ICspInformation::get_Valid","get_Valid","security.icspinformation_valid_property"]
old-location: security\icspinformation_valid_property.htm
tech.root: security
ms.assetid: 507896b0-598c-4a2d-854e-d4d266fdfaf7
ms.date: 12/05/2018
ms.keywords: ICspInformation interface [Security],Valid property, ICspInformation.Valid, ICspInformation.get_Valid, ICspInformation::Valid, ICspInformation::get_Valid, Valid property [Security], Valid property [Security],ICspInformation interface, certenroll/ICspInformation::Valid, certenroll/ICspInformation::get_Valid, get_Valid, security.icspinformation_valid_property
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
 - ICspInformation::get_Valid
 - certenroll/ICspInformation::get_Valid
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
 - ICspInformation.Valid
 - ICspInformation.get_Valid
---

# ICspInformation::get_Valid


## -description

The <b>Valid</b> property retrieves a Boolean value that specifies whether the provider is installed on the client computer.

This property is read-only.

## -parameters

## -remarks

The <b>Valid</b> property is typically set by the Certificate Enrollment Control when it processes the list of providers identified in a template-based certificate request. If a provider listed in the template is not installed on the client, the control creates an <a href="/windows/desktop/api/certenroll/nn-certenroll-icspinformation">ICspInformation</a> object and sets the value of this property to false. You can use this property value in a user interface to indicate whether a provider is available. If a provider is not installed, only the <b>Valid</b> property and the <a href="/windows/desktop/api/certenroll/nf-certenroll-icspinformation-get_name">Name</a> property provide meaningful information.

## -see-also

<a href="/windows/desktop/api/certenroll/nn-certenroll-icspinformation">ICspInformation</a>