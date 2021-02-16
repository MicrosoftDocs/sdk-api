---
UID: NF:casetup.ICertificateEnrollmentServerSetup.get_ErrorString
title: ICertificateEnrollmentServerSetup::get_ErrorString (casetup.h)
description: Retrieves a string that contains additional information about Certificate Enrollment Web Service (CES) setup failure.
helpviewer_keywords: ["ErrorString property [Security]","ErrorString property [Security]","ICertificateEnrollmentServerSetup interface","ICertificateEnrollmentServerSetup interface [Security]","ErrorString property","ICertificateEnrollmentServerSetup.ErrorString","ICertificateEnrollmentServerSetup.get_ErrorString","ICertificateEnrollmentServerSetup::ErrorString","ICertificateEnrollmentServerSetup::get_ErrorString","casetup/ICertificateEnrollmentServerSetup::ErrorString","casetup/ICertificateEnrollmentServerSetup::get_ErrorString","get_ErrorString","security.icertificateenrollmentserversetup_errorstring"]
old-location: security\icertificateenrollmentserversetup_errorstring.htm
tech.root: security
ms.assetid: D4322BE8-1CED-47D0-98C2-D5D7C151DEAB
ms.date: 12/05/2018
ms.keywords: ErrorString property [Security], ErrorString property [Security],ICertificateEnrollmentServerSetup interface, ICertificateEnrollmentServerSetup interface [Security],ErrorString property, ICertificateEnrollmentServerSetup.ErrorString, ICertificateEnrollmentServerSetup.get_ErrorString, ICertificateEnrollmentServerSetup::ErrorString, ICertificateEnrollmentServerSetup::get_ErrorString, casetup/ICertificateEnrollmentServerSetup::ErrorString, casetup/ICertificateEnrollmentServerSetup::get_ErrorString, get_ErrorString, security.icertificateenrollmentserversetup_errorstring
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
 - ICertificateEnrollmentServerSetup::get_ErrorString
 - casetup/ICertificateEnrollmentServerSetup::get_ErrorString
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
 - ICertificateEnrollmentServerSetup.ErrorString
 - ICertificateEnrollmentServerSetup.get_ErrorString
---

# ICertificateEnrollmentServerSetup::get_ErrorString


## -description

The <b>ErrorString</b> property retrieves a string that contains additional information about Certificate Enrollment Web Service (CES) setup failure.

This property is read-only.

## -parameters

## -remarks

Calling any method on the <a href="/windows/desktop/api/casetup/nn-casetup-icertificateenrollmentserversetup">ICertificateEnrollmentServerSetup</a> interface resets this property value to an empty error string.

## -see-also

<a href="/windows/desktop/api/casetup/nn-casetup-icertificateenrollmentserversetup">ICertificateEnrollmentServerSetup</a>