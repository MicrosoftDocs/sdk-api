---
UID: NF:filehc.SetDotStuffingOnWrites
title: SetDotStuffingOnWrites function (filehc.h)
description: Enables dot-stuffing properties on the write path of the file handle cache of the message.
helpviewer_keywords: ["SetDotStuffingOnWrites","SetDotStuffingOnWrites function [Windows API]","filehc/SetDotStuffingOnWrites","winprog._setdotstuffingonwrites"]
old-location: winprog\_setdotstuffingonwrites.htm
tech.root: winprog
ms.assetid: 6191e097-3e8a-4149-85bb-88d804caa3ae
ms.date: 12/05/2018
ms.keywords: SetDotStuffingOnWrites, SetDotStuffingOnWrites function [Windows API], filehc/SetDotStuffingOnWrites, winprog._setdotstuffingonwrites
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
 - SetDotStuffingOnWrites
 - filehc/SetDotStuffingOnWrites
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
 - SetDotStuffingOnWrites
---

# SetDotStuffingOnWrites function


## -description

Enables dot-stuffing properties on the write path of the file handle cache of the message.

## -parameters

### -param pContext [in]

A pointer to an <a href="/previous-versions/exchange-server/exchange-10/ms528326(v=exchg.10)">FIO_CONTEXT</a> structure that contains context information.

### -param fEnable [in]

Specifies whether dot stuffing is available. If <b>FALSE</b>, all dot-stuffing behavior is turned off.

### -param fStripDots [in]

Specifies whether occurrences of "\r\n." are converted to "\r\n" within the message. If <b>TRUE</b>,  "\r\n." is converted to "\r\n" (unstuffing or stripping). If  <b>FALSE</b>,   "\r\n." is converted to "\r\n.." (stuffing).

## -returns

Returns <b>TRUE</b> if the function succeeds; otherwise, it is <b>FALSE</b>.

## -see-also

<a href="/previous-versions/exchange-server/exchange-10/ms528326(v=exchg.10)">FIO_CONTEXT</a>