---
UID: NF:certenroll.IX509NameValuePairs.Add
title: IX509NameValuePairs::Add
author: windows-sdk-content
description: Adds an IX509NameValuePair object to the collection.
old-location: security\ix509namevaluepairs_add_method.htm
tech.root: SecCertEnroll
ms.assetid: 2b5592d4-4f3b-4cea-8c59-15529cc53efa
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: Add, Add method [Security], Add method [Security],IX509NameValuePairs interface, IX509NameValuePairs interface [Security],Add method, IX509NameValuePairs.Add, IX509NameValuePairs::Add, certenroll/IX509NameValuePairs::Add, security.ix509namevaluepairs_add_method
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
 - IX509NameValuePairs.Add
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IX509NameValuePairs::Add


## -description


The <b>Add</b> method adds an <a href="https://msdn.microsoft.com/e3b87c45-44c2-4fc6-ac75-0bf125f3c4b3">IX509NameValuePair</a> object to the collection.


## -parameters




### -param pVal [in]

A pointer to an <a href="https://msdn.microsoft.com/e3b87c45-44c2-4fc6-ac75-0bf125f3c4b3">IX509NameValuePair</a> interface that represents the name-value pair to add.


## -returns



If the function succeeds, the function returns <b>S_OK</b>.

If the function fails, it returns an <b>HRESULT</b> value that indicates the error. For a list of common error codes, see <a href="https://msdn.microsoft.com/ce52efc3-92c7-40e4-ac49-0c54049e169f">Common HRESULT Values</a>.




## -see-also




<a href="https://msdn.microsoft.com/e3b87c45-44c2-4fc6-ac75-0bf125f3c4b3">IX509NameValuePair</a>



<a href="https://msdn.microsoft.com/c881dc9f-4187-4ba1-9f3a-e1564e4f37c7">IX509NameValuePairs</a>
 

 

