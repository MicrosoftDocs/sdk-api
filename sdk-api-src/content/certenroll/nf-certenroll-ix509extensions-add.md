---
UID: NF:certenroll.IX509Extensions.Add
title: IX509Extensions::Add
author: windows-sdk-content
description: Adds an IX509Extension object to the collection.
old-location: security\ix509extensions_add_method.htm
tech.root: SecCertEnroll
ms.assetid: 08109828-44d9-4b8f-a57c-bbedfc82fbbb
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: Add, Add method [Security], Add method [Security],IX509Extensions interface, IX509Extensions interface [Security],Add method, IX509Extensions.Add, IX509Extensions::Add, certenroll/IX509Extensions::Add, security.ix509extensions_add_method
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
 - IX509Extensions.Add
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- certenroll.h
: 
- IX509Extensions.Add
: 
---

# IX509Extensions::Add


## -description


The <b>Add</b> method adds an <a href="https://msdn.microsoft.com/en-us/library/Aa378077(v=VS.85).aspx">IX509Extension</a> object to the collection. This method is web enabled.


## -parameters




### -param pVal [in]

Pointer to an <a href="https://msdn.microsoft.com/en-us/library/Aa378077(v=VS.85).aspx">IX509Extension</a> object to add to the collection.


## -returns



If the function succeeds, the function returns <b>S_OK</b>.

If the function fails, it returns an <b>HRESULT</b> value that indicates the error. For a list of common error codes, see <a href="https://msdn.microsoft.com/en-us/library/Aa378137(v=VS.85).aspx">Common HRESULT Values</a>.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Aa378077(v=VS.85).aspx">IX509Extension</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa378174(v=VS.85).aspx">IX509Extensions</a>
 

 

