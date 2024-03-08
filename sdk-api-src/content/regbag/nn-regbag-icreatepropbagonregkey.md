---
UID: NN:regbag.ICreatePropBagOnRegKey
title: ICreatePropBagOnRegKey (regbag.h)
description: The ICreatePropBagOnRegKey interface creates a property bag that can store information in the system registry.Use this interface to store the default tune request in the registry.
helpviewer_keywords: ["ICreatePropBagOnRegKey","ICreatePropBagOnRegKey interface [Microsoft TV Technologies]","ICreatePropBagOnRegKey interface [Microsoft TV Technologies]","described","ICreatePropBagOnRegKeyInterface","mstv.icreatepropbagonregkey","regbag/ICreatePropBagOnRegKey"]
old-location: mstv\icreatepropbagonregkey.htm
tech.root: mstv
ms.assetid: f634a04f-911f-4d53-be70-d5dbf2395ce5
ms.date: 12/05/2018
ms.keywords: ICreatePropBagOnRegKey, ICreatePropBagOnRegKey interface [Microsoft TV Technologies], ICreatePropBagOnRegKey interface [Microsoft TV Technologies],described, ICreatePropBagOnRegKeyInterface, mstv.icreatepropbagonregkey, regbag/ICreatePropBagOnRegKey
req.header: regbag.h
req.include-header: Tuner.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: None supported
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Regbag.idl
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
 - ICreatePropBagOnRegKey
 - regbag/ICreatePropBagOnRegKey
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - regbag.h
api_name:
 - ICreatePropBagOnRegKey
---

# ICreatePropBagOnRegKey interface


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

The <b>ICreatePropBagOnRegKey</b> interface creates a property bag that can store information in the system registry.

Use this interface to store the default tune request in the registry. When Microsoft® Internet Explorer® loads a "tv:" object in a Web page, it automatically tunes to the default tune request.

## -inheritance

The <b>ICreatePropBagOnRegKey</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>ICreatePropBagOnRegKey</b> also has these types of members:
<ul>
<li><a href="/">Methods</a></li>
</ul>

## -remarks

To declare the interface identifier (IID) for this interface, use the <b>__uuidof</b> operator: <code>__uuidof(ICreatePropBagOnRegKey)</code>.

## -see-also

<a href="/previous-versions/windows/desktop/mstv/tuning-model-interfaces">Tuning Model Interfaces</a>
