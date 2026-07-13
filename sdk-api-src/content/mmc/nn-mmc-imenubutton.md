---
UID: NN:mmc.IMenuButton
title: IMenuButton (mmc.h)
description: The IMenuButton interface enables the user to add and manage menu buttons for a snap-in.
helpviewer_keywords: ["IMenuButton","IMenuButton interface [MMC]","IMenuButton interface [MMC]","described","_slate_imenubutton","mmc.imenubutton","mmc/IMenuButton"]
old-location: mmc\imenubutton.htm
tech.root: mmc
ms.assetid: 51bbd98a-7017-497a-858a-dd63cefc679a
ms.date: 12/05/2018
ms.keywords: IMenuButton, IMenuButton interface [MMC], IMenuButton interface [MMC],described, _slate_imenubutton, mmc.imenubutton, mmc/IMenuButton
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
 - IMenuButton
 - mmc/IMenuButton
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
 - IMenuButton
---

# IMenuButton interface


## -description

The 
<b>IMenuButton</b> interface enables the user to add and manage menu buttons for a snap-in. MMC provides one menu bar per view; when a snap-in has the focus you can add one or more menu buttons for the view to this bar. These buttons are always added by appending them to the buttons already in the menu bar.

## -inheritance

The <b>IMenuButton</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IMenuButton</b> also has these types of members:

