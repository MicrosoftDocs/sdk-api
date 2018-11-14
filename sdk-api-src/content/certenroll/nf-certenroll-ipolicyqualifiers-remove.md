---
UID: NF:certenroll.IPolicyQualifiers.Remove
title: IPolicyQualifiers::Remove
author: windows-sdk-content
description: Removes an object from the collection by index value.
old-location: security\ipolicyqualifiers_remove_method.htm
tech.root: SecCertEnroll
ms.assetid: 6071dbc2-210d-42e2-8431-68eef1e89e24
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: IPolicyQualifiers interface [Security],Remove method, IPolicyQualifiers.Remove, IPolicyQualifiers::Remove, Remove, Remove method [Security], Remove method [Security],IPolicyQualifiers interface, certenroll/IPolicyQualifiers::Remove, security.ipolicyqualifiers_remove_method
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
 - IPolicyQualifiers.Remove
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
- IPolicyQualifiers.Remove
: 
---

# IPolicyQualifiers::Remove


## -description


The <b>Remove</b> method removes an object from the collection by index value.


## -parameters




### -param Index [in]

A <b>LONG</b> variable that contains the index of the object to remove.


## -returns



If the function succeeds, the function returns <b>S_OK</b>.

If the function fails, it returns an <b>HRESULT</b> value that indicates the error. For a list of common error codes, see <a href="https://msdn.microsoft.com/en-us/library/Aa378137(v=VS.85).aspx">Common HRESULT Values</a>.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Aa376803(v=VS.85).aspx">IPolicyQualifier</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa376804(v=VS.85).aspx">IPolicyQualifiers</a>
 

 

