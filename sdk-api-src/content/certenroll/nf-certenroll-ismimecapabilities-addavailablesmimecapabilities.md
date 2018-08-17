---
UID: NF:certenroll.ISmimeCapabilities.AddAvailableSmimeCapabilities
title: ISmimeCapabilities::AddAvailableSmimeCapabilities
author: windows-sdk-content
description: Adds ISmimeCapability objects to the collection by identifying the encryption algorithms supported by the default RSA cryptographic provider.
old-location: security\ismimecapabilities_addavailablesmimecapabilities_method.htm
old-project: seccertenroll
ms.assetid: b3b087e7-9934-4d29-a516-db5bba824774
ms.author: windowssdkdev
ms.date: 07/30/2018
ms.keywords: AddAvailableSmimeCapabilities, AddAvailableSmimeCapabilities method [Security], AddAvailableSmimeCapabilities method [Security],ISmimeCapabilities interface, ISmimeCapabilities interface [Security],AddAvailableSmimeCapabilities method, ISmimeCapabilities.AddAvailableSmimeCapabilities, ISmimeCapabilities::AddAvailableSmimeCapabilities, certenroll/ISmimeCapabilities::AddAvailableSmimeCapabilities, security.ismimecapabilities_addavailablesmimecapabilities_method
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
 - ISmimeCapabilities.AddAvailableSmimeCapabilities
product: Windows
targetos: Windows
req.lib: 
req.dll: CertEnroll.dll
req.irql: 
---

# ISmimeCapabilities::AddAvailableSmimeCapabilities


## -description


The <b>AddAvailableSmimeCapabilities</b> method adds <a href="https://msdn.microsoft.com/en-us/library/Aa377045(v=VS.85).aspx">ISmimeCapability</a> objects to the collection by identifying the encryption algorithms supported by the default RSA cryptographic provider.


## -parameters




### -param MachineContext [in]

A <b>VARIANT_BOOL</b> variable that identifies the certificate store context. Specify <b>VARIANT_TRUE</b> for the computer and <b>VARIANT_FALSE</b> for the user.


## -returns



If the function succeeds, the function returns <b>S_OK</b>.

If the function fails, it returns an <b>HRESULT</b> value that indicates the error. For a list of common error codes, see <a href="https://msdn.microsoft.com/en-us/library/Aa378137(v=VS.85).aspx">Common HRESULT Values</a>.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Aa376841(v=VS.85).aspx">ISmimeCapabilities</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa377045(v=VS.85).aspx">ISmimeCapability</a>
 

 

