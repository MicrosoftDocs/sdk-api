---
UID: NF:certenroll.ISignerCertificates.Find
title: ISignerCertificates::Find (certenroll.h)
author: windows-sdk-content
description: Retrieves the index number of an ISignerCertificate object.
old-location: security\isignercertificates_find_method.htm
tech.root: seccertenroll
ms.assetid: ee741eda-e125-4938-bc49-d8089f7d5df2
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: Find, Find method [Security], Find method [Security],ISignerCertificates interface, ISignerCertificates interface [Security],Find method, ISignerCertificates.Find, ISignerCertificates::Find, certenroll/ISignerCertificates::Find, security.isignercertificates_find_method
ms.topic: method
f1_keywords: 
 - "certenroll/ISignerCertificates.Find"
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
 - ISignerCertificates.Find
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ISignerCertificates::Find


## -description


The <b>Find</b> method retrieves the index number of an <a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nn-certenroll-isignercertificate">ISignerCertificate</a> object.


## -parameters




### -param pSignerCert [in]

Pointer to the <a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nn-certenroll-isignercertificate">ISignerCertificate</a> interface.


### -param piSignerCert [out]

Pointer to a <b>LONG</b> variable that receives the index number.


## -returns



If the function succeeds, the function returns <b>S_OK</b>.

If the function fails, it returns an <b>HRESULT</b> value that indicates the error. For a list of common error codes, see <a href="https://docs.microsoft.com/windows/desktop/SecCrypto/common-hresult-values">Common HRESULT Values</a>.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nn-certenroll-isignercertificate">ISignerCertificate</a>



<a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nn-certenroll-isignercertificates">ISignerCertificates</a>
 

 

