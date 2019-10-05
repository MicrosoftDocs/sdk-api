---
UID: NF:certenroll.IPolicyQualifiers.Add
title: IPolicyQualifiers::Add (certenroll.h)
author: windows-sdk-content
description: Adds an object to the collection.
old-location: security\ipolicyqualifiers_add_method.htm
tech.root: seccertenroll
ms.assetid: 41ead360-0b11-4e47-86c5-24e636cc589d
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: Add, Add method [Security], Add method [Security],IPolicyQualifiers interface, IPolicyQualifiers interface [Security],Add method, IPolicyQualifiers.Add, IPolicyQualifiers::Add, certenroll/IPolicyQualifiers::Add, security.ipolicyqualifiers_add_method
ms.topic: method
f1_keywords: 
 - "certenroll/IPolicyQualifiers.Add"
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
 - IPolicyQualifiers.Add
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IPolicyQualifiers::Add


## -description


The <b>Add</b> method adds an object to the collection.


## -parameters




### -param pVal [in]

Pointer to the <a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nn-certenroll-ipolicyqualifier">IPolicyQualifier</a> interface to add.


## -returns



If the function succeeds, the function returns <b>S_OK</b>.

If the function fails, it returns an <b>HRESULT</b> value that indicates the error. For a list of common error codes, see <a href="https://docs.microsoft.com/windows/desktop/SecCrypto/common-hresult-values">Common HRESULT Values</a>.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nn-certenroll-ipolicyqualifier">IPolicyQualifier</a>



<a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nn-certenroll-ipolicyqualifiers">IPolicyQualifiers</a>
 

 

