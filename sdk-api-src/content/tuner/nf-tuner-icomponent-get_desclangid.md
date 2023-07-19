---
UID: NF:tuner.IComponent.get_DescLangID
title: IComponent::get_DescLangID (tuner.h)
description: The get_DescLangID method retrieves the language identifier for the description property.
helpviewer_keywords: ["IComponent interface [Microsoft TV Technologies]","get_DescLangID method","IComponent.get_DescLangID","IComponent::get_DescLangID","IComponentget_DescLangID","get_DescLangID","get_DescLangID method [Microsoft TV Technologies]","get_DescLangID method [Microsoft TV Technologies]","IComponent interface","mstv.icomponent_get_desclangid","tuner/IComponent::get_DescLangID"]
old-location: mstv\icomponent_get_desclangid.htm
tech.root: mstv
ms.assetid: 1c041173-0c78-486e-93b5-a46c9dc0afb1
ms.date: 12/05/2018
ms.keywords: IComponent interface [Microsoft TV Technologies],get_DescLangID method, IComponent.get_DescLangID, IComponent::get_DescLangID, IComponentget_DescLangID, get_DescLangID, get_DescLangID method [Microsoft TV Technologies], get_DescLangID method [Microsoft TV Technologies],IComponent interface, mstv.icomponent_get_desclangid, tuner/IComponent::get_DescLangID
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
 - IComponent::get_DescLangID
 - tuner/IComponent::get_DescLangID
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
 - IComponent.get_DescLangID
---

# IComponent::get_DescLangID


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

The <b>get_DescLangID</b> method retrieves the language identifier for the description property.

## -parameters

### -param LangID [out]

Receives the language identifier.

## -returns

Returns S_OK if successful. If the method fails, error information can be retrieved using the standard COM <b>IErrorInfo</b> interface.

## -remarks

The returned language identifier identifies the language of the description property, which is obtained by calling the <b>get_Description</b> method.

To get the language of the stream content, call the <a href="/previous-versions/windows/desktop/api/tuner/nf-tuner-ilanguagecomponenttype-get_langid">ILanguageComponentType::get_LangID</a> method (only if the component object exposes the <a href="/previous-versions/windows/desktop/api/tuner/nn-tuner-ilanguagecomponenttype">ILanguageComponentType</a> interface).

## -see-also

<a href="/previous-versions/windows/desktop/api/tuner/nn-tuner-icomponent">IComponent Interface</a>



<a href="/previous-versions/windows/desktop/api/tuner/nf-tuner-icomponent-get_description">IComponent::get_Description</a>