---
UID: NF:certenroll.IX509NameValuePair.Initialize
title: IX509NameValuePair::Initialize
author: windows-sdk-content
description: Initializes the object from strings that contain the name and associated value.
old-location: security\ix509namevaluepair_initialize_method.htm
tech.root: seccertenroll
ms.assetid: 3e935718-a59a-443e-bff2-a010a41e7756
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IX509NameValuePair interface [Security],Initialize method, IX509NameValuePair.Initialize, IX509NameValuePair::Initialize, Initialize, Initialize method [Security], Initialize method [Security],IX509NameValuePair interface, certenroll/IX509NameValuePair::Initialize, security.ix509namevaluepair_initialize_method
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
 - IX509NameValuePair.Initialize
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
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

If the function fails, it returns an <b>HRESULT</b> value that indicates the error. For a list of common error codes, see <a href="https://msdn.microsoft.com/en-us/library/Aa378137(v=VS.85).aspx">Common HRESULT Values</a>.




## -remarks



You can call the <a href="https://msdn.microsoft.com/en-us/library/Aa378904(v=VS.85).aspx">Name</a> and <a href="https://msdn.microsoft.com/en-us/library/Aa378913(v=VS.85).aspx">Value</a> properties to retrieve the values initialized by calling this method.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Aa378525(v=VS.85).aspx">IX509NameValuePair</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa378904(v=VS.85).aspx">Name</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa378913(v=VS.85).aspx">Value</a>
 

 

