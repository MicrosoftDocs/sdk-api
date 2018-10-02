---
UID: NN:mmcobj.ISnapinProperties
title: ISnapinProperties
author: windows-sdk-content
description: The ISnapinProperties interface enables a snap-in to initialize the snap-in's properties and receive notification when a property is added, changed, or deleted.
old-location: mmc\isnapinproperties.htm
tech.root: MMC
ms.assetid: d3a7d7e0-25c3-4dfa-8984-ca9c91db8493
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: ISnapinProperties, ISnapinProperties interface [MMC], ISnapinProperties interface [MMC],described, _slate_isnapinproperties, mmc.isnapinproperties, mmcobj/ISnapinProperties
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
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
---

# ISnapinProperties interface


## -description


The 
<b>ISnapinProperties</b> interface enables a snap-in to initialize the snap-in's properties and receive notification when a property is added, changed, or deleted.

The 
<b>ISnapinProperties</b> interface is implemented by the snap-in. The properties provided by the 
<b>ISnapinProperties</b> interface correspond to the 
<a href="https://msdn.microsoft.com/0895ff50-4c7e-4d77-9710-a9d0e76c62d0">Properties</a> property of the 
<a href="https://msdn.microsoft.com/94a9c623-8778-4010-bb69-6ac0d7ae5ca9">SnapIn</a> object. The 
<b>SnapIn</b> object is part of the 
<a href="https://msdn.microsoft.com/eb7c92e7-d834-4736-bff4-74940c9bb194">MMC 2.0 automation object model</a>.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ISnapinProperties</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>ISnapinProperties</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/b5140b15-d622-4abe-baef-061fe13a213f">Initialize</a>
</td>
<td align="left" width="63%">
Provides the snap-in with the 
<a href="https://msdn.microsoft.com/40d3ebc4-5b91-4869-a6e2-6cc3b8d73b26">Properties</a> collection, which can be used for initialization.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/6e64a620-9c1d-4803-81a0-ec432c30fbc9">PropertiesChanged</a>
</td>
<td align="left" width="63%">
Informs the snap-in that one or more of its configuration properties has been added, deleted, or changed.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/41f949aa-4be5-4e60-aa1d-0605f489fec6">QueryPropertyNames</a>
</td>
<td align="left" width="63%">
Returns the names of the properties that the snap-in uses for configuration.

</td>
</tr>
</table> 

