---
UID: NN:mmcobj.ISnapinProperties
title: ISnapinProperties (mmcobj.h)
description: The ISnapinProperties interface enables a snap-in to initialize the snap-in's properties and receive notification when a property is added, changed, or deleted.
helpviewer_keywords: ["ISnapinProperties","ISnapinProperties interface [MMC]","ISnapinProperties interface [MMC]","described","_slate_isnapinproperties","mmc.isnapinproperties","mmcobj/ISnapinProperties"]
old-location: mmc\isnapinproperties.htm
tech.root: mmc
ms.assetid: d3a7d7e0-25c3-4dfa-8984-ca9c91db8493
ms.date: 12/05/2018
ms.keywords: ISnapinProperties, ISnapinProperties interface [MMC], ISnapinProperties interface [MMC],described, _slate_isnapinproperties, mmc.isnapinproperties, mmcobj/ISnapinProperties
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ISnapinProperties
 - mmcobj/ISnapinProperties
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Mmcobj.h
api_name:
 - ISnapinProperties
---

# ISnapinProperties interface


## -description

The 
<b>ISnapinProperties</b> interface enables a snap-in to initialize the snap-in's properties and receive notification when a property is added, changed, or deleted.

The 
<b>ISnapinProperties</b> interface is implemented by the snap-in. The properties provided by the 
<b>ISnapinProperties</b> interface correspond to the 
<a href="/previous-versions/windows/desktop/mmc/snapin-properties">Properties</a> property of the 
<a href="/previous-versions/windows/desktop/mmc/snapin-object">SnapIn</a> object. The 
<b>SnapIn</b> object is part of the 
<a href="/previous-versions/windows/desktop/mmc/mmc-2-0-automation-object-model">MMC 2.0 automation object model</a>.

## -inheritance

The <b>ISnapinProperties</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>ISnapinProperties</b> also has these types of members:

