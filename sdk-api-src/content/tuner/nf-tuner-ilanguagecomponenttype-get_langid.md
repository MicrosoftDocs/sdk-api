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

# ILanguageComponentType::get_LangID


## -description



The <b>get_LangID</b> method retrieves the LCID that identifies the language.




## -parameters




### -param LangID






#### - pLangID [out]

Pointer to a variable that receives the LCID.


## -returns



Returns S_OK if successful. If the method fails, error information can be retrieved using the standard COM <b>IErrorInfo</b> interface.




## -remarks




          The <i>pLangID</i> parameter is a pointer to a Win32 LCID. Use this method to determine the language of an audio stream. Use the <a href="https://msdn.microsoft.com/1c041173-0c78-486e-93b5-a46c9dc0afb1">IComponent::get_DescLangID</a> to determine the language of the text description of the stream.




## -see-also




<a href="https://msdn.microsoft.com/775b5e8d-d9ed-4371-a651-bfeed6fa0ad5">ILanguageComponentType Interface</a>



<a href="https://msdn.microsoft.com/c0dc0141-a839-4fdc-9313-24ddd3eaf63d">ILanguageComponentType::put_LangID</a>
 

 

