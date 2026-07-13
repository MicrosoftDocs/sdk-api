---
UID: NF:certenroll.ICertificatePolicies.Add
title: ICertificatePolicies::Add (certenroll.h)
description: Adds an object to the collection. (ICertificatePolicies.Add)
helpviewer_keywords: ["Add","Add method [Security]","Add method [Security]","ICertificatePolicies interface","ICertificatePolicies interface [Security]","Add method","ICertificatePolicies.Add","ICertificatePolicies::Add","certenroll/ICertificatePolicies::Add","security.icertificatepolicies_add_method"]
old-location: security\icertificatepolicies_add_method.htm
tech.root: security
ms.assetid: 85dc750c-ef18-4136-962e-c95bcca05b9a
ms.date: 12/05/2018
ms.keywords: Add, Add method [Security], Add method [Security],ICertificatePolicies interface, ICertificatePolicies interface [Security],Add method, ICertificatePolicies.Add, ICertificatePolicies::Add, certenroll/ICertificatePolicies::Add, security.icertificatepolicies_add_method
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
 - ICertificatePolicies::Add
 - certenroll/ICertificatePolicies::Add
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
 - ICertificatePolicies.Add
---

# ICertificatePolicies::Add


## -description

The <b>Add</b> method adds an object to the collection.

## -parameters

### -param pVal [in]

Pointer to the <a href="/windows/desktop/api/certenroll/nn-certenroll-icertificatepolicy">ICertificatePolicy</a> interface to add.

## -returns

If the function succeeds, the function returns <b>S_OK</b>.

If the function fails, it returns an <b>HRESULT</b> value that indicates the error. For a list of common error codes, see <a href="/windows/desktop/SecCrypto/common-hresult-values">Common HRESULT Values</a>.

## -see-also

<a href="/windows/desktop/api/certenroll/nn-certenroll-icertificatepolicies">ICertificatePolicies</a>



<a href="/windows/desktop/api/certenroll/nn-certenroll-icertificatepolicy">ICertificatePolicy</a>
