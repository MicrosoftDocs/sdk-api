---
UID: NF:tuner.IComponent.put_Status
title: IComponent::put_Status (tuner.h)
description: The put_Status method sets the requested or actual status of the component.
helpviewer_keywords: ["IComponent interface [Microsoft TV Technologies]","put_Status method","IComponent.put_Status","IComponent::put_Status","IComponentput_Status","mstv.icomponent_put_status","put_Status","put_Status method [Microsoft TV Technologies]","put_Status method [Microsoft TV Technologies]","IComponent interface","tuner/IComponent::put_Status"]
old-location: mstv\icomponent_put_status.htm
tech.root: mstv
ms.assetid: f1f9cf98-69fd-4c54-8023-742f86413220
ms.date: 12/05/2018
ms.keywords: IComponent interface [Microsoft TV Technologies],put_Status method, IComponent.put_Status, IComponent::put_Status, IComponentput_Status, mstv.icomponent_put_status, put_Status, put_Status method [Microsoft TV Technologies], put_Status method [Microsoft TV Technologies],IComponent interface, tuner/IComponent::put_Status
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
 - IComponent::put_Status
 - tuner/IComponent::put_Status
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
 - IComponent.put_Status
---

# IComponent::put_Status


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

The <b>put_Status</b> method sets the requested or actual status of the component.

## -parameters

### -param Status [in]

A variable of type <a href="/previous-versions/windows/desktop/mstv/componentstatus">ComponentStatus</a> that specifies the status value.

## -returns

Returns S_OK if successful. If the method fails, error information can be retrieved using the standard COM <b>IErrorInfo</b> interface.

## -remarks

Use this method to activate or inactivate a stream component.

## -see-also

<a href="/previous-versions/windows/desktop/api/tuner/nn-tuner-icomponent">IComponent Interface</a>



<a href="/previous-versions/windows/desktop/api/tuner/nf-tuner-icomponent-get_status">IComponent::get_Status</a>