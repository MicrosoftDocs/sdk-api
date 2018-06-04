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

# IWMStreamConfig3::GetLanguage


## -description



The <b>GetLanguage</b> method retrieves the RFC1766-compliant language string for the stream.




## -parameters




### -param pwszLanguageString [out]

Pointer to a wide-character <b>null</b>-terminated string containing the language string. Pass <b>NULL</b> to retrieve the size of the string, which is returned in <i>pcchLanguageStringLength</i>.


### -param pcchLanguageStringLength [in, out]

Pointer to a <b>WORD</b> containing the size of the language string in wide characters. This size includes the terminating <b>null</b> character.


## -returns



If the method succeeds, it returns S_OK. If it fails, it returns an <b>HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/c79ddfb8-b1ff-475c-8c9d-01e0dbe3f681">IWMStreamConfig3 Interface</a>



<a href="https://msdn.microsoft.com/3d5c65b1-5e8b-4ee7-b28c-a35376c91ac4">IWMStreamConfig3::SetLanguage</a>
 

 

