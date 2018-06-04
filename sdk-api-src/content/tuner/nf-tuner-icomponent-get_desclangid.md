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

# IComponent::get_DescLangID


## -description



The <b>get_DescLangID</b> method retrieves the language identifier for the description property.




## -parameters




### -param LangID






#### - pLangID [out]

Receives the language identifier.


## -returns



Returns S_OK if successful. If the method fails, error information can be retrieved using the standard COM <b>IErrorInfo</b> interface.




## -remarks



The returned language identifer identifies the language of the description property, which is obtained by calling the <b>get_Description</b> method.

To get the language of the stream content, call the <a href="https://msdn.microsoft.com/f70dcc70-701a-4465-ad40-1ddc5e697f46">ILanguageComponentType::get_LangID</a> method (only if the component object exposes the <a href="https://msdn.microsoft.com/775b5e8d-d9ed-4371-a651-bfeed6fa0ad5">ILanguageComponentType</a> interface).




## -see-also




<a href="https://msdn.microsoft.com/516b30ba-4f55-49b7-8085-d436bf4a94e1">IComponent Interface</a>



<a href="https://msdn.microsoft.com/ef7d1308-27ff-4d4d-b88d-58a9f89abc7f">IComponent::get_Description</a>
 

 

