---
UID: NF:certenroll.IAlternativeNames.Add
title: IAlternativeNames::Add method
author: windows-driver-content
description: Adds an object to the collection.
old-location: security\ialternativenames_add_method.htm
old-project: SecCertEnroll
ms.assetid: 02085a1c-0821-4b11-95ad-e1c3a69f4e80
ms.author: windowsdriverdev
ms.date: 4/5/2018
ms.keywords: Add method [Security], Add method [Security], IAlternativeNames interface, Add,IAlternativeNames.Add, IAlternativeNames, IAlternativeNames interface [Security], Add method, IAlternativeNames::Add, certenroll/IAlternativeNames::Add, security.ialternativenames_add_method
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
-	IAlternativeNames.Add
product: Windows
targetos: Windows
req.lib: 
req.dll: CertEnroll.dll
req.irql: 
---

# IAlternativeNames::Add method


## -description


The <b>Add</b> method adds an object to the collection.


## -parameters




### -param pVal [in]

Pointer to an <a href="https://msdn.microsoft.com/2a6cfda8-b3cb-4a0f-bb65-b182c16207be">IAlternativeName</a> interface to add.


## -returns



If the function succeeds, the function returns <b>S_OK</b>.

If the function fails, it returns an <b>HRESULT</b> value that indicates the error. For a list of common error codes, see <a href="https://msdn.microsoft.com/ce52efc3-92c7-40e4-ac49-0c54049e169f">Common HRESULT Values</a>.




## -see-also




<a href="https://msdn.microsoft.com/2a6cfda8-b3cb-4a0f-bb65-b182c16207be">IAlternativeName</a>



<a href="https://msdn.microsoft.com/6ebd5bd5-7bf3-43e3-9b72-47b2c9743174">IAlternativeNames</a>
 

 

