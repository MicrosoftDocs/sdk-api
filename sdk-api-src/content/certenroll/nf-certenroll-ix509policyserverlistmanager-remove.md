---
UID: NF:certenroll.IX509PolicyServerListManager.Remove
title: IX509PolicyServerListManager::Remove (certenroll.h)
description: Removes an IX509PolicyServerUrl object from the collection by index number.
helpviewer_keywords: ["IX509PolicyServerListManager interface [Security]","Remove method","IX509PolicyServerListManager.Remove","IX509PolicyServerListManager::Remove","Remove","Remove method [Security]","Remove method [Security]","IX509PolicyServerListManager interface","certenroll/IX509PolicyServerListManager::Remove","security.ix509policyserverlistmanager_remove"]
old-location: security\ix509policyserverlistmanager_remove.htm
tech.root: security
ms.assetid: c2e59087-a62b-4013-9a16-fedd03b2c286
ms.date: 12/05/2018
ms.keywords: IX509PolicyServerListManager interface [Security],Remove method, IX509PolicyServerListManager.Remove, IX509PolicyServerListManager::Remove, Remove, Remove method [Security], Remove method [Security],IX509PolicyServerListManager interface, certenroll/IX509PolicyServerListManager::Remove, security.ix509policyserverlistmanager_remove
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
 - IX509PolicyServerListManager::Remove
 - certenroll/IX509PolicyServerListManager::Remove
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
 - IX509PolicyServerListManager.Remove
---

# IX509PolicyServerListManager::Remove


## -description

The <b>Remove</b> method removes an <a href="/windows/desktop/api/certenroll/nn-certenroll-ix509policyserverurl">IX509PolicyServerUrl</a> object from the collection by index number.

## -parameters

### -param Index [in]

A <b>LONG</b> variable that contains the index of the object to remove.

## -returns

If the function succeeds, the function returns <b>S_OK</b>.

If the function fails, it returns an <b>HRESULT</b> value that indicates the error. For a list of common error codes, see <a href="/windows/desktop/SecCrypto/common-hresult-values">Common HRESULT Values</a>.

## -see-also

<a href="/windows/desktop/api/certenroll/nn-certenroll-ix509policyserverlistmanager">IX509PolicyServerListManager</a>