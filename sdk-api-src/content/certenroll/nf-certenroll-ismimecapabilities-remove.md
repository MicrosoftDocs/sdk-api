---
UID: NF:certenroll.ISmimeCapabilities.Remove
title: ISmimeCapabilities::Remove
author: windows-sdk-content
description: Removes an object from the collection by index value.
old-location: security\ismimecapabilities_remove_method.htm
old-project: seccertenroll
ms.assetid: 516726cc-f7b9-4813-999f-036694322fe5
ms.author: windowssdkdev
ms.date: 07/30/2018
ms.keywords: ISmimeCapabilities interface [Security],Remove method, ISmimeCapabilities.Remove, ISmimeCapabilities::Remove, Remove, Remove method [Security], Remove method [Security],ISmimeCapabilities interface, certenroll/ISmimeCapabilities::Remove, security.ismimecapabilities_remove_method
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
 - ISmimeCapabilities.Remove
product: Windows
targetos: Windows
req.lib: 
req.dll: CertEnroll.dll
req.irql: 
---

# ISmimeCapabilities::Remove


## -description


The <b>Remove</b> method removes an object from the collection by index value.


## -parameters




### -param Index [in]

A <b>LONG</b> variable that contains the index of the object to remove.


## -returns



If the function succeeds, the function returns <b>S_OK</b>.

If the function fails, it returns an <b>HRESULT</b> value that indicates the error. For a list of common error codes, see <a href="https://msdn.microsoft.com/ce52efc3-92c7-40e4-ac49-0c54049e169f">Common HRESULT Values</a>.




## -see-also




<a href="https://msdn.microsoft.com/f9750b68-9d35-4594-96fc-2fbd54a87dcc">ISmimeCapabilities</a>



<a href="https://msdn.microsoft.com/3cfbb16f-88fa-41f1-b719-cd5e8ad636cc">ISmimeCapability</a>
 

 

