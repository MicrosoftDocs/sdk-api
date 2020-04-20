---
UID: NF:certenroll.IPolicyQualifiers.Remove
title: IPolicyQualifiers::Remove (certenroll.h)
description: Removes an object from the collection by index value.helpviewer_keywords: ["IPolicyQualifiers interface [Security]","Remove method","IPolicyQualifiers.Remove","IPolicyQualifiers::Remove","Remove","Remove method [Security]","Remove method [Security]","IPolicyQualifiers interface","certenroll/IPolicyQualifiers::Remove","security.ipolicyqualifiers_remove_method"]
old-location: security\ipolicyqualifiers_remove_method.htm
tech.root: seccertenroll
ms.assetid: 6071dbc2-210d-42e2-8431-68eef1e89e24
ms.date: 12/05/2018
ms.keywords: IPolicyQualifiers interface [Security],Remove method, IPolicyQualifiers.Remove, IPolicyQualifiers::Remove, Remove, Remove method [Security], Remove method [Security],IPolicyQualifiers interface, certenroll/IPolicyQualifiers::Remove, security.ipolicyqualifiers_remove_method
f1_keywords:
- certenroll/IPolicyQualifiers.Remove
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
- IPolicyQualifiers.Remove
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IPolicyQualifiers::Remove


## -description


The <b>Remove</b> method removes an object from the collection by index value.


## -parameters




### -param Index [in]

A <b>LONG</b> variable that contains the index of the object to remove.


## -returns



If the function succeeds, the function returns <b>S_OK</b>.

If the function fails, it returns an <b>HRESULT</b> value that indicates the error. For a list of common error codes, see <a href="https://docs.microsoft.com/windows/desktop/SecCrypto/common-hresult-values">Common HRESULT Values</a>.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nn-certenroll-ipolicyqualifier">IPolicyQualifier</a>



<a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nn-certenroll-ipolicyqualifiers">IPolicyQualifiers</a>
 

 

