---
UID: NF:certenroll.IX509NameValuePair.Initialize
title: IX509NameValuePair::Initialize
author: windows-sdk-content
description: Initializes the object from strings that contain the name and associated value.
old-location: security\ix509namevaluepair_initialize_method.htm
old-project: SecCertEnroll
ms.assetid: 3e935718-a59a-443e-bff2-a010a41e7756
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: IX509NameValuePair interface [Security],Initialize method, IX509NameValuePair.Initialize, IX509NameValuePair::Initialize, Initialize, Initialize method [Security], Initialize method [Security],IX509NameValuePair interface, certenroll/IX509NameValuePair::Initialize, security.ix509namevaluepair_initialize_method
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
 - IX509NameValuePair.Initialize
product: Windows
targetos: Windows
req.lib: 
req.dll: CertEnroll.dll
req.irql: 
---

# IX509NameValuePair::Initialize


## -description


The <b>Initialize</b> method initializes the object from strings that contain the  name and associated value.


## -parameters




### -param strName [in]

A <b>BSTR</b> variable that contains the name.


### -param strValue [in]

A <b>BSTR</b> variable that contains the value.


## -returns



If the function succeeds, the function returns <b>S_OK</b>.

If the function fails, it returns an <b>HRESULT</b> value that indicates the error. For a list of common error codes, see <a href="https://msdn.microsoft.com/ce52efc3-92c7-40e4-ac49-0c54049e169f">Common HRESULT Values</a>.




## -remarks



You can call the <a href="https://msdn.microsoft.com/2a124fe7-7f28-4911-b5fe-2c98b4187723">Name</a> and <a href="https://msdn.microsoft.com/769eb16b-68c7-4540-bd1d-d04585ba0dfd">Value</a> properties to retrieve the values initialized by calling this method.




## -see-also




<a href="https://msdn.microsoft.com/e3b87c45-44c2-4fc6-ac75-0bf125f3c4b3">IX509NameValuePair</a>



<a href="https://msdn.microsoft.com/2a124fe7-7f28-4911-b5fe-2c98b4187723">Name</a>



<a href="https://msdn.microsoft.com/769eb16b-68c7-4540-bd1d-d04585ba0dfd">Value</a>
 

 

