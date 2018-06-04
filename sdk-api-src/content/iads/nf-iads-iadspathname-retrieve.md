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

# IADsPathname::Retrieve


## -description


The <b>IADsPathname::Retrieve</b> method retrieves the path of the object with different format types.


## -parameters




### -param lnFormatType [in]

Specifies the format that the path should be retrieved in. This can be one of the values specified in the <a href="https://msdn.microsoft.com/d0c94f30-6b8c-4c7a-bb74-205b2b658dbb">ADS_FORMAT_ENUM</a> enumeration.


### -param pbstrADsPath [out]

Contains a pointer to a <b>BSTR</b> value the receives the object path. The caller must free this memory with the <a href="8f230ee3-5f6e-4cb9-a910-9c90b754dcd3">SysFreeString</a> function when it is no longer required.


## -returns



This method supports the standard return values, as well as the following.

For more information and other return values, see  <a href="https://msdn.microsoft.com/573889e4-37af-4aca-afd7-ef06bcf8aa0d">ADSI Error Codes</a>.




## -see-also




<a href="https://msdn.microsoft.com/573889e4-37af-4aca-afd7-ef06bcf8aa0d">ADSI Error Codes</a>



<a href="https://msdn.microsoft.com/d0c94f30-6b8c-4c7a-bb74-205b2b658dbb">ADS_FORMAT_ENUM</a>



<a href="https://msdn.microsoft.com/9aa26d6c-aa86-4a23-a986-b8cb9057772a">IADsPathname</a>



<a href="8f230ee3-5f6e-4cb9-a910-9c90b754dcd3">SysFreeString</a>
 

 

