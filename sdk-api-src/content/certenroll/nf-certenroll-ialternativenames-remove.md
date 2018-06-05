---
UID: NF:certenroll.IAlternativeNames.Remove
title: IAlternativeNames::Remove
author: windows-sdk-content
description: Removes an object from the collection by index number.
old-location: security\ialternativenames_remove_method.htm
old-project: SecCertEnroll
ms.assetid: 1507d03b-2c1d-416e-b346-16795902f5e2
ms.author: windowssdkdev
ms.date: 05/10/2018
ms.keywords: IAlternativeNames interface [Security],Remove method, IAlternativeNames.Remove, IAlternativeNames::Remove, Remove, Remove method [Security], Remove method [Security],IAlternativeNames interface, certenroll/IAlternativeNames::Remove, security.ialternativenames_remove_method
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: X509RequestType
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	CertEnroll.dll
api_name:
-	IAlternativeNames.Remove
product: Windows
targetos: Windows
req.lib: 
req.dll: CertEnroll.dll
req.irql: 
---

# IAlternativeNames::Remove


## -description


The <b>Remove</b> method removes an object from the collection by index number.


## -parameters




### -param Index [in]

A <b>LONG</b> variable that contains the index of the object to remove.


## -returns



If the function succeeds, the function returns <b>S_OK</b>.

If the function fails, it returns an <b>HRESULT</b> value that indicates the error. For a list of common error codes, see <a href="https://msdn.microsoft.com/ce52efc3-92c7-40e4-ac49-0c54049e169f">Common HRESULT Values</a>.




## -see-also




<a href="https://msdn.microsoft.com/2a6cfda8-b3cb-4a0f-bb65-b182c16207be">IAlternativeName</a>



<a href="https://msdn.microsoft.com/6ebd5bd5-7bf3-43e3-9b72-47b2c9743174">IAlternativeNames</a>
 

 

