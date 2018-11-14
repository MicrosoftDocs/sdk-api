---
UID: NF:certenroll.ISmimeCapabilities.Add
title: ISmimeCapabilities::Add
author: windows-sdk-content
description: Adds an ISmimeCapability object to the collection.
old-location: security\ismimecapabilities_add_method.htm
tech.root: SecCertEnroll
ms.assetid: 8ad35758-0dc1-4887-aea7-b8ead537cab2
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: Add, Add method [Security], Add method [Security],ISmimeCapabilities interface, ISmimeCapabilities interface [Security],Add method, ISmimeCapabilities.Add, ISmimeCapabilities::Add, certenroll/ISmimeCapabilities::Add, security.ismimecapabilities_add_method
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
 - ISmimeCapabilities.Add
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
- ISmimeCapabilities.Add
: 
---

# ISmimeCapabilities::Add


## -description


The <b>Add</b> method adds an <a href="https://msdn.microsoft.com/en-us/library/Aa377045(v=VS.85).aspx">ISmimeCapability</a> object to the collection.


## -parameters




### -param pVal [in]

Pointer to the <a href="https://msdn.microsoft.com/en-us/library/Aa377045(v=VS.85).aspx">ISmimeCapability</a> interface to add.


## -returns



If the function succeeds, the function returns <b>S_OK</b>.

If the function fails, it returns an <b>HRESULT</b> value that indicates the error. For a list of common error codes, see <a href="https://msdn.microsoft.com/en-us/library/Aa378137(v=VS.85).aspx">Common HRESULT Values</a>.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Aa376841(v=VS.85).aspx">ISmimeCapabilities</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa377045(v=VS.85).aspx">ISmimeCapability</a>
 

 

