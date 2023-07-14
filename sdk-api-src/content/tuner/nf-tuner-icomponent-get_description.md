---
UID: NF:tuner.IComponent.get_Description
title: IComponent::get_Description (tuner.h)
description: The get_Description method retrieves the description of the component.
helpviewer_keywords: ["IComponent interface [Microsoft TV Technologies]","get_Description method","IComponent.get_Description","IComponent::get_Description","IComponentget_Description","get_Description","get_Description method [Microsoft TV Technologies]","get_Description method [Microsoft TV Technologies]","IComponent interface","mstv.icomponent_get_description","tuner/IComponent::get_Description"]
old-location: mstv\icomponent_get_description.htm
tech.root: mstv
ms.assetid: ef7d1308-27ff-4d4d-b88d-58a9f89abc7f
ms.date: 12/05/2018
ms.keywords: IComponent interface [Microsoft TV Technologies],get_Description method, IComponent.get_Description, IComponent::get_Description, IComponentget_Description, get_Description, get_Description method [Microsoft TV Technologies], get_Description method [Microsoft TV Technologies],IComponent interface, mstv.icomponent_get_description, tuner/IComponent::get_Description
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
 - IComponent::get_Description
 - tuner/IComponent::get_Description
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
 - IComponent.get_Description
---

# IComponent::get_Description


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

The <b>get_Description</b> method retrieves the description of the component.

## -parameters

### -param Description [out]

Pointer to a variable that receives the description.

## -returns

Returns S_OK if successful. If the method fails, error information can be retrieved using the standard COM <b>IErrorInfo</b> interface.

## -remarks

The caller must release the returned <b>BSTR</b> by calling <b>SysFreeString</b>.

## -see-also

<a href="/previous-versions/windows/desktop/api/tuner/nn-tuner-icomponent">IComponent Interface</a>