---
UID: NN:tuner.ILanguageComponentType
title: ILanguageComponentType (tuner.h)
description: The ILanguageComponentType interface is implemented on LanguageComponentType objects. It provides methods that define the language of the stream content. Not all streams have a language component.
old-location: mstv\ilanguagecomponenttype.htm
tech.root: mstv
ms.assetid: 775b5e8d-d9ed-4371-a651-bfeed6fa0ad5
ms.date: 12/05/2018
ms.keywords: ILanguageComponentType, ILanguageComponentType interface [Microsoft TV Technologies], ILanguageComponentType interface [Microsoft TV Technologies],described, ILanguageComponentTypeInterface, mstv.ilanguagecomponenttype, tuner/ILanguageComponentType
f1_keywords:
- tuner/ILanguageComponentType
dev_langs:
- c++
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
- ILanguageComponentType
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ILanguageComponentType interface


## -description



The <b>ILanguageComponentType</b> interface is implemented on <a href="https://docs.microsoft.com/previous-versions/windows/desktop/mstv/languagecomponenttype-object">LanguageComponentType</a> objects. It provides methods that define the language of the stream content. Not all streams have a language component.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ILanguageComponentType</b> interface inherits from <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/tuner/nn-tuner-icomponenttype">IComponentType</a>. <b>ILanguageComponentType</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ILanguageComponentType</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/tuner/nf-tuner-ilanguagecomponenttype-get_langid">get_LangID</a>
</td>
<td align="left" width="63%">
Retrieves the language of the stream content.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/tuner/nf-tuner-ilanguagecomponenttype-put_langid">put_LangID</a>
</td>
<td align="left" width="63%">
Sets the language of the stream content.

</td>
</tr>
</table> 


## -remarks



To declare the interface identifier (IID) for this interface, use the <b>__uuidof</b> operator: <code>__uuidof(ILanguageComponentType)</code>.




## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/tuner/nn-tuner-icomponenttype">IComponentType</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/mstv/tuning-model-interfaces">Tuning Model Interfaces</a>
 

 

