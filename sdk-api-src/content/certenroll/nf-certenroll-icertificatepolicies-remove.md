---
UID: NF:certenroll.ICertificatePolicies.Remove
title: ICertificatePolicies::Remove (certenroll.h)
author: windows-sdk-content
description: Removes an object from the collection by index number.
old-location: security\icertificatepolicies_remove_method.htm
tech.root: seccertenroll
ms.assetid: 5cd010bb-50ee-4251-815e-1fb4de1f2a81
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: ICertificatePolicies interface [Security],Remove method, ICertificatePolicies.Remove, ICertificatePolicies::Remove, Remove, Remove method [Security], Remove method [Security],ICertificatePolicies interface, certenroll/ICertificatePolicies::Remove, security.icertificatepolicies_remove_method
ms.topic: method
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
 - ICertificatePolicies.Remove
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ICertificatePolicies::Remove


## -description


The <b>Remove</b> method removes an object from the collection by index number.


## -parameters




### -param Index [in]

A <b>LONG</b> variable that contains the index of the object to remove.


## -returns



If the function succeeds, the function returns <b>S_OK</b>.

If the function fails, it returns an <b>HRESULT</b> value that indicates the error. For a list of common error codes, see <a href="https://docs.microsoft.com/windows/desktop/SecCrypto/common-hresult-values">Common HRESULT Values</a>.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nn-certenroll-icertificatepolicies">ICertificatePolicies</a>



<a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nn-certenroll-icertificatepolicy">ICertificatePolicy</a>
 

 

