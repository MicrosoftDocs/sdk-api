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

# WintrustSetDefaultIncludePEPageHashes function


## -description


The <b>WintrustSetDefaultIncludePEPageHashes</b> function sets the default setting that determines whether page hashes are included when creating subject interface package (SIP) indirect data for PE files.

This setting is only used if neither the <b>SPC_EXC_PE_PAGE_HASHES_FLAG</b> or the <b>SPC_INC_PE_PAGE_HASHES_FLAG</b> flag is specified in the <i>dwFlags</i> parameter of the <a href="https://msdn.microsoft.com/9921ffae-2299-4bf2-b76d-77f7f6afb663">SignerSignEx</a> function.

 This function has no associated import library. You must use the <a href="https://msdn.microsoft.com/d936b4dd-058c-48e1-834b-b47ef6d8ef65">LoadLibrary</a> and <a href="https://msdn.microsoft.com/a0d7fc09-f888-4f46-a571-d3719a627597">GetProcAddress</a> functions to dynamically link to Wintrust.dll.


## -parameters




### -param fIncludePEPageHashes [in]

Determines whether page hashes are included when creating SIP indirect data for PE files. If this parameter is nonzero, page hashes are included. If this parameter is zero, page hashes are not included. The value is zero by default.


## -returns



This function does not return a value.




## -remarks



This setting applies to each instance of Wintrust.dll.




## -see-also




<a href="https://msdn.microsoft.com/9921ffae-2299-4bf2-b76d-77f7f6afb663">SignerSignEx</a>
 

 

