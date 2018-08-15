---
UID: NF:certenroll.ICertProperties.Remove
title: ICertProperties::Remove
author: windows-sdk-content
description: Removes a property from the collection by index value.
old-location: security\icertproperties_remove_method.htm
old-project: seccertenroll
ms.assetid: 7ee9e624-6f27-4177-9711-7062cb10f77b
ms.author: windowssdkdev
ms.date: 07/30/2018
ms.keywords: ICertProperties interface [Security],Remove method, ICertProperties.Remove, ICertProperties::Remove, Remove, Remove method [Security], Remove method [Security],ICertProperties interface, certenroll/ICertProperties::Remove, security.icertproperties_remove_method
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
 - ICertProperties.Remove
product: Windows
targetos: Windows
req.lib: 
req.dll: CertEnroll.dll
req.irql: 
---

# ICertProperties::Remove


## -description


The <b>Remove</b> method removes a property from the collection by index value.


## -parameters




### -param Index [in]

A <b>LONG</b> variable that contains the index of the property to remove.


## -returns



If the function succeeds, the function returns <b>S_OK</b>.

If the function fails, it returns an <b>HRESULT</b> value that indicates the error. For a list of common error codes, see <a href="https://msdn.microsoft.com/ce52efc3-92c7-40e4-ac49-0c54049e169f">Common HRESULT Values</a>.




## -see-also




<a href="https://msdn.microsoft.com/b830c0af-0a38-419d-8a33-8e3626c4e8f1">ICertProperties</a>



<a href="https://msdn.microsoft.com/947c2f09-993d-4ced-8b76-66b79d96e3bc">ICertProperty</a>
 

 

