---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# IMDSPDevice2::GetCanonicalName


## -description



The <b>GetCanonicalPName</b> method gets the canonical name of a device.




## -parameters




### -param pwszPnPName [out]

A wide character, null-terminated buffer holding the canonical name. The caller allocates and releases this buffer.


### -param nMaxChars [in]

Integer containing the maximum number of characters that can be placed in <i>pwszCanonicalName</i>, including the termination character.


## -returns



The method returns an <b>HRESULT</b>. Possible values include, but are not limited to, those in the following table.




## -remarks



This method returns a canonical name for the device. The service provider should return the device path name of the device as its canonical name. The service provider is passed the device path name in the <b>CreateDevice</b> method on the <a href="https://msdn.microsoft.com/d9ffaea8-5616-4bc2-a27c-8b77ea177b6b">IMDServiceProvider2</a> interface.

This is optional. For more information, see <a href="https://msdn.microsoft.com/582c9dd5-f8ab-48df-afb3-fba931ee0dea">Mandatory and Optional Interfaces</a>.




## -see-also




<a href="https://msdn.microsoft.com/a53052a1-89f4-4571-9eee-031e0049a92e">IMDSPDevice2 Interface</a>



<a href="https://msdn.microsoft.com/d9ffaea8-5616-4bc2-a27c-8b77ea177b6b">IMDServiceProvider2 Interface</a>



<a href="https://msdn.microsoft.com/f724ef14-c572-41ca-a56b-fde85d7620e0">IMDServiceProvider2::CreateDevice</a>
 

 

