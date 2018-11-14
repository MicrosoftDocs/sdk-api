---
UID: NF:certenroll.IX509NameValuePairs.Remove
title: IX509NameValuePairs::Remove
author: windows-sdk-content
description: Removes an IX509NameValuePair object from the collection by index number.
old-location: security\ix509namevaluepairs_remove_method.htm
tech.root: SecCertEnroll
ms.assetid: f66dbfd1-331f-4e1b-a17e-f8071044d073
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: IX509NameValuePairs interface [Security],Remove method, IX509NameValuePairs.Remove, IX509NameValuePairs::Remove, Remove, Remove method [Security], Remove method [Security],IX509NameValuePairs interface, certenroll/IX509NameValuePairs::Remove, security.ix509namevaluepairs_remove_method
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
 - IX509NameValuePairs.Remove
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
- IX509NameValuePairs.Remove
: 
---

# IX509NameValuePairs::Remove


## -description


The <b>Remove</b> method removes an <a href="https://msdn.microsoft.com/en-us/library/Aa378525(v=VS.85).aspx">IX509NameValuePair</a> object from the collection by index number.


## -parameters




### -param Index [in]

A <b>LONG</b> variable that contains the index of the object to remove.


## -returns



If the function succeeds, the function returns <b>S_OK</b>.

If the function fails, it returns an <b>HRESULT</b> value that indicates the error. For a list of common error codes, see <a href="https://msdn.microsoft.com/en-us/library/Aa378137(v=VS.85).aspx">Common HRESULT Values</a>.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Aa378525(v=VS.85).aspx">IX509NameValuePair</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa378746(v=VS.85).aspx">IX509NameValuePairs</a>
 

 

