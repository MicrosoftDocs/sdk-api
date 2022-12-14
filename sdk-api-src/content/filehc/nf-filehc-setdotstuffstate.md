---
UID: NF:filehc.SetDotStuffState
title: SetDotStuffState function (filehc.h)
description: Enables dot stuffing to be set in an FIO_CONTEXT structure.
helpviewer_keywords: ["SetDotStuffState","SetDotStuffState function [Windows API]","filehc/SetDotStuffState","winprog._setdotstuffstate"]
old-location: winprog\_setdotstuffstate.htm
tech.root: winprog
ms.assetid: 3acfaf74-ec36-4afb-b358-425bd5062153
ms.date: 12/05/2018
ms.keywords: SetDotStuffState, SetDotStuffState function [Windows API], filehc/SetDotStuffState, winprog._setdotstuffstate
req.header: filehc.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Fcachdll.lib
req.dll: Fcachdll.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - SetDotStuffState
 - filehc/SetDotStuffState
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Fcachdll.dll
api_name:
 - SetDotStuffState
---

# SetDotStuffState function


## -description

Enables dot stuffing to be set in an <a href="/previous-versions/exchange-server/exchange-10/ms528326(v=exchg.10)">FIO_CONTEXT</a> structure.

## -parameters

### -param pContext [in]

A pointer to the <a href="/previous-versions/exchange-server/exchange-10/ms528326(v=exchg.10)">FIO_CONTEXT</a> structure to be examined.

### -param fKnown [in]

Specifies whether the dot stuff state is known. If <b>TRUE</b>, the message requires dot stuffing and the <i>fRequiresStuffing</i> parameter becomes meaningful.

### -param fRequiresStuffing [in]

Specifies whether dot stuffing is required. If <i>fKnown</i> is  <b>TRUE</b>, <i>fRequiresStuffing</i> can be either <b>TRUE</b> or <b>FALSE</b>. If <i>fKnown</i> is <b>FALSE</b>, <i>fRequiresStuffing</i> is ignored.

## -see-also

<a href="/previous-versions/exchange-server/exchange-10/ms528326(v=exchg.10)">FIO_CONTEXT</a>