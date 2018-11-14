---
UID: NF:mmcobj.ISnapinProperties.Initialize
title: ISnapinProperties::Initialize
author: windows-sdk-content
description: The Initialize method initializes a snap-in.
old-location: mmc\isnapinproperties_initialize.htm
tech.root: mmc
ms.assetid: b5140b15-d622-4abe-baef-061fe13a213f
ms.author: windowssdkdev
ms.date: 10/05/2018
ms.keywords: ISnapinProperties interface [MMC],Initialize method, ISnapinProperties.Initialize, ISnapinProperties::Initialize, Initialize, Initialize method [MMC], Initialize method [MMC],ISnapinProperties interface, _slate_isnapinproperties_initialize, mmc.isnapinproperties_initialize, mmcobj/ISnapinProperties::Initialize
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
 - ISnapinProperties.Initialize
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- mmcobj.h
: 
- ISnapinProperties.Initialize
: 
---

# ISnapinProperties::Initialize


## -description


The 
<b>Initialize</b> method initializes a snap-in.


## -parameters




### -param pProperties [in]


<a href="https://msdn.microsoft.com/40d3ebc4-5b91-4869-a6e2-6cc3b8d73b26">Properties</a> collection that can be used by the snap-in for initialization.


## -returns



If successful, the return value is S_OK; otherwise, the return value is E_FAIL.



