---
UID: NF:certenroll.IPolicyQualifiers.Add
title: IPolicyQualifiers::Add
author: windows-sdk-content
description: Adds an object to the collection.
old-location: security\ipolicyqualifiers_add_method.htm
old-project: SecCertEnroll
ms.assetid: 41ead360-0b11-4e47-86c5-24e636cc589d
ms.author: windowssdkdev
ms.date: 05/10/2018
ms.keywords: Add, Add method [Security], Add method [Security],IPolicyQualifiers interface, IPolicyQualifiers interface [Security],Add method, IPolicyQualifiers.Add, IPolicyQualifiers::Add, certenroll/IPolicyQualifiers::Add, security.ipolicyqualifiers_add_method
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
 - IPolicyQualifiers.Add
product: Windows
targetos: Windows
req.lib: 
req.dll: CertEnroll.dll
req.irql: 
---

# IPolicyQualifiers::Add


## -description


The <b>Add</b> method adds an object to the collection.


## -parameters




### -param pVal [in]

Pointer to the <a href="https://msdn.microsoft.com/3804e372-17bb-458d-8da5-85d760fe5e60">IPolicyQualifier</a> interface to add.


## -returns



If the function succeeds, the function returns <b>S_OK</b>.

If the function fails, it returns an <b>HRESULT</b> value that indicates the error. For a list of common error codes, see <a href="https://msdn.microsoft.com/ce52efc3-92c7-40e4-ac49-0c54049e169f">Common HRESULT Values</a>.




## -see-also




<a href="https://msdn.microsoft.com/3804e372-17bb-458d-8da5-85d760fe5e60">IPolicyQualifier</a>



<a href="https://msdn.microsoft.com/da8b6289-379e-4dff-b15a-b0967f245c3d">IPolicyQualifiers</a>
 

 

