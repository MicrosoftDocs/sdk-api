---
UID: NF:tuner.ILanguageComponentType.put_LangID
title: ILanguageComponentType::put_LangID
author: windows-sdk-content
description: The put_LangID method specifies the LCID that identifies the language.
old-location: mstv\ilanguagecomponenttype_put_langid.htm
tech.root: mstv
ms.assetid: c0dc0141-a839-4fdc-9313-24ddd3eaf63d
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: ILanguageComponentType interface [Microsoft TV Technologies],put_LangID method, ILanguageComponentType.put_LangID, ILanguageComponentType::put_LangID, ILanguageComponentTypeput_LangID, mstv.ilanguagecomponenttype_put_langid, put_LangID, put_LangID method [Microsoft TV Technologies], put_LangID method [Microsoft TV Technologies],ILanguageComponentType interface, tuner/ILanguageComponentType::put_LangID
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - ILanguageComponentType.put_LangID
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ILanguageComponentType::put_LangID


## -description



The <b>put_LangID</b> method specifies the LCID that identifies the language




## -parameters




### -param LangID [in]

Specifies the LCID.


## -returns



Returns S_OK if successful. If the method fails, error information can be retrieved using the standard COM <b>IErrorInfo</b> interface.




## -remarks



The <i>LangID</i> parameter is a Win32 LCID. Use this method to set the language of an audio stream, for example when creating a new entry for the Guide Store database. Use the <a href="https://msdn.microsoft.com/0f914835-e097-4a02-80fe-371154c9d95a">IComponent::put_DescLangID</a> method to specify the language of the text description of the stream.




## -see-also




<a href="https://msdn.microsoft.com/775b5e8d-d9ed-4371-a651-bfeed6fa0ad5">ILanguageComponentType Interface</a>



<a href="https://msdn.microsoft.com/f70dcc70-701a-4465-ad40-1ddc5e697f46">ILanguageComponentType::get_LangID</a>
 

 

