---
UID: NN:tuner.ILanguageComponentType
title: ILanguageComponentType (tuner.h)
description: The ILanguageComponentType interface is implemented on LanguageComponentType objects. It provides methods that define the language of the stream content. Not all streams have a language component.
helpviewer_keywords: ["ILanguageComponentType","ILanguageComponentType interface [Microsoft TV Technologies]","ILanguageComponentType interface [Microsoft TV Technologies]","described","ILanguageComponentTypeInterface","mstv.ilanguagecomponenttype","tuner/ILanguageComponentType"]
old-location: mstv\ilanguagecomponenttype.htm
tech.root: mstv
ms.assetid: 775b5e8d-d9ed-4371-a651-bfeed6fa0ad5
ms.date: 12/05/2018
ms.keywords: ILanguageComponentType, ILanguageComponentType interface [Microsoft TV Technologies], ILanguageComponentType interface [Microsoft TV Technologies],described, ILanguageComponentTypeInterface, mstv.ilanguagecomponenttype, tuner/ILanguageComponentType
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
 - ILanguageComponentType
 - tuner/ILanguageComponentType
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
 - ILanguageComponentType
---

# ILanguageComponentType interface


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

The <b>ILanguageComponentType</b> interface is implemented on <a href="/previous-versions/windows/desktop/mstv/languagecomponenttype-object">LanguageComponentType</a> objects. It provides methods that define the language of the stream content. Not all streams have a language component.

## -inheritance

The <b>ILanguageComponentType</b> interface inherits from <a href="/previous-versions/windows/desktop/api/tuner/nn-tuner-icomponenttype">IComponentType</a>. <b>ILanguageComponentType</b> also has these types of members:
<ul>
<li><a href="/">Methods</a></li>
</ul>

## -remarks

To declare the interface identifier (IID) for this interface, use the <b>__uuidof</b> operator: <code>__uuidof(ILanguageComponentType)</code>.

## -see-also

<a href="/previous-versions/windows/desktop/api/tuner/nn-tuner-icomponenttype">IComponentType</a>



<a href="/previous-versions/windows/desktop/mstv/tuning-model-interfaces">Tuning Model Interfaces</a>
