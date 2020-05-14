---
UID: NF:recapis.GetLeftSeparator
title: GetLeftSeparator function (recapis.h)
description: Gets the left separator for the recognizer context.helpviewer_keywords: ["GetLeftSeparator","GetLeftSeparator function [Tablet PC]","recapis/GetLeftSeparator","tablet.getleftseparator"]
old-location: tablet\getleftseparator.htm
tech.root: tablet
ms.assetid: 5528d31e-580f-4da7-b683-e9ea2931989b
ms.date: 12/05/2018
ms.keywords: GetLeftSeparator, GetLeftSeparator function [Tablet PC], recapis/GetLeftSeparator, tablet.getleftseparator
f1_keywords:
- recapis/GetLeftSeparator
dev_langs:
- c++
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- HeaderDef
api_location:
- recapis.h
api_name:
- GetLeftSeparator
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# GetLeftSeparator function


## -description


Gets the left separator for the recognizer context.


## -parameters




### -param hrc

The handle to the recognizer context.


### -param pcSize [in, out]

A pointer to the size of the left separator.


### -param pwcLeftSeparator [out]

A pointer to the left separator.


## -returns



If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



