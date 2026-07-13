---
UID: NF:winddi.EngMulDiv
title: EngMulDiv function (winddi.h)
description: The EngMulDiv function multiplies two 32-bit values and then divides the 64-bit result by a third 32-bit value.
helpviewer_keywords: ["EngMulDiv","EngMulDiv function [Display Devices]","display.engmuldiv","gdifncs_0d175bf5-b421-43e5-acc5-a11299b0d990.xml","winddi/EngMulDiv"]
old-location: display\engmuldiv.htm
tech.root: display
ms.assetid: e1d9d790-4038-445c-a1ea-fe689cb0e694
ms.date: 12/05/2018
ms.keywords: EngMulDiv, EngMulDiv function [Display Devices], display.engmuldiv, gdifncs_0d175bf5-b421-43e5-acc5-a11299b0d990.xml, winddi/EngMulDiv
req.header: winddi.h
req.include-header: Winddi.h
req.target-type: Universal
req.target-min-winverclnt: Available in Windows 2000 and later versions of the Windows operating systems.
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
req.lib: Win32k.lib
req.dll: Win32k.sys
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - EngMulDiv
 - winddi/EngMulDiv
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - ext-ms-win-core-win32k-base-export-l1-1-0.dll
 - Win32k.sys
api_name:
 - EngMulDiv
---

# EngMulDiv function


## -description

The <b>EngMulDiv</b> function multiplies two 32-bit values and then divides the 64-bit result by a third 32-bit value.

## -parameters

### -param a [in]

Specifies the 32-bit signed multiplicand.

### -param b [in]

Specifies the 32-bit signed multiplier.

### -param c [in]

Specifies the 32-bit signed divisor by which the result of <i>a</i>*<i>b</i> is to be divided.

## -returns

<b>EngMulDiv</b> returns the signed 32-bit result of the multiplication and division. The return value is rounded up or down to the nearest integer.

## -remarks

Drivers should not pass a zero divisor to <b>EngMulDiv</b>.

