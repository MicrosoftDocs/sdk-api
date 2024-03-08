---
UID: NF:recapis.GetContextPreferenceFlags
title: GetContextPreferenceFlags function (recapis.h)
description: Gets the context preference flags.
helpviewer_keywords: ["GetContextPreferenceFlags","GetContextPreferenceFlags function [Tablet PC]","recapis/GetContextPreferenceFlags","tablet.getcontextpreferenceflags"]
old-location: tablet\getcontextpreferenceflags.htm
tech.root: tablet
ms.assetid: 0804cd56-7baf-4b93-97b5-4131118b72b6
ms.date: 12/05/2018
ms.keywords: GetContextPreferenceFlags, GetContextPreferenceFlags function [Tablet PC], recapis/GetContextPreferenceFlags, tablet.getcontextpreferenceflags
req.header: recapis.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
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
req.dll: inkobjcore.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - GetContextPreferenceFlags
 - recapis/GetContextPreferenceFlags
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
 - GetContextPreferenceFlags
---

# GetContextPreferenceFlags function


## -description

Gets the context preference flags.

## -parameters

### -param hrc

The handle to the recognizer context.

### -param pdwContextPreferenceFlags

The handle to the context preference flags.

## -returns

If this function succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

