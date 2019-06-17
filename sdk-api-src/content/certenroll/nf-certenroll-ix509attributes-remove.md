---
UID: NF:certenroll.IX509Attributes.Remove
title: IX509Attributes::Remove (certenroll.h)
author: windows-sdk-content
description: Removes an IX509Attribute object from the collection by index number.
old-location: security\ix509attributes_remove_method.htm
tech.root: seccertenroll
ms.assetid: 5821f4bd-5165-4ffc-8d1c-5ef89188b307
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IX509Attributes interface [Security],Remove method, IX509Attributes.Remove, IX509Attributes::Remove, Remove, Remove method [Security], Remove method [Security],IX509Attributes interface, certenroll/IX509Attributes::Remove, security.ix509attributes_remove_method
ms.topic: method
f1_keywords: ["certenroll/IX509Attributes.Remove"]
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
 - IX509Attributes.Remove
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IX509Attributes::Remove


## -description


The <b>Remove</b> method removes an <a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nn-certenroll-ix509attribute">IX509Attribute</a> object from the collection by index number.


## -parameters




### -param Index [in]

A <b>LONG</b> variable that contains the index of the object to remove.


## -returns



If the function succeeds, the function returns <b>S_OK</b>.

If the function fails, it returns an <b>HRESULT</b> value that indicates the error. For a list of common error codes, see <a href="https://docs.microsoft.com/windows/desktop/SecCrypto/common-hresult-values">Common HRESULT Values</a>.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nn-certenroll-ix509attribute">IX509Attribute</a>



<a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nn-certenroll-ix509attributeextensions">IX509AttributeExtensions</a>



<a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nn-certenroll-ix509attributes">IX509Attributes</a>
 

 

