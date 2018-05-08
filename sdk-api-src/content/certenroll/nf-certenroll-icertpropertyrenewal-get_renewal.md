---
UID: NF:certenroll.ICertPropertyRenewal.get_Renewal
title: ICertPropertyRenewal::get_Renewal
author: windows-driver-content
description: Retrieves the SHA-1 hash of the new certificate.
old-location: security\icertpropertyrenewal_renewal_property.htm
old-project: SecCertEnroll
ms.assetid: f2ea8198-01ec-4485-9f7e-9b9fa8ddba6f
ms.author: windowsdriverdev
ms.date: 4/5/2018
ms.keywords: ICertPropertyRenewal interface [Security],Renewal property, ICertPropertyRenewal.Renewal, ICertPropertyRenewal.get_Renewal, ICertPropertyRenewal::Renewal, ICertPropertyRenewal::get_Renewal, Renewal property [Security], Renewal property [Security],ICertPropertyRenewal interface, certenroll/ICertPropertyRenewal::Renewal, certenroll/ICertPropertyRenewal::get_Renewal, get_Renewal, security.icertpropertyrenewal_renewal_property
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.typenames: X509RequestType
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	CertEnroll.dll
api_name:
-	ICertPropertyRenewal.Renewal
-	ICertPropertyRenewal.get_Renewal
product: Windows
targetos: Windows
req.lib: 
req.dll: CertEnroll.dll
req.irql: 
---

# ICertPropertyRenewal::get_Renewal


## -description


The <b>Renewal</b> property retrieves the SHA-1 hash of the new certificate. The hash is returned in a byte array , and the byte array is represented by a Unicode encoded string.

This property is read-only.


## -parameters


## -remarks



Call the <a href="https://msdn.microsoft.com/library/windows/hardware/ff550945">Initialize</a> method or the <a href="https://msdn.microsoft.com/87e0eabf-7a4a-4ff2-a9ce-6482f119cafd">InitializeFromCertificateHash</a> method to specify a value for the <b>Renewal</b> property.




## -see-also




<a href="https://msdn.microsoft.com/c87a391a-aec9-4b42-8084-c593ecbb0bc6">ICertPropertyRenewal</a>
 

 

