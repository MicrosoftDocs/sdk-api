---
UID: NF:werapi.WerSetMaxProcessHoldMilliseconds
tech.root: wer
title: WerSetMaxProcessHoldMilliseconds
ms.date: 07/21/2023
targetos: Windows
description: Sets the maximum process hold time for Windows Error Reporting (WER), in milliseconds.
prerelease: false
req.assembly: 
req.construct-type: function
req.ddi-compliance: 
req.dll: 
req.header: werapi.h
req.idl: 
req.include-header: 
req.irql: 
req.kmdf-ver: 
req.lib: 
req.max-support: 
req.namespace: 
req.redist: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.target-type: 
req.type-library: 
req.umdf-ver: 
req.unicode-ansi: 
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - api-ms-win-core-windowserrorreporting-l1-1-3.dll
 - werapi.h
api_name:
 - WerSetMaxProcessHoldMilliseconds
f1_keywords:
 - WerSetMaxProcessHoldMilliseconds
 - werapi/WerSetMaxProcessHoldMilliseconds
dev_langs:
 - c++
helpviewer_keywords:
 - WerSetMaxProcessHoldMilliseconds
---

# WerSetMaxProcessHoldMilliseconds function

## -description

Sets the maximum process hold time for [Windows Error Reporting](../_wer/index.md) (WER), in milliseconds.

## -parameters

### -param dwMilliseconds

The process hold time, in milliseconds.

## -returns

This function returns **S_OK** on success or an error code on failure.

## -remarks

## -see-also
