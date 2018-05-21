---
UID: NF:certenroll.IX509CertificateTemplates.Remove
title: IX509CertificateTemplates::Remove
author: windows-driver-content
description: Removes an IX509CertificateTemplate object from the collection by index number.
old-location: security\ix509certificatetemplates_remove.htm
old-project: SecCertEnroll
ms.assetid: e30aaeab-4130-40ab-9b50-32a119fdb794
ms.author: windowsdriverdev
ms.date: 5/10/2018
ms.keywords: IX509CertificateTemplates interface [Security],Remove method, IX509CertificateTemplates.Remove, IX509CertificateTemplates::Remove, Remove, Remove method [Security], Remove method [Security],IX509CertificateTemplates interface, certenroll/IX509CertificateTemplates::Remove, security.ix509certificatetemplates_remove
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: certenroll.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Certenroll.idl
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
-	Certenroll.h
api_name:
-	IX509CertificateTemplates.Remove
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# IX509CertificateTemplates::Remove


## -description


The <b>Remove</b> method removes an <a href="https://msdn.microsoft.com/56122d92-7e38-4eaa-b2f5-713adc81e68e">IX509CertificateTemplate</a> object from the collection by index number.


## -parameters




### -param Index [in]

A <b>LONG</b> variable that contains the index of the object to remove.


## -returns



If the function succeeds, the function returns <b>S_OK</b>.

If the function fails, it returns an <b>HRESULT</b> value that indicates the error. For a list of common error codes, see <a href="https://msdn.microsoft.com/ce52efc3-92c7-40e4-ac49-0c54049e169f">Common HRESULT Values</a>.




## -see-also




<a href="https://msdn.microsoft.com/82d14b93-e07b-4ff3-88b9-b1873972b4ad">IX509CertificateTemplates</a>
 

 

