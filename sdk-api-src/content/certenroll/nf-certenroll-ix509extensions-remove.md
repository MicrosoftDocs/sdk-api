---
UID: NF:certenroll.IX509Extensions.Remove
title: IX509Extensions::Remove (certenroll.h)

description: Removes an IX509Extension object from the collection by index number.
old-location: security\ix509extensions_remove_method.htm
tech.root: seccertenroll
ms.assetid: da1fcad3-7351-4d26-b483-a6548c3bdbec

ms.date: 12/05/2018
ms.keywords: IX509Extensions interface [Security],Remove method, IX509Extensions.Remove, IX509Extensions::Remove, Remove, Remove method [Security], Remove method [Security],IX509Extensions interface, certenroll/IX509Extensions::Remove, security.ix509extensions_remove_method
ms.topic: method
f1_keywords: 
 - "certenroll/IX509Extensions.Remove"
dev_langs:
 - c++
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - CertEnroll.dll
api_name:
 - IX509Extensions.Remove
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IX509Extensions::Remove


## -description


The <b>Remove</b> method removes an <a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nn-certenroll-ix509extension">IX509Extension</a> object from the collection by index number.


## -parameters




### -param Index [in]

A <b>LONG</b> variable that contains the index of the object to remove.


## -returns



If the function succeeds, the function returns <b>S_OK</b>.

If the function fails, it returns an <b>HRESULT</b> value that indicates the error. For a list of common error codes, see <a href="https://docs.microsoft.com/windows/desktop/SecCrypto/common-hresult-values">Common HRESULT Values</a>.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nn-certenroll-ix509extension">IX509Extension</a>



<a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nn-certenroll-ix509extensions">IX509Extensions</a>
 

 

