---
UID: NF:mmcobj.ISnapinProperties.Initialize
title: ISnapinProperties::Initialize (mmcobj.h)
description: The Initialize method initializes a snap-in.
helpviewer_keywords: ["ISnapinProperties interface [MMC]","Initialize method","ISnapinProperties.Initialize","ISnapinProperties::Initialize","Initialize","Initialize method [MMC]","Initialize method [MMC]","ISnapinProperties interface","_slate_isnapinproperties_initialize","mmc.isnapinproperties_initialize","mmcobj/ISnapinProperties::Initialize"]
old-location: mmc\isnapinproperties_initialize.htm
tech.root: mmc
ms.assetid: b5140b15-d622-4abe-baef-061fe13a213f
ms.date: 12/05/2018
ms.keywords: ISnapinProperties interface [MMC],Initialize method, ISnapinProperties.Initialize, ISnapinProperties::Initialize, Initialize, Initialize method [MMC], Initialize method [MMC],ISnapinProperties interface, _slate_isnapinproperties_initialize, mmc.isnapinproperties_initialize, mmcobj/ISnapinProperties::Initialize
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
 - ISnapinProperties::Initialize
 - mmcobj/ISnapinProperties::Initialize
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
 - ISnapinProperties.Initialize
---

# ISnapinProperties::Initialize


## -description

The 
<b>Initialize</b> method initializes a snap-in.

## -parameters

### -param pProperties [in]

<a href="/previous-versions/windows/desktop/mmc/properties-collection">Properties</a> collection that can be used by the snap-in for initialization.

## -returns

If successful, the return value is S_OK; otherwise, the return value is E_FAIL.