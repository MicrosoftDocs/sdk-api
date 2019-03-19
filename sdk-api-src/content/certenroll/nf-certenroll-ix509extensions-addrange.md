---
UID: NF:certenroll.IX509Extensions.AddRange
title: IX509Extensions::AddRange (certenroll.h)
author: windows-sdk-content
description: Adds a range of IX509Extension objects to the collection.
old-location: security\ix509extensions_addrange_method.htm
tech.root: seccertenroll
ms.assetid: e2e11b36-966b-497a-a199-41364314d287
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: AddRange, AddRange method [Security], AddRange method [Security],IX509Extensions interface, IX509Extensions interface [Security],AddRange method, IX509Extensions.AddRange, IX509Extensions::AddRange, certenroll/IX509Extensions::AddRange, security.ix509extensions_addrange_method
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
 - IX509Extensions.AddRange
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IX509Extensions::AddRange


## -description


The <b>AddRange</b> method adds a range of <a href="https://msdn.microsoft.com/f04e3f63-c826-4401-a1c8-b2614e0dc374">IX509Extension</a> objects to the collection.


## -parameters




### -param pValue [in]

Pointer to an <a href="https://msdn.microsoft.com/d6bdbcff-1d6b-4813-8269-b75061a42de8">IX509Extensions</a> interface that contains the collection to add.


## -returns



If the function succeeds, the function returns <b>S_OK</b>.

If the function fails, it returns an <b>HRESULT</b> value that indicates the error. For a list of common error codes, see <a href="https://msdn.microsoft.com/ce52efc3-92c7-40e4-ac49-0c54049e169f">Common HRESULT Values</a>.




## -see-also




<a href="https://msdn.microsoft.com/f04e3f63-c826-4401-a1c8-b2614e0dc374">IX509Extension</a>



<a href="https://msdn.microsoft.com/d6bdbcff-1d6b-4813-8269-b75061a42de8">IX509Extensions</a>
 

 

