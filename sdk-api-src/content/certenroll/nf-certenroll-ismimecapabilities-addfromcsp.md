---
UID: NF:certenroll.ISmimeCapabilities.AddFromCsp
title: ISmimeCapabilities::AddFromCsp
author: windows-sdk-content
description: Adds objects to the collection by identifying the encryption algorithms supported by a specific cryptographic provider.
old-location: security\ismimecapabilities_addfromcsp_method.htm
old-project: seccertenroll
ms.assetid: a4244a4e-6ec3-4c1f-a0d6-607cc942b5f5
ms.author: windowssdkdev
ms.date: 07/30/2018
ms.keywords: AddFromCsp, AddFromCsp method [Security], AddFromCsp method [Security],ISmimeCapabilities interface, ISmimeCapabilities interface [Security],AddFromCsp method, ISmimeCapabilities.AddFromCsp, ISmimeCapabilities::AddFromCsp, certenroll/ISmimeCapabilities::AddFromCsp, security.ismimecapabilities_addfromcsp_method
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
 - ISmimeCapabilities.AddFromCsp
product: Windows
targetos: Windows
req.lib: 
req.dll: CertEnroll.dll
req.irql: 
---

# ISmimeCapabilities::AddFromCsp


## -description


The <b>AddFromCsp</b> method adds objects to the collection by identifying the encryption algorithms supported by a specific cryptographic provider.


## -parameters




### -param pValue [in]

Pointer to an <a href="https://msdn.microsoft.com/en-us/library/Aa375967(v=VS.85).aspx">ICspInformation</a> interface that represents the provider. 


## -returns



If the function succeeds, the function returns <b>S_OK</b>.

If the function fails, it returns an <b>HRESULT</b> value that indicates the error. For a list of common error codes, see <a href="https://msdn.microsoft.com/en-us/library/Aa378137(v=VS.85).aspx">Common HRESULT Values</a>.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Aa376841(v=VS.85).aspx">ISmimeCapabilities</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa377045(v=VS.85).aspx">ISmimeCapability</a>
 

 

