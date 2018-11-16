---
UID: NF:certenroll.IAlternativeNames.Remove
title: IAlternativeNames::Remove
author: windows-sdk-content
description: Removes an object from the collection by index number.
old-location: security\ialternativenames_remove_method.htm
tech.root: SecCertEnroll
ms.assetid: 1507d03b-2c1d-416e-b346-16795902f5e2
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: IAlternativeNames interface [Security],Remove method, IAlternativeNames.Remove, IAlternativeNames::Remove, Remove, Remove method [Security], Remove method [Security],IAlternativeNames interface, certenroll/IAlternativeNames::Remove, security.ialternativenames_remove_method
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
 - IAlternativeNames.Remove
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
- IAlternativeNames.Remove
: 
---

# IAlternativeNames::Remove


## -description


The <b>Remove</b> method removes an object from the collection by index number.


## -parameters




### -param Index [in]

A <b>LONG</b> variable that contains the index of the object to remove.


## -returns



If the function succeeds, the function returns <b>S_OK</b>.

If the function fails, it returns an <b>HRESULT</b> value that indicates the error. For a list of common error codes, see <a href="https://msdn.microsoft.com/en-us/library/Aa378137(v=VS.85).aspx">Common HRESULT Values</a>.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Aa374981(v=VS.85).aspx">IAlternativeName</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa374984(v=VS.85).aspx">IAlternativeNames</a>
 

 

