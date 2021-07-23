---
UID: NN:certenroll.ICspInformation
title: ICspInformation (certenroll.h)
description: Provides access to general information about a cryptographic provider.
helpviewer_keywords: ["ICspInformation","ICspInformation interface [Security]","ICspInformation interface [Security]","described","certenroll/ICspInformation","security.icspinformation"]
old-location: security\icspinformation.htm
tech.root: security
ms.assetid: e337ae2c-6f86-4025-8d31-47bc5d8a4ca8
ms.date: 12/05/2018
ms.keywords: ICspInformation, ICspInformation interface [Security], ICspInformation interface [Security],described, certenroll/ICspInformation, security.icspinformation
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
 - ICspInformation
 - certenroll/ICspInformation
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
 - ICspInformation
---

# ICspInformation interface


## -description

The <b>ICspInformation</b> interface provides access to general information about a cryptographic  provider. The information is initialized by calling the <a href="/windows/desktop/api/certenroll/nf-certenroll-icspinformation-initializefromname">InitializeFromName</a> or <a href="/windows/desktop/api/certenroll/nf-certenroll-icspinformation-initializefromtype">InitializeFromType</a> method. The information is retrieved by using the following methods and properties. For information about CSPs, see <a href="/windows/desktop/SecCrypto/csps-and-the-cryptography-process">CSPs and the Cryptography Process</a>.

## -inheritance

The <b>ICspInformation</b> interface inherits from the <a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface. <b>ICspInformation</b> also has these types of members:

## -see-also

<a href="/windows/desktop/SecCertEnroll/certenroll-interfaces">CertEnroll Interfaces</a>



<a href="/windows/desktop/api/certenroll/nn-certenroll-icspinformations">ICspInformations</a>



<a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a>
