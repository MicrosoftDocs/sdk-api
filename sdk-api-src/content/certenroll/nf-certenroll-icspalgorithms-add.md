---
UID: NF:certenroll.ICspAlgorithms.Add
title: ICspAlgorithms::Add
author: windows-sdk-content
description: Adds an ICspAlgorithm object to the collection.
old-location: security\icspalgorithms_add_method.htm
old-project: seccertenroll
ms.assetid: 53cd408e-752c-4256-839c-e09055487c39
ms.author: windowssdkdev
ms.date: 07/30/2018
ms.keywords: Add, Add method [Security], Add method [Security],ICspAlgorithms interface, ICspAlgorithms interface [Security],Add method, ICspAlgorithms.Add, ICspAlgorithms::Add, certenroll/ICspAlgorithms::Add, security.icspalgorithms_add_method
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
 - ICspAlgorithms.Add
product: Windows
targetos: Windows
req.lib: 
req.dll: CertEnroll.dll
req.irql: 
---

# ICspAlgorithms::Add


## -description


The <b>Add</b> method adds an <a href="https://msdn.microsoft.com/e3b87c45-44c2-4fc6-ac75-0bf125f3c4b3">ICspAlgorithm</a> object to the collection. This method is web enabled.


## -parameters




### -param pVal [in]

Pointer to an <a href="https://msdn.microsoft.com/e3b87c45-44c2-4fc6-ac75-0bf125f3c4b3">ICspAlgorithm</a> interface to add.


## -returns



If the function succeeds, the function returns <b>S_OK</b>.

If the function fails, it returns an <b>HRESULT</b> value that indicates the error. For a list of common error codes, see <a href="https://msdn.microsoft.com/ce52efc3-92c7-40e4-ac49-0c54049e169f">Common HRESULT Values</a>.




## -see-also




<a href="https://msdn.microsoft.com/e3b87c45-44c2-4fc6-ac75-0bf125f3c4b3">ICspAlgorithm</a>



<a href="https://msdn.microsoft.com/bbf8cff4-b1b2-480e-8c30-eb34166db143">ICspAlgorithms</a>
 

 

