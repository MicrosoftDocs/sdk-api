---
UID: NN:mmcobj.ISnapinProperties
title: ISnapinProperties (mmcobj.h)
author: windows-sdk-content
description: The ISnapinProperties interface enables a snap-in to initialize the snap-in's properties and receive notification when a property is added, changed, or deleted.
old-location: mmc\isnapinproperties.htm
tech.root: mmc
ms.assetid: d3a7d7e0-25c3-4dfa-8984-ca9c91db8493
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: ISnapinProperties, ISnapinProperties interface [MMC], ISnapinProperties interface [MMC],described, _slate_isnapinproperties, mmc.isnapinproperties, mmcobj/ISnapinProperties
ms.topic: interface
f1_keywords: 
 - "mmcobj/ISnapinProperties"
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
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Mmcobj.h
api_name:
 - ISnapinProperties
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ISnapinProperties interface


## -description


The 
<b>ISnapinProperties</b> interface enables a snap-in to initialize the snap-in's properties and receive notification when a property is added, changed, or deleted.

The 
<b>ISnapinProperties</b> interface is implemented by the snap-in. The properties provided by the 
<b>ISnapinProperties</b> interface correspond to the 
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/mmc/snapin-properties">Properties</a> property of the 
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/mmc/snapin-object">SnapIn</a> object. The 
<b>SnapIn</b> object is part of the 
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/mmc/mmc-2-0-automation-object-model">MMC 2.0 automation object model</a>.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ISnapinProperties</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>ISnapinProperties</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ISnapinProperties</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mmcobj/nf-mmcobj-isnapinproperties-initialize">Initialize</a>
</td>
<td align="left" width="63%">
Provides the snap-in with the 
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/mmc/properties-collection">Properties</a> collection, which can be used for initialization.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mmcobj/nf-mmcobj-isnapinproperties-propertieschanged">PropertiesChanged</a>
</td>
<td align="left" width="63%">
Informs the snap-in that one or more of its configuration properties has been added, deleted, or changed.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mmcobj/nf-mmcobj-isnapinproperties-querypropertynames">QueryPropertyNames</a>
</td>
<td align="left" width="63%">
Returns the names of the properties that the snap-in uses for configuration.

</td>
</tr>
</table> 

