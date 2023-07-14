---
UID: NF:tuner.IComponent.put_DescLangID
title: IComponent::put_DescLangID (tuner.h)
description: The put_DescLangID method sets the language for presentation of the description.
helpviewer_keywords: ["IComponent interface [Microsoft TV Technologies]","put_DescLangID method","IComponent.put_DescLangID","IComponent::put_DescLangID","IComponentput_DescLangID","mstv.icomponent_put_desclangid","put_DescLangID","put_DescLangID method [Microsoft TV Technologies]","put_DescLangID method [Microsoft TV Technologies]","IComponent interface","tuner/IComponent::put_DescLangID"]
old-location: mstv\icomponent_put_desclangid.htm
tech.root: mstv
ms.assetid: 0f914835-e097-4a02-80fe-371154c9d95a
ms.date: 12/05/2018
ms.keywords: IComponent interface [Microsoft TV Technologies],put_DescLangID method, IComponent.put_DescLangID, IComponent::put_DescLangID, IComponentput_DescLangID, mstv.icomponent_put_desclangid, put_DescLangID, put_DescLangID method [Microsoft TV Technologies], put_DescLangID method [Microsoft TV Technologies],IComponent interface, tuner/IComponent::put_DescLangID
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
 - IComponent::put_DescLangID
 - tuner/IComponent::put_DescLangID
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
 - IComponent.put_DescLangID
---

# IComponent::put_DescLangID


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

The <b>put_DescLangID</b> method sets the language for presentation of the description.

## -parameters

### -param LangID [in]

Specifies the language ID.

## -returns

Returns S_OK if successful. If the method fails, error information can be retrieved using the standard COM <b>IErrorInfo</b> interface.

## -remarks

This is the language of the descriptive info in the component object. It is not the same as the language ID in the language component type which defines the language of the stream content. An application can modify this value in order to activate a different language substream.

## -see-also

<a href="/previous-versions/windows/desktop/api/tuner/nn-tuner-icomponent">IComponent Interface</a>