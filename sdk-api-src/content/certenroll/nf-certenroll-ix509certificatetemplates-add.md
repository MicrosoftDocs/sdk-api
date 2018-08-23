---
UID: NF:certenroll.IX509CertificateTemplates.Add
title: IX509CertificateTemplates::Add
author: windows-sdk-content
description: Adds an IX509CertificateTemplate object to the collection.
old-location: security\ix509certificatetemplates_add.htm
old-project: seccertenroll
ms.assetid: c52186bc-af51-4369-8ff5-6122d2e80450
ms.author: windowssdkdev
ms.date: 07/30/2018
ms.keywords: Add, Add method [Security], Add method [Security],IX509CertificateTemplates interface, IX509CertificateTemplates interface [Security],Add method, IX509CertificateTemplates.Add, IX509CertificateTemplates::Add, certenroll/IX509CertificateTemplates::Add, security.ix509certificatetemplates_add
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: certenroll.h
req.include-header: 
req.redist: 
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
tech.root: 
req.typenames: X509RequestType
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Certenroll.h
api_name:
 - IX509CertificateTemplates.Add
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# IX509CertificateTemplates::Add


## -description


The <b>Add</b> method adds an <a href="https://msdn.microsoft.com/56122d92-7e38-4eaa-b2f5-713adc81e68e">IX509CertificateTemplate</a> object to the collection.  This method is web enabled.


## -parameters




### -param pVal [in]

Pointer to an <a href="https://msdn.microsoft.com/56122d92-7e38-4eaa-b2f5-713adc81e68e">IX509CertificateTemplate</a> object to add to the collection.


## -returns



If the function succeeds, the function returns <b>S_OK</b>.

If the function fails, it returns an <b>HRESULT</b> value that indicates the error. For a list of common error codes, see <a href="https://msdn.microsoft.com/ce52efc3-92c7-40e4-ac49-0c54049e169f">Common HRESULT Values</a>.




## -see-also




<a href="https://msdn.microsoft.com/56122d92-7e38-4eaa-b2f5-713adc81e68e">IX509CertificateTemplate</a>



<a href="https://msdn.microsoft.com/82d14b93-e07b-4ff3-88b9-b1873972b4ad">IX509CertificateTemplates</a>
 

 

