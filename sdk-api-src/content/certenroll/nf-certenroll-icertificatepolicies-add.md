---
UID: NF:certenroll.ICertificatePolicies.Add
title: ICertificatePolicies::Add
author: windows-sdk-content
description: Adds an object to the collection.
old-location: security\icertificatepolicies_add_method.htm
tech.root: SecCertEnroll
ms.assetid: 85dc750c-ef18-4136-962e-c95bcca05b9a
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: Add, Add method [Security], Add method [Security],ICertificatePolicies interface, ICertificatePolicies interface [Security],Add method, ICertificatePolicies.Add, ICertificatePolicies::Add, certenroll/ICertificatePolicies::Add, security.icertificatepolicies_add_method
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
 - ICertificatePolicies.Add
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ICertificatePolicies::Add


## -description


The <b>Add</b> method adds an object to the collection.


## -parameters




### -param pVal [in]

Pointer to the <a href="https://msdn.microsoft.com/2162de70-edcc-4f01-807d-79ff200d0016">ICertificatePolicy</a> interface to add.


## -returns



If the function succeeds, the function returns <b>S_OK</b>.

If the function fails, it returns an <b>HRESULT</b> value that indicates the error. For a list of common error codes, see <a href="https://msdn.microsoft.com/ce52efc3-92c7-40e4-ac49-0c54049e169f">Common HRESULT Values</a>.




## -see-also




<a href="https://msdn.microsoft.com/2503adcb-0b73-42ef-98cf-a2b906e34ef7">ICertificatePolicies</a>



<a href="https://msdn.microsoft.com/2162de70-edcc-4f01-807d-79ff200d0016">ICertificatePolicy</a>
 

 

