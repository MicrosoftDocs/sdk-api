---
UID: NF:tuner.ILanguageComponentType.get_LangID
title: ILanguageComponentType::get_LangID (tuner.h)
author: windows-sdk-content
description: The get_LangID method retrieves the LCID that identifies the language.
old-location: mstv\ilanguagecomponenttype_get_langid.htm
tech.root: mstv
ms.assetid: f70dcc70-701a-4465-ad40-1ddc5e697f46
ms.author: windowssdkdev
ms.date: 12/05/2018
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
ms.custom: 19H1
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



The <i>pLangID</i> parameter is a pointer to a Win32 LCID. Use this method to determine the language of an audio stream. Use the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/tuner/nf-tuner-icomponent-get_desclangid">IComponent::get_DescLangID</a> to determine the language of the text description of the stream.




## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/tuner/nn-tuner-ilanguagecomponenttype">ILanguageComponentType Interface</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/tuner/nf-tuner-ilanguagecomponenttype-put_langid">ILanguageComponentType::put_LangID</a>
 

 

