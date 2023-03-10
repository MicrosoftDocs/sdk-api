---
UID: NF:certenroll.ICertificatePolicies.Remove
title: ICertificatePolicies::Remove (certenroll.h)
description: Removes an object from the collection by index number. (ICertificatePolicies.Remove)
helpviewer_keywords: ["ICertificatePolicies interface [Security]","Remove method","ICertificatePolicies.Remove","ICertificatePolicies::Remove","Remove","Remove method [Security]","Remove method [Security]","ICertificatePolicies interface","certenroll/ICertificatePolicies::Remove","security.icertificatepolicies_remove_method"]
old-location: security\icertificatepolicies_remove_method.htm
tech.root: security
ms.assetid: 5cd010bb-50ee-4251-815e-1fb4de1f2a81
ms.date: 12/05/2018
ms.keywords: ICertificatePolicies interface [Security],Remove method, ICertificatePolicies.Remove, ICertificatePolicies::Remove, Remove, Remove method [Security], Remove method [Security],ICertificatePolicies interface, certenroll/ICertificatePolicies::Remove, security.icertificatepolicies_remove_method
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
 - ICertificatePolicies::Remove
 - certenroll/ICertificatePolicies::Remove
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
 - ICertificatePolicies.Remove
---

# ICertificatePolicies::Remove


## -description

The <b>Remove</b> method removes an object from the collection by index number.

## -parameters

### -param Index [in]

A <b>LONG</b> variable that contains the index of the object to remove.

## -returns

If the function succeeds, the function returns <b>S_OK</b>.

If the function fails, it returns an <b>HRESULT</b> value that indicates the error. For a list of common error codes, see <a href="/windows/desktop/SecCrypto/common-hresult-values">Common HRESULT Values</a>.

## -see-also

<a href="/windows/desktop/api/certenroll/nn-certenroll-icertificatepolicies">ICertificatePolicies</a>



<a href="/windows/desktop/api/certenroll/nn-certenroll-icertificatepolicy">ICertificatePolicy</a>
