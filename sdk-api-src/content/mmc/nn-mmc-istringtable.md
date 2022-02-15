---
UID: NN:mmc.IStringTable
title: IStringTable (mmc.h)
description: The IStringTable interface is introduced in MMC 1.1.
helpviewer_keywords: ["IStringTable","IStringTable interface [MMC]","IStringTable interface [MMC]","described","_slate_istringtable","mmc.istringtable","mmc/IStringTable"]
old-location: mmc\istringtable.htm
tech.root: mmc
ms.assetid: 3b4cfc92-4f50-4b62-bb2c-77c8e0e003da
ms.date: 12/05/2018
ms.keywords: IStringTable, IStringTable interface [MMC], IStringTable interface [MMC],described, _slate_istringtable, mmc.istringtable, mmc/IStringTable
req.header: mmc.h
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
 - IStringTable
 - mmc/IStringTable
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
 - IStringTable
---

# IStringTable interface


## -description

The 
<b>IStringTable</b> interface is introduced in MMC 1.1.

The 
<b>IStringTable</b> interface provides a way to store string data with the snap-in. A string table is created in the console file as required for each snap-in by MMC.

The 
<b>IStringTable</b> interface allows strings to be saved in the console file. Be aware that this interface is designed to work with specialized localization tools. Snap-ins without access to these localization tools will not benefit from using this interface.

## -inheritance

The <b>IStringTable</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IStringTable</b> also has these types of members:

