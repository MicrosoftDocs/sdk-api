---
UID: NF:advpub.RegInstallW
title: RegInstallW function (advpub.h)
description: Updates the string registry values in the provided table. (Unicode)
helpviewer_keywords: ["RegInstallW", "RegInstallW function [Windows API]", "advpub/RegInstallW", "winprog.reginstallw"]
old-location: winprog\reginstallw.htm
tech.root: winprog
ms.assetid: 3E3A48B6-FAF8-4C21-8438-41FA94937A39
ms.date: 12/05/2018
ms.keywords: RegInstallW, RegInstallW function [Windows API], advpub/RegInstallW, winprog.reginstallw
req.header: advpub.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10 [desktop apps only]
req.target-min-winversvr: Windows Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Advpack.lib
req.dll: Advpack.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - RegInstallW
 - advpub/RegInstallW
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - advpack.dll
api_name:
 - RegInstallW
---

# RegInstallW function


## -description

Updates the string registry values in the provided table.

## -parameters

### -param hmod

The module containing the values to be updated.

### -param pszSection

The sections containing the values to be updated.

### -param pstTable

The table of values to be updated.

## -returns

Returns S_OK on success. Returns E_FAIL on failure.

## -remarks

> [!NOTE]
> The advpub.h header defines RegInstall as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

