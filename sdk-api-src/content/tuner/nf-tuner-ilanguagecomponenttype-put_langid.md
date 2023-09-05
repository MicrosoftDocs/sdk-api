---
UID: NF:tuner.ILanguageComponentType.put_LangID
title: ILanguageComponentType::put_LangID (tuner.h)
description: The put_LangID method specifies the LCID that identifies the language.
helpviewer_keywords: ["ILanguageComponentType interface [Microsoft TV Technologies]","put_LangID method","ILanguageComponentType.put_LangID","ILanguageComponentType::put_LangID","ILanguageComponentTypeput_LangID","mstv.ilanguagecomponenttype_put_langid","put_LangID","put_LangID method [Microsoft TV Technologies]","put_LangID method [Microsoft TV Technologies]","ILanguageComponentType interface","tuner/ILanguageComponentType::put_LangID"]
old-location: mstv\ilanguagecomponenttype_put_langid.htm
tech.root: mstv
ms.assetid: c0dc0141-a839-4fdc-9313-24ddd3eaf63d
ms.date: 12/05/2018
ms.keywords: ILanguageComponentType interface [Microsoft TV Technologies],put_LangID method, ILanguageComponentType.put_LangID, ILanguageComponentType::put_LangID, ILanguageComponentTypeput_LangID, mstv.ilanguagecomponenttype_put_langid, put_LangID, put_LangID method [Microsoft TV Technologies], put_LangID method [Microsoft TV Technologies],ILanguageComponentType interface, tuner/ILanguageComponentType::put_LangID
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
 - ILanguageComponentType::put_LangID
 - tuner/ILanguageComponentType::put_LangID
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
 - ILanguageComponentType.put_LangID
---

# ILanguageComponentType::put_LangID


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

The <b>put_LangID</b> method specifies the LCID that identifies the language

## -parameters

### -param LangID [in]

Specifies the LCID.

## -returns

Returns S_OK if successful. If the method fails, error information can be retrieved using the standard COM <b>IErrorInfo</b> interface.

## -remarks

The <i>LangID</i> parameter is a Win32 LCID. Use this method to set the language of an audio stream, for example when creating a new entry for the Guide Store database. Use the <a href="/previous-versions/windows/desktop/api/tuner/nf-tuner-icomponent-put_desclangid">IComponent::put_DescLangID</a> method to specify the language of the text description of the stream.

## -see-also

<a href="/previous-versions/windows/desktop/api/tuner/nn-tuner-ilanguagecomponenttype">ILanguageComponentType Interface</a>



<a href="/previous-versions/windows/desktop/api/tuner/nf-tuner-ilanguagecomponenttype-get_langid">ILanguageComponentType::get_LangID</a>