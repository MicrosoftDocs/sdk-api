---
UID: NF:mmc.IConsole.QueryResultView
title: IConsole::QueryResultView (mmc.h)
description: Queries IConsole for the result view object IUnknown interface pointer.
helpviewer_keywords: ["IConsole interface [MMC]","QueryResultView method","IConsole.QueryResultView","IConsole::QueryResultView","QueryResultView","QueryResultView method [MMC]","QueryResultView method [MMC]","IConsole interface","mmc.iconsole_queryresultview","mmc/IConsole::QueryResultView"]
old-location: mmc\iconsole_queryresultview.htm
tech.root: mmc
ms.assetid: A13410D1-38F3-489A-8AAC-BD2909341ACB
ms.date: 12/05/2018
ms.keywords: IConsole interface [MMC],QueryResultView method, IConsole.QueryResultView, IConsole::QueryResultView, QueryResultView, QueryResultView method [MMC], QueryResultView method [MMC],IConsole interface, mmc.iconsole_queryresultview, mmc/IConsole::QueryResultView
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
 - IConsole::QueryResultView
 - mmc/IConsole::QueryResultView
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
 - IConsole.QueryResultView
---

# IConsole::QueryResultView


## -description

Queries 
<a href="/windows/desktop/api/mmc/nn-mmc-iconsole">IConsole</a> for the result view object 
<a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface pointer.

## -parameters

### -param pUnknown [out]

A pointer to the location of the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface pointer to the result view object.

## -returns

This method can return one of these values.

## -remarks

<b>QueryResultView</b> can be used when the result view is an OLE custom control (OCX) that implements the 
<a href="/windows/desktop/WinAuto/idispatch-interface">IDispatch</a> interface. The user should call 
<b>QueryResultView</b> to get the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> pointer to the OCX. This is necessary because the Node Manager handles the creation of the OCX.

## -see-also

<a href="/windows/desktop/api/mmc/nn-mmc-iconsole">IConsole</a>