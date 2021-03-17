---
UID: NF:casetup.ICertificateEnrollmentPolicyServerSetup.get_ErrorString
title: ICertificateEnrollmentPolicyServerSetup::get_ErrorString (casetup.h)
description: Retrieves a string that contains additional information about Certificate Enrollment Policy (CEP) Web Service setup failure.
helpviewer_keywords: ["ErrorString property [Security]","ErrorString property [Security]","ICertificateEnrollmentPolicyServerSetup interface","ICertificateEnrollmentPolicyServerSetup interface [Security]","ErrorString property","ICertificateEnrollmentPolicyServerSetup.ErrorString","ICertificateEnrollmentPolicyServerSetup.get_ErrorString","ICertificateEnrollmentPolicyServerSetup::ErrorString","ICertificateEnrollmentPolicyServerSetup::get_ErrorString","casetup/ICertificateEnrollmentPolicyServerSetup::ErrorString","casetup/ICertificateEnrollmentPolicyServerSetup::get_ErrorString","get_ErrorString","security.icertificateenrollmentpolicyserversetup_errorstring"]
old-location: security\icertificateenrollmentpolicyserversetup_errorstring.htm
tech.root: security
ms.assetid: CA9103BD-96CA-4FF3-B78D-A1F1345E58D3
ms.date: 12/05/2018
ms.keywords: ErrorString property [Security], ErrorString property [Security],ICertificateEnrollmentPolicyServerSetup interface, ICertificateEnrollmentPolicyServerSetup interface [Security],ErrorString property, ICertificateEnrollmentPolicyServerSetup.ErrorString, ICertificateEnrollmentPolicyServerSetup.get_ErrorString, ICertificateEnrollmentPolicyServerSetup::ErrorString, ICertificateEnrollmentPolicyServerSetup::get_ErrorString, casetup/ICertificateEnrollmentPolicyServerSetup::ErrorString, casetup/ICertificateEnrollmentPolicyServerSetup::get_ErrorString, get_ErrorString, security.icertificateenrollmentpolicyserversetup_errorstring
req.header: casetup.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Casetup.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: Certocm.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ICertificateEnrollmentPolicyServerSetup::get_ErrorString
 - casetup/ICertificateEnrollmentPolicyServerSetup::get_ErrorString
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Certocm.dll
api_name:
 - ICertificateEnrollmentPolicyServerSetup.ErrorString
 - ICertificateEnrollmentPolicyServerSetup.get_ErrorString
---

# ICertificateEnrollmentPolicyServerSetup::get_ErrorString


## -description

The <b>ErrorString</b> property retrieves a string that contains additional information about Certificate Enrollment Policy (CEP) Web Service setup failure.

This property is read-only.

## -parameters

## -remarks

Calling any method on the <a href="/windows/desktop/api/casetup/nn-casetup-icertificateenrollmentpolicyserversetup">ICertificateEnrollmentPolicyServerSetup</a> interface resets this property value to an empty error string.

## -see-also

<a href="/windows/desktop/api/casetup/nn-casetup-icertificateenrollmentpolicyserversetup">ICertificateEnrollmentPolicyServerSetup</a>