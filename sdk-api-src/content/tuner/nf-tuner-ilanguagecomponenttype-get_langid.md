---
UID: NF:tuner.ILanguageComponentType.get_LangID
title: ILanguageComponentType::get_LangID
author: windows-sdk-content
description: The get_LangID method retrieves the LCID that identifies the language.
old-location: mstv\ilanguagecomponenttype_get_langid.htm
tech.root: mstv
ms.assetid: f70dcc70-701a-4465-ad40-1ddc5e697f46
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: ILanguageComponentType interface [Microsoft TV Technologies],get_LangID method, ILanguageComponentType.get_LangID, ILanguageComponentType::get_LangID, ILanguageComponentTypeget_LangID, get_LangID, get_LangID method [Microsoft TV Technologies], get_LangID method [Microsoft TV Technologies],ILanguageComponentType interface, mstv.ilanguagecomponenttype_get_langid, tuner/ILanguageComponentType::get_LangID
ms.topic: method
req.header: tuner.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: None supported
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Tuner.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - tuner.h
api_name:
 - ILanguageComponentType.get_LangID
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ILanguageComponentType::get_LangID


## -description



The <b>get_LangID</b> method retrieves the LCID that identifies the language.




## -parameters




### -param LangID [out]

Pointer to a variable that receives the LCID.


## -returns



Returns S_OK if successful. If the method fails, error information can be retrieved using the standard COM <b>IErrorInfo</b> interface.




## -remarks



The <i>pLangID</i> parameter is a pointer to a Win32 LCID. Use this method to determine the language of an audio stream. Use the <a href="https://msdn.microsoft.com/1c041173-0c78-486e-93b5-a46c9dc0afb1">IComponent::get_DescLangID</a> to determine the language of the text description of the stream.




## -see-also




<a href="https://msdn.microsoft.com/775b5e8d-d9ed-4371-a651-bfeed6fa0ad5">ILanguageComponentType Interface</a>



<a href="https://msdn.microsoft.com/c0dc0141-a839-4fdc-9313-24ddd3eaf63d">ILanguageComponentType::put_LangID</a>
 

 

