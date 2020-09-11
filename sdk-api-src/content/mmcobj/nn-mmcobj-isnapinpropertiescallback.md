---
UID: NN:mmcobj.ISnapinPropertiesCallback
title: ISnapinPropertiesCallback (mmcobj.h)
description: The ISnapinPropertiesCallback interface adds property names for the snap-in. This interface is implemented by MMC for the snap-in.
helpviewer_keywords: ["ISnapinPropertiesCallback","ISnapinPropertiesCallback interface [MMC]","ISnapinPropertiesCallback interface [MMC]","described","_slate_isnapinpropertiescallback","mmc.isnapinpropertiescallback","mmcobj/ISnapinPropertiesCallback"]
old-location: mmc\isnapinpropertiescallback.htm
tech.root: mmc
ms.assetid: d02d265c-f3fa-4332-910e-f0d9d4f0687a
ms.date: 12/05/2018
ms.keywords: ISnapinPropertiesCallback, ISnapinPropertiesCallback interface [MMC], ISnapinPropertiesCallback interface [MMC],described, _slate_isnapinpropertiescallback, mmc.isnapinpropertiescallback, mmcobj/ISnapinPropertiesCallback
req.header: mmcobj.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: Mmcndmgr.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ISnapinPropertiesCallback
 - mmcobj/ISnapinPropertiesCallback
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Mmcndmgr.dll
api_name:
 - ISnapinPropertiesCallback
---

# ISnapinPropertiesCallback interface


## -description

The 
<b>ISnapinPropertiesCallback</b> interface adds property names for the snap-in. This interface is implemented by MMC for the snap-in.

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ISnapinPropertiesCallback</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>ISnapinPropertiesCallback</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ISnapinPropertiesCallback</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mmcobj/nf-mmcobj-isnapinpropertiescallback-addpropertyname">AddPropertyName</a>
</td>
<td align="left" width="63%">
Adds a property by name for the snap-in to use.

</td>
</tr>
</table>

