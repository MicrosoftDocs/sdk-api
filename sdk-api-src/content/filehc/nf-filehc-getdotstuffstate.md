---
UID: NF:filehc.GetDotStuffState
title: GetDotStuffState function (filehc.h)
description: Determines whether dots are added to the file when any dot stuffing mechanisms are turned on.
helpviewer_keywords: ["GetDotStuffState","GetDotStuffState function [Windows API]","filehc/GetDotStuffState","winprog._getdotstuffstate"]
old-location: winprog\_getdotstuffstate.htm
tech.root: winprog
ms.assetid: 069d9cc9-0478-457a-826b-2e4d1e1b0b05
ms.date: 12/05/2018
ms.keywords: GetDotStuffState, GetDotStuffState function [Windows API], filehc/GetDotStuffState, winprog._getdotstuffstate
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
 - GetDotStuffState
 - filehc/GetDotStuffState
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
 - GetDotStuffState
---

# GetDotStuffState function


## -description

Determines whether dots are added to the file when any dot stuffing mechanisms are turned on.

## -parameters

### -param pContext [in]

A pointer to the <a href="/previous-versions/exchange-server/exchange-10/ms528326(v=exchg.10)">FIO_CONTEXT</a> structure.

### -param fReads [in]

Indicates the dot stuff states that resulted from reads or from writes. If <b>TRUE</b>, the states of Reads are provided. If <b>FALSE</b>, the states of Writes are provided.

### -param pfStuffed [out]

Indicates whether any dots were processed, scanned, or modified. If no dots were processed, scanned, or modified, this value is <b>FALSE</b>; otherwise, it is <b>TRUE</b>. 

<div class="alert"><b>Note</b>  This parameter cannot be set to <b>NULL</b>.</div>
<div> </div>

### -param pfStoredWithDots [out]

Indicates whether the file was stored with stuffed dots.

## -returns

Returns <b>TRUE</b> if the dot stuff state is known; otherwise, it returns <b>FALSE</b>.

## -remarks

The information about dot stuffing is provided by DOT_STUFF_MANAGER objects.

## -see-also

<a href="/previous-versions/exchange-server/exchange-10/ms528326(v=exchg.10)">FIO_CONTEXT</a>