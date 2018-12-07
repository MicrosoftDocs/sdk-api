---
UID: NF:certenroll.ICertProperties.Remove
title: ICertProperties::Remove
author: windows-sdk-content
description: Removes a property from the collection by index value.
old-location: security\icertproperties_remove_method.htm
tech.root: seccertenroll
ms.assetid: 7ee9e624-6f27-4177-9711-7062cb10f77b
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: ICertProperties interface [Security],Remove method, ICertProperties.Remove, ICertProperties::Remove, Remove, Remove method [Security], Remove method [Security],ICertProperties interface, certenroll/ICertProperties::Remove, security.icertproperties_remove_method
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
 - ICertProperties.Remove
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ICertProperties::Remove


## -description


The <b>Remove</b> method removes a property from the collection by index value.


## -parameters




### -param Index [in]

A <b>LONG</b> variable that contains the index of the property to remove.


## -returns



If the function succeeds, the function returns <b>S_OK</b>.

If the function fails, it returns an <b>HRESULT</b> value that indicates the error. For a list of common error codes, see <a href="https://msdn.microsoft.com/en-us/library/Aa378137(v=VS.85).aspx">Common HRESULT Values</a>.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Aa375231(v=VS.85).aspx">ICertProperties</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa375239(v=VS.85).aspx">ICertProperty</a>
 

 

