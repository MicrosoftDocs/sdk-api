---
UID: NF:certenroll.ICspInformations.Remove
title: ICspInformations::Remove (certenroll.h)
description: Removes an ICspInformation object from the collection by index number.
helpviewer_keywords: ["ICspInformations interface [Security]","Remove method","ICspInformations.Remove","ICspInformations::Remove","Remove","Remove method [Security]","Remove method [Security]","ICspInformations interface","certenroll/ICspInformations::Remove","security.icspinformations_remove_method"]
old-location: security\icspinformations_remove_method.htm
tech.root: security
ms.assetid: cbf427d8-3f66-4a54-a226-2060c58924b6
ms.date: 12/05/2018
ms.keywords: ICspInformations interface [Security],Remove method, ICspInformations.Remove, ICspInformations::Remove, Remove, Remove method [Security], Remove method [Security],ICspInformations interface, certenroll/ICspInformations::Remove, security.icspinformations_remove_method
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
 - ICspInformations::Remove
 - certenroll/ICspInformations::Remove
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
 - ICspInformations.Remove
---

# ICspInformations::Remove


## -description

The <b>Remove</b> method removes an <a href="/windows/desktop/api/certenroll/nn-certenroll-icspinformation">ICspInformation</a> object from the collection by index number.

## -parameters

### -param Index [in]

A <b>LONG</b> variable that contains the index of the object to remove.

## -returns

If the function succeeds, the function returns <b>S_OK</b>.

If the function fails, it returns an <b>HRESULT</b> value that indicates the error. For a list of common error codes, see <a href="/windows/desktop/SecCrypto/common-hresult-values">Common HRESULT Values</a>.

## -see-also

<a href="/windows/desktop/api/certenroll/nn-certenroll-icspinformation">ICspInformation</a>



<a href="/windows/desktop/api/certenroll/nn-certenroll-icspinformations">ICspInformations</a>