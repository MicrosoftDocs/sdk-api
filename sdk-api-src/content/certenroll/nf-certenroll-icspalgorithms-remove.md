---
UID: NF:certenroll.ICspAlgorithms.Remove
title: ICspAlgorithms::Remove
author: windows-sdk-content
description: Removes an ICspAlgorithm object from the collection by index number.
old-location: security\icspalgorithms_remove_method.htm
old-project: SecCertEnroll
ms.assetid: 9116ca78-3b99-4b9a-97af-d01077e201f7
ms.author: windowssdkdev
ms.date: 05/10/2018
ms.keywords: ICspAlgorithms interface [Security],Remove method, ICspAlgorithms.Remove, ICspAlgorithms::Remove, Remove, Remove method [Security], Remove method [Security],ICspAlgorithms interface, certenroll/ICspAlgorithms::Remove, security.icspalgorithms_remove_method
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
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - CertEnroll.dll
api_name:
 - ICspAlgorithms.Remove
product: Windows
targetos: Windows
req.lib: 
req.dll: CertEnroll.dll
req.irql: 
---

# ICspAlgorithms::Remove


## -description


The <b>Remove</b> method removes an <a href="https://msdn.microsoft.com/e3b87c45-44c2-4fc6-ac75-0bf125f3c4b3">ICspAlgorithm</a> object from the collection by index number.


## -parameters




### -param Index [in]

A <b>LONG</b> variable that contains the index of the object to remove.


## -returns



If the function succeeds, the function returns <b>S_OK</b>.

If the function fails, it returns an <b>HRESULT</b> value that indicates the error. For a list of common error codes, see <a href="https://msdn.microsoft.com/ce52efc3-92c7-40e4-ac49-0c54049e169f">Common HRESULT Values</a>.




## -see-also




<a href="https://msdn.microsoft.com/e3b87c45-44c2-4fc6-ac75-0bf125f3c4b3">ICspAlgorithm</a>



<a href="https://msdn.microsoft.com/bbf8cff4-b1b2-480e-8c30-eb34166db143">ICspAlgorithms</a>
 

 

