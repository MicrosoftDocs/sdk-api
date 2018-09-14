---
UID: NF:certenroll.ISmimeCapabilities.AddFromCsp
title: ISmimeCapabilities::AddFromCsp
author: windows-sdk-content
description: Adds objects to the collection by identifying the encryption algorithms supported by a specific cryptographic provider.
old-location: security\ismimecapabilities_addfromcsp_method.htm
tech.root: seccertenroll
ms.assetid: a4244a4e-6ec3-4c1f-a0d6-607cc942b5f5
ms.author: windowssdkdev
ms.date: 08/31/2018
ms.keywords: AddFromCsp, AddFromCsp method [Security], AddFromCsp method [Security],ISmimeCapabilities interface, ISmimeCapabilities interface [Security],AddFromCsp method, ISmimeCapabilities.AddFromCsp, ISmimeCapabilities::AddFromCsp, certenroll/ISmimeCapabilities::AddFromCsp, security.ismimecapabilities_addfromcsp_method
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
 - ISmimeCapabilities.AddFromCsp
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ISmimeCapabilities::AddFromCsp


## -description


The <b>AddFromCsp</b> method adds objects to the collection by identifying the encryption algorithms supported by a specific cryptographic provider.


## -parameters




### -param pValue [in]

Pointer to an <a href="https://msdn.microsoft.com/e337ae2c-6f86-4025-8d31-47bc5d8a4ca8">ICspInformation</a> interface that represents the provider. 


## -returns



If the function succeeds, the function returns <b>S_OK</b>.

If the function fails, it returns an <b>HRESULT</b> value that indicates the error. For a list of common error codes, see <a href="https://msdn.microsoft.com/ce52efc3-92c7-40e4-ac49-0c54049e169f">Common HRESULT Values</a>.




## -see-also




<a href="https://msdn.microsoft.com/f9750b68-9d35-4594-96fc-2fbd54a87dcc">ISmimeCapabilities</a>



<a href="https://msdn.microsoft.com/3cfbb16f-88fa-41f1-b719-cd5e8ad636cc">ISmimeCapability</a>
 

 

