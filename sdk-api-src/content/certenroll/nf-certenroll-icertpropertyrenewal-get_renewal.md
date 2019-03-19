---
UID: NF:certenroll.ICertPropertyRenewal.get_Renewal
title: ICertPropertyRenewal::get_Renewal (certenroll.h)
author: windows-sdk-content
description: Retrieves the SHA-1 hash of the new certificate.
old-location: security\icertpropertyrenewal_renewal_property.htm
tech.root: seccertenroll
ms.assetid: f2ea8198-01ec-4485-9f7e-9b9fa8ddba6f
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: ICertPropertyRenewal interface [Security],Renewal property, ICertPropertyRenewal.Renewal, ICertPropertyRenewal.get_Renewal, ICertPropertyRenewal::Renewal, ICertPropertyRenewal::get_Renewal, Renewal property [Security], Renewal property [Security],ICertPropertyRenewal interface, certenroll/ICertPropertyRenewal::Renewal, certenroll/ICertPropertyRenewal::get_Renewal, get_Renewal, security.icertpropertyrenewal_renewal_property
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
 - ICertPropertyRenewal.Renewal
 - ICertPropertyRenewal.get_Renewal
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ICertPropertyRenewal::get_Renewal


## -description


The <b>Renewal</b> property retrieves the SHA-1 hash of the new certificate. The hash is returned in a byte array , and the byte array is represented by a Unicode encoded string.

This property is read-only.


## -parameters


## -remarks



Call the <a href="https://msdn.microsoft.com/dc1e124e-400a-4f1e-8e87-095b6a3341d4">Initialize</a> method or the <a href="https://msdn.microsoft.com/87e0eabf-7a4a-4ff2-a9ce-6482f119cafd">InitializeFromCertificateHash</a> method to specify a value for the <b>Renewal</b> property.




## -see-also




<a href="https://msdn.microsoft.com/c87a391a-aec9-4b42-8084-c593ecbb0bc6">ICertPropertyRenewal</a>
 

 

