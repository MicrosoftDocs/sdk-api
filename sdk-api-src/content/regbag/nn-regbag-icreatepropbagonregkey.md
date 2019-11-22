---
UID: NN:regbag.ICreatePropBagOnRegKey
title: ICreatePropBagOnRegKey (regbag.h)

description: The ICreatePropBagOnRegKey interface creates a property bag that can store information in the system registry.Use this interface to store the default tune request in the registry.
old-location: mstv\icreatepropbagonregkey.htm
tech.root: mstv
ms.assetid: f634a04f-911f-4d53-be70-d5dbf2395ce5

ms.date: 12/05/2018
ms.keywords: ICreatePropBagOnRegKey, ICreatePropBagOnRegKey interface [Microsoft TV Technologies], ICreatePropBagOnRegKey interface [Microsoft TV Technologies],described, ICreatePropBagOnRegKeyInterface, mstv.icreatepropbagonregkey, regbag/ICreatePropBagOnRegKey
ms.topic: interface
f1_keywords: 
 - "regbag/ICreatePropBagOnRegKey"
dev_langs:
 - c++
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - regbag.h
api_name:
 - ICreatePropBagOnRegKey
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ICreatePropBagOnRegKey interface


## -description



The <b>ICreatePropBagOnRegKey</b> interface creates a property bag that can store information in the system registry.

Use this interface to store the default tune request in the registry. When Microsoft® Internet Explorer® loads a "tv:" object in a Web page, it automatically tunes to the default tune request.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ICreatePropBagOnRegKey</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>ICreatePropBagOnRegKey</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ICreatePropBagOnRegKey</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/regbag/nf-regbag-icreatepropbagonregkey-create">Create</a>
</td>
<td align="left" width="63%">
Creates a property bag that can store information in the system registry.

</td>
</tr>
</table> 


## -remarks



To declare the interface identifier (IID) for this interface, use the <b>__uuidof</b> operator: <code>__uuidof(ICreatePropBagOnRegKey)</code>.




## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/mstv/tuning-model-interfaces">Tuning Model Interfaces</a>
 

 

