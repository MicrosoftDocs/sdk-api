---
UID: NN:regbag.ICreatePropBagOnRegKey
title: ICreatePropBagOnRegKey
author: windows-driver-content
description: The ICreatePropBagOnRegKey interface creates a property bag that can store information in the system registry.Use this interface to store the default tune request in the registry.
old-location: mstv\icreatepropbagonregkey.htm
old-project: mstv
ms.assetid: f634a04f-911f-4d53-be70-d5dbf2395ce5
ms.author: windowsdriverdev
ms.date: 4/26/2018
ms.keywords: ICreatePropBagOnRegKey, ICreatePropBagOnRegKey interface [Microsoft TV Technologies], ICreatePropBagOnRegKey interface [Microsoft TV Technologies], described, ICreatePropBagOnRegKeyInterface, mstv.icreatepropbagonregkey, regbag/ICreatePropBagOnRegKey
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: interface
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
req.typenames: RECO_RANGE, RECO_RANGE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	regbag.h
api_name:
-	ICreatePropBagOnRegKey
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 SP2 or later
---

# ICreatePropBagOnRegKey interface


## -description



The <b>ICreatePropBagOnRegKey</b> interface creates a property bag that can store information in the system registry.

Use this interface to store the default tune request in the registry. When Microsoft® Internet Explorer® loads a "tv:" object in a Web page, it automatically tunes to the default tune request.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ICreatePropBagOnRegKey</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>ICreatePropBagOnRegKey</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/d6410ead-7364-4db4-a4c9-cafe5fbf2e84">Create</a>
</td>
<td align="left" width="63%">
Creates a property bag that can store information in the system registry.

</td>
</tr>
</table> 


## -remarks



To declare the interface identifier (IID) for this interface, use the <b>__uuidof</b> operator: <code>__uuidof(ICreatePropBagOnRegKey)</code>.




## -see-also




<a href="https://msdn.microsoft.com/5d956e1d-88b3-4236-9987-f37f674645de">Tuning Model Interfaces</a>
 

 

