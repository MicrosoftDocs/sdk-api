---
UID: NF:tuner.ILanguageComponentType.get_LangID
title: ILanguageComponentType::get_LangID (tuner.h)
description: The get_LangID method retrieves the LCID that identifies the language.
helpviewer_keywords: ["ILanguageComponentType interface [Microsoft TV Technologies]","get_LangID method","ILanguageComponentType.get_LangID","ILanguageComponentType::get_LangID","ILanguageComponentTypeget_LangID","get_LangID","get_LangID method [Microsoft TV Technologies]","get_LangID method [Microsoft TV Technologies]","ILanguageComponentType interface","mstv.ilanguagecomponenttype_get_langid","tuner/ILanguageComponentType::get_LangID"]
old-location: mstv\ilanguagecomponenttype_get_langid.htm
tech.root: mstv
ms.assetid: f70dcc70-701a-4465-ad40-1ddc5e697f46
ms.date: 12/05/2018
ms.keywords: ILanguageComponentType interface [Microsoft TV Technologies],get_LangID method, ILanguageComponentType.get_LangID, ILanguageComponentType::get_LangID, ILanguageComponentTypeget_LangID, get_LangID, get_LangID method [Microsoft TV Technologies], get_LangID method [Microsoft TV Technologies],ILanguageComponentType interface, mstv.ilanguagecomponenttype_get_langid, tuner/ILanguageComponentType::get_LangID
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ILanguageComponentType::get_LangID
 - tuner/ILanguageComponentType::get_LangID
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - tuner.h
api_name:
 - ILanguageComponentType.get_LangID
---

# ILanguageComponentType::get_LangID


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

The <b>get_LangID</b> method retrieves the LCID that identifies the language.

## -parameters

### -param LangID [out]

Pointer to a variable that receives the LCID.

## -returns

Returns S_OK if successful. If the method fails, error information can be retrieved using the standard COM <b>IErrorInfo</b> interface.

## -remarks

The <i>pLangID</i> parameter is a pointer to a Win32 LCID. Use this method to determine the language of an audio stream. Use the <a href="/previous-versions/windows/desktop/api/tuner/nf-tuner-icomponent-get_desclangid">IComponent::get_DescLangID</a> to determine the language of the text description of the stream.

## -see-also

<a href="/previous-versions/windows/desktop/api/tuner/nn-tuner-ilanguagecomponenttype">ILanguageComponentType Interface</a>



<a href="/previous-versions/windows/desktop/api/tuner/nf-tuner-ilanguagecomponenttype-put_langid">ILanguageComponentType::put_LangID</a>