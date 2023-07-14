---
UID: NF:tuner.IComponent.put_Type
title: IComponent::put_Type (tuner.h)
description: The put_Type method sets an IComponentType object describing the general characteristics of the component.
helpviewer_keywords: ["IComponent interface [Microsoft TV Technologies]","put_Type method","IComponent.put_Type","IComponent::put_Type","IComponentput_Type","mstv.icomponent_put_type","put_Type","put_Type method [Microsoft TV Technologies]","put_Type method [Microsoft TV Technologies]","IComponent interface","tuner/IComponent::put_Type"]
old-location: mstv\icomponent_put_type.htm
tech.root: mstv
ms.assetid: 07d8cc28-d34e-4332-8648-d69a471ca8ac
ms.date: 12/05/2018
ms.keywords: IComponent interface [Microsoft TV Technologies],put_Type method, IComponent.put_Type, IComponent::put_Type, IComponentput_Type, mstv.icomponent_put_type, put_Type, put_Type method [Microsoft TV Technologies], put_Type method [Microsoft TV Technologies],IComponent interface, tuner/IComponent::put_Type
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
 - IComponent::put_Type
 - tuner/IComponent::put_Type
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
 - IComponent.put_Type
---

# IComponent::put_Type


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

The <b>put_Type</b> method sets an <a href="/previous-versions/windows/desktop/api/tuner/nn-tuner-icomponenttype">IComponentType</a> object describing the general characteristics of the component.

## -parameters

### -param CT [in]

Pointer to an <a href="/previous-versions/windows/desktop/api/tuner/nn-tuner-icomponenttype">IComponentType</a> object that specifies the new values for the component.

## -returns

Returns S_OK if successful. If the method fails, error information can be retrieved using the standard COM <b>IErrorInfo</b> interface.

## -remarks

Using the <a href="/previous-versions/windows/desktop/api/tuner/nn-tuner-icomponent">IComponent</a> base class interface, it is possible to set the type to be <b>NULL</b>. If you try to do this with the derived <a href="/previous-versions/windows/desktop/api/tuner/nn-tuner-impeg2component">IMPEG2Component</a> class interface, this method will return E_POINTER. The <b>IMPEG2Component</b> object cannot have the base <a href="/previous-versions/windows/desktop/api/tuner/nn-tuner-icomponenttype">IComponentType</a> class interface as the set type - this will return Type Mismatch (0x80020005).

## -see-also

<a href="/previous-versions/windows/desktop/api/tuner/nn-tuner-icomponent">IComponent Interface</a>