---
UID: NF:tuner.IComponent.get_Type
title: IComponent::get_Type (tuner.h)
description: The get_Type method retrieves an IComponentType interface describing the general characteristics of the component.
helpviewer_keywords: ["IComponent interface [Microsoft TV Technologies]","get_Type method","IComponent.get_Type","IComponent::get_Type","IComponentget_Type","get_Type","get_Type method [Microsoft TV Technologies]","get_Type method [Microsoft TV Technologies]","IComponent interface","mstv.icomponent_get_type","tuner/IComponent::get_Type"]
old-location: mstv\icomponent_get_type.htm
tech.root: mstv
ms.assetid: 19eb345f-24a2-4522-87cc-fc4953faf343
ms.date: 12/05/2018
ms.keywords: IComponent interface [Microsoft TV Technologies],get_Type method, IComponent.get_Type, IComponent::get_Type, IComponentget_Type, get_Type, get_Type method [Microsoft TV Technologies], get_Type method [Microsoft TV Technologies],IComponent interface, mstv.icomponent_get_type, tuner/IComponent::get_Type
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
 - IComponent::get_Type
 - tuner/IComponent::get_Type
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
 - IComponent.get_Type
---

# IComponent::get_Type


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

The <b>get_Type</b> method retrieves an <a href="/previous-versions/windows/desktop/api/tuner/nn-tuner-icomponenttype">IComponentType</a> interface describing the general characteristics of the component.

## -parameters

### -param CT [out]

Address of an <a href="/previous-versions/windows/desktop/api/tuner/nn-tuner-icomponenttype">IComponentType</a> interface pointer that will be set to the retrieved component.

## -returns

Returns S_OK if successful. If the method fails, error information can be retrieved using the standard COM <b>IErrorInfo</b> interface.

## -see-also

<a href="/previous-versions/windows/desktop/api/tuner/nn-tuner-icomponent">IComponent Interface</a>