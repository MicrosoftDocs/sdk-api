---
UID: NN:ehstorapi.IEnhancedStorageSiloAction
title: IEnhancedStorageSiloAction (ehstorapi.h)
description: Use this interface as a point of access for actions involving IEEE 1667 silos.
helpviewer_keywords: ["IEnhancedStorageSiloAction","IEnhancedStorageSiloAction interface [Enhanced Storage]","IEnhancedStorageSiloAction interface [Enhanced Storage]","described","ehstorapi/IEnhancedStorageSiloAction","enstor.ienhancedstoragesiloaction"]
old-location: enstor\ienhancedstoragesiloaction.htm
tech.root: enstor
ms.assetid: 6deb7e22-f153-45fd-98ea-53a2e5692df7
ms.date: 12/05/2018
ms.keywords: IEnhancedStorageSiloAction, IEnhancedStorageSiloAction interface [Enhanced Storage], IEnhancedStorageSiloAction interface [Enhanced Storage],described, ehstorapi/IEnhancedStorageSiloAction, enstor.ienhancedstoragesiloaction
f1_keywords:
- ehstorapi/IEnhancedStorageSiloAction
dev_langs:
- c++
req.header: ehstorapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista with SP2 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: EhStorAPI.idl
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
- EhStorAPI.h
api_name:
- IEnhancedStorageSiloAction
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IEnhancedStorageSiloAction interface


## -description


 Use this interface as a point of access for actions involving IEEE 1667 silos.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IEnhancedStorageSiloAction</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IEnhancedStorageSiloAction</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IEnhancedStorageSiloAction</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/ehstorapi/nf-ehstorapi-ienhancedstoragesiloaction-getdescription">GetDescription</a>
</td>
<td align="left" width="63%">
Returns a descriptive string for the action specified by the <b>IEnhancedStorageSiloAction</b> object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/ehstorapi/nf-ehstorapi-ienhancedstoragesiloaction-getname">GetName</a>
</td>
<td align="left" width="63%">
Returns a string for the name of the action specified by the <b>IEnhancedStorageSiloAction</b> object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/ehstorapi/nf-ehstorapi-ienhancedstoragesiloaction-invoke">Invoke</a>
</td>
<td align="left" width="63%">
Performs the action specified by an <b>IEnhancedStorageSiloAction</b> object.

</td>
</tr>
</table> 

