---
UID: NF:mmc.IConsole.QueryConsoleVerb
title: IConsole::QueryConsoleVerb (mmc.h)
description: Queries for the IConsoleVerb interface.
helpviewer_keywords: ["IConsole interface [MMC]","QueryConsoleVerb method","IConsole.QueryConsoleVerb","IConsole::QueryConsoleVerb","QueryConsoleVerb","QueryConsoleVerb method [MMC]","QueryConsoleVerb method [MMC]","IConsole interface","mmc.iconsole_queryconsoleverb","mmc/IConsole::QueryConsoleVerb"]
old-location: mmc\iconsole_queryconsoleverb.htm
tech.root: mmc
ms.assetid: 6C40014C-EBCC-455C-A575-4637B253439C
ms.date: 12/05/2018
ms.keywords: IConsole interface [MMC],QueryConsoleVerb method, IConsole.QueryConsoleVerb, IConsole::QueryConsoleVerb, QueryConsoleVerb, QueryConsoleVerb method [MMC], QueryConsoleVerb method [MMC],IConsole interface, mmc.iconsole_queryconsoleverb, mmc/IConsole::QueryConsoleVerb
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
 - IConsole::QueryConsoleVerb
 - mmc/IConsole::QueryConsoleVerb
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
 - IConsole.QueryConsoleVerb
---

# IConsole::QueryConsoleVerb


## -description

Queries for the 
<a href="/windows/desktop/api/mmc/nn-mmc-iconsoleverb">IConsoleVerb</a> interface.

## -parameters

### -param ppConsoleVerb [out]

A pointer to the address of a variable that receives the 
<a href="/windows/desktop/api/mmc/nn-mmc-iconsoleverb">IConsoleVerb</a> interface pointer.

## -returns

This method can return one of these values.

## -remarks

This method should be called from an 
<a href="/windows/desktop/api/mmc/nn-mmc-iconsole">IConsole</a> interface pointer obtained through the 
<a href="/windows/desktop/api/mmc/nn-mmc-icomponent">IComponent</a> interface.

## -see-also

<a href="/windows/desktop/api/mmc/nn-mmc-iconsole">IConsole</a>



<a href="/windows/desktop/api/mmc/nn-mmc-iconsoleverb">IConsoleVerb</a>