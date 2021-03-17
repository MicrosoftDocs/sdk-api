---
UID: NF:certenroll.IX509PolicyServerListManager.Add
title: IX509PolicyServerListManager::Add (certenroll.h)
description: Adds an IX509PolicyServerUrl object to the collection.
helpviewer_keywords: ["Add","Add method [Security]","Add method [Security]","IX509PolicyServerListManager interface","IX509PolicyServerListManager interface [Security]","Add method","IX509PolicyServerListManager.Add","IX509PolicyServerListManager::Add","certenroll/IX509PolicyServerListManager::Add","security.ix509policyserverlistmanager_add"]
old-location: security\ix509policyserverlistmanager_add.htm
tech.root: security
ms.assetid: f1f22d27-96bf-47f7-8572-5f3842797c18
ms.date: 12/05/2018
ms.keywords: Add, Add method [Security], Add method [Security],IX509PolicyServerListManager interface, IX509PolicyServerListManager interface [Security],Add method, IX509PolicyServerListManager.Add, IX509PolicyServerListManager::Add, certenroll/IX509PolicyServerListManager::Add, security.ix509policyserverlistmanager_add
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
 - IX509PolicyServerListManager::Add
 - certenroll/IX509PolicyServerListManager::Add
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
 - IX509PolicyServerListManager.Add
---

# IX509PolicyServerListManager::Add


## -description

The <b>Add</b> method adds an <a href="/windows/desktop/api/certenroll/nn-certenroll-ix509policyserverurl">IX509PolicyServerUrl</a> object to the collection.

## -parameters

### -param pVal [in]

Pointer to the <a href="/windows/desktop/api/certenroll/nn-certenroll-ix509policyserverurl">IX509PolicyServerUrl</a> object to add.

## -returns

If the function succeeds, the function returns <b>S_OK</b>.

If the function fails, it returns an <b>HRESULT</b> value that indicates the error. For a list of common error codes, see <a href="/windows/desktop/SecCrypto/common-hresult-values">Common HRESULT Values</a>.

## -see-also

<a href="/windows/desktop/api/certenroll/nn-certenroll-ix509policyserverlistmanager">IX509PolicyServerListManager</a>