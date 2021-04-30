---
UID: NF:mmc.IConsole.SetToolbar
title: IConsole::SetToolbar (mmc.h)
description: Sets the toolbar interface to be used for this instance of IComponent. Be aware that this is used only by instances of IComponent.
helpviewer_keywords: ["IConsole interface [MMC]","SetToolbar method","IConsole.SetToolbar","IConsole::SetToolbar","SetToolbar","SetToolbar method [MMC]","SetToolbar method [MMC]","IConsole interface","mmc.iconsole_settoolbar","mmc/IConsole::SetToolbar"]
old-location: mmc\iconsole_settoolbar.htm
tech.root: mmc
ms.assetid: 242F3143-A6C1-49A1-A51B-735EE5D5D353
ms.date: 12/05/2018
ms.keywords: IConsole interface [MMC],SetToolbar method, IConsole.SetToolbar, IConsole::SetToolbar, SetToolbar, SetToolbar method [MMC], SetToolbar method [MMC],IConsole interface, mmc.iconsole_settoolbar, mmc/IConsole::SetToolbar
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
 - IConsole::SetToolbar
 - mmc/IConsole::SetToolbar
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
 - IConsole.SetToolbar
---

# IConsole::SetToolbar


## -description

Sets the toolbar interface to be used for this instance of 
<a href="/windows/desktop/api/mmc/nn-mmc-icomponent">IComponent</a>. Be aware that this is used only by instances of 
<b>IComponent</b>.

## -parameters

### -param pToolbar [in]

A pointer to the 
<a href="/windows/desktop/api/mmc/nn-mmc-itoolbar">IToolbar</a> interface.

## -returns

This method can return one of these values.

## -see-also

<a href="/windows/desktop/api/mmc/nn-mmc-iconsole">IConsole</a>



<a href="/windows/desktop/api/mmc/nn-mmc-itoolbar">IToolbar</a>