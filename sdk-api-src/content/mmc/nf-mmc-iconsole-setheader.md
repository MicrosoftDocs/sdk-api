---
UID: NF:mmc.IConsole.SetHeader
title: IConsole::SetHeader (mmc.h)
description: Sets the header interface to use for this instance of IComponent. This is used only by instances of IComponent.
helpviewer_keywords: ["IConsole interface [MMC]","SetHeader method","IConsole.SetHeader","IConsole::SetHeader","SetHeader","SetHeader method [MMC]","SetHeader method [MMC]","IConsole interface","mmc.iconsole_setheader","mmc/IConsole::SetHeader"]
old-location: mmc\iconsole_setheader.htm
tech.root: mmc
ms.assetid: B607F719-3D74-48EB-A1FD-A311B5C3F6A1
ms.date: 12/05/2018
ms.keywords: IConsole interface [MMC],SetHeader method, IConsole.SetHeader, IConsole::SetHeader, SetHeader, SetHeader method [MMC], SetHeader method [MMC],IConsole interface, mmc.iconsole_setheader, mmc/IConsole::SetHeader
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
 - IConsole::SetHeader
 - mmc/IConsole::SetHeader
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
 - IConsole.SetHeader
---

# IConsole::SetHeader


## -description

<div class="alert"><b>Note</b>  The <b>IConsole::SetHeader</b> method is obsolete in MMC version 1.1 and later. It is no longer required by snap-ins. However, the method can still safely be used by snap-ins that already call it.</div><div> </div>Sets the header interface to use for this instance of 
<a href="/windows/desktop/api/mmc/nn-mmc-icomponent">IComponent</a>. This is used only by instances of 
<b>IComponent</b>.

## -parameters

### -param pHeader [in]

A pointer to the 
<b>IHeaderCtrl</b> interface.

## -returns

This method can return one of these values.

## -remarks

The snap-in must instruct the console to release the 
<b>IHeaderCtrl</b> interface by calling <b>IConsole::SetHeader</b>(NULL).

The best time to release the 
<b>IHeaderCtrl</b> interface is during a call to 
<a href="/windows/desktop/api/mmc/nf-mmc-icomponent-destroy">IComponent::Destroy</a>.

## -see-also

<a href="/windows/desktop/api/mmc/nn-mmc-iconsole">IConsole</a>