---
UID: NF:certenroll.IX509Extensions.Remove
title: IX509Extensions::Remove
author: windows-sdk-content
description: Removes an IX509Extension object from the collection by index number.
old-location: security\ix509extensions_remove_method.htm
old-project: SecCertEnroll
ms.assetid: da1fcad3-7351-4d26-b483-a6548c3bdbec
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: IX509Extensions interface [Security],Remove method, IX509Extensions.Remove, IX509Extensions::Remove, Remove, Remove method [Security], Remove method [Security],IX509Extensions interface, certenroll/IX509Extensions::Remove, security.ix509extensions_remove_method
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: certenroll.h
req.include-header: 
req.redist: 
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
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - CertEnroll.dll
api_name:
 - IX509Extensions.Remove
product: Windows
targetos: Windows
req.lib: 
req.dll: CertEnroll.dll
req.irql: 
---

# IX509Extensions::Remove


## -description


The <b>Remove</b> method removes an <a href="https://msdn.microsoft.com/f04e3f63-c826-4401-a1c8-b2614e0dc374">IX509Extension</a> object from the collection by index number.


## -parameters




### -param Index [in]

A <b>LONG</b> variable that contains the index of the object to remove.


## -returns



If the function succeeds, the function returns <b>S_OK</b>.

If the function fails, it returns an <b>HRESULT</b> value that indicates the error. For a list of common error codes, see <a href="https://msdn.microsoft.com/ce52efc3-92c7-40e4-ac49-0c54049e169f">Common HRESULT Values</a>.




## -see-also




<a href="https://msdn.microsoft.com/f04e3f63-c826-4401-a1c8-b2614e0dc374">IX509Extension</a>



<a href="https://msdn.microsoft.com/d6bdbcff-1d6b-4813-8269-b75061a42de8">IX509Extensions</a>
 

 

