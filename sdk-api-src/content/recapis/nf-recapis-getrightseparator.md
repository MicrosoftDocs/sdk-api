---
UID: NF:recapis.GetRightSeparator
title: GetRightSeparator function (recapis.h)
description: Gets the right separator for the recognizer context.
helpviewer_keywords: ["GetRightSeparator","GetRightSeparator function [Tablet PC]","recapis/GetRightSeparator","tablet.getrightseparator"]
old-location: tablet\getrightseparator.htm
tech.root: tablet
ms.assetid: 1fc11447-3125-4853-bba6-2784e69d033e
ms.date: 12/05/2018
ms.keywords: GetRightSeparator, GetRightSeparator function [Tablet PC], recapis/GetRightSeparator, tablet.getrightseparator
req.header: recapis.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps \| UWP apps]
req.target-min-winversvr: None supported
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: inkobjcore.lib
req.dll: inkobjcore.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - GetRightSeparator
 - recapis/GetRightSeparator
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - recapis.h
api_name:
 - GetRightSeparator
---

# GetRightSeparator function


## -description

Gets the right separator for the recognizer context.

## -parameters

### -param hrc

The handle to the recognizer context.

### -param pcSize [in, out]

A pointer to the size of the right separator.

### -param pwcRightSeparator [out, optional]

A pointer to the right separator.

## -returns

If this function succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

