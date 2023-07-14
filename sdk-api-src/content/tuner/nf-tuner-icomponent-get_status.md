---
UID: NF:tuner.IComponent.get_Status
title: IComponent::get_Status (tuner.h)
description: The get_Status method retrieves the requested or actual status of the component.
helpviewer_keywords: ["IComponent interface [Microsoft TV Technologies]","get_Status method","IComponent.get_Status","IComponent::get_Status","IComponentget_Status","get_Status","get_Status method [Microsoft TV Technologies]","get_Status method [Microsoft TV Technologies]","IComponent interface","mstv.icomponent_get_status","tuner/IComponent::get_Status"]
old-location: mstv\icomponent_get_status.htm
tech.root: mstv
ms.assetid: 3f517db8-a207-472e-8c6c-7cb2cac91f62
ms.date: 12/05/2018
ms.keywords: IComponent interface [Microsoft TV Technologies],get_Status method, IComponent.get_Status, IComponent::get_Status, IComponentget_Status, get_Status, get_Status method [Microsoft TV Technologies], get_Status method [Microsoft TV Technologies],IComponent interface, mstv.icomponent_get_status, tuner/IComponent::get_Status
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
 - IComponent::get_Status
 - tuner/IComponent::get_Status
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
 - IComponent.get_Status
---

# IComponent::get_Status


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

The <b>get_Status</b> method retrieves the requested or actual status of the component.

## -parameters

### -param Status [out]

Pointer to a <a href="/previous-versions/windows/desktop/mstv/componentstatus">ComponentStatus</a> enumeration that receives the status value.

## -returns

Returns S_OK if successful. If the method fails, error information can be retrieved using the standard COM <b>IErrorInfo</b> interface.

## -remarks

When the TIF adds a component to the <a href="/previous-versions/windows/desktop/api/tuner/nn-tuner-icomponents">IComponents</a> collection, it can indicate whether the component is active or not. An application can attempt to set this status, and resubmit a tune request. The tuner will update the status from the enumeration: Active, Inactive, Unavailable. The Unavailable status is only set by a tuner in response to a request to activate, when the component is not really available.

## -see-also

<a href="/previous-versions/windows/desktop/api/tuner/nn-tuner-icomponent">IComponent Interface</a>