---
UID: NF:mmc.IHeaderCtrl.SetColumnText
title: IHeaderCtrl::SetColumnText (mmc.h)
description: Sets the text of the title in a specific column.
helpviewer_keywords: ["IHeaderCtrl interface [MMC]","SetColumnText method","IHeaderCtrl.SetColumnText","IHeaderCtrl::SetColumnText","SetColumnText","SetColumnText method [MMC]","SetColumnText method [MMC]","IHeaderCtrl interface","mmc.iheaderctrl_setcolumntext","mmc/IHeaderCtrl::SetColumnText"]
old-location: mmc\iheaderctrl_setcolumntext.htm
tech.root: mmc
ms.assetid: B760D7E1-DE2D-4E1A-898C-5EC1E99E9B91
ms.date: 12/05/2018
ms.keywords: IHeaderCtrl interface [MMC],SetColumnText method, IHeaderCtrl.SetColumnText, IHeaderCtrl::SetColumnText, SetColumnText, SetColumnText method [MMC], SetColumnText method [MMC],IHeaderCtrl interface, mmc.iheaderctrl_setcolumntext, mmc/IHeaderCtrl::SetColumnText
req.header: mmc.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Mmc.idl
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
 - IHeaderCtrl::SetColumnText
 - mmc/IHeaderCtrl::SetColumnText
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
 - IHeaderCtrl.SetColumnText
---

# IHeaderCtrl::SetColumnText


## -description

Sets the text of the title in a specific column.

## -parameters

### -param nCol [in]

A zero-based index that specifies the location of the column.

### -param title [in]

A pointer to the string that represents the title of the column being inserted. This string can have  a maximum length of MAX_PATH characters.

## -returns

This method can return one of these values.

## -see-also

<a href="/windows/desktop/api/mmc/nn-mmc-iheaderctrl">IHeaderCtrl</a>