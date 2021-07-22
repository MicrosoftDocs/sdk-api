---
UID: NF:intsafe.SSIZETMult
title: SSIZETMult function (intsafe.h)
description: Multiplies one SSIZE_T value by another.
helpviewer_keywords: ["SSIZETMult","SSIZETMult function [Windows Shell]","intsafe/SSIZETMult","shell.SSIZETMult"]
old-location: shell\SSIZETMult.htm
tech.root: shell
ms.assetid: 9b698951-dd9d-427c-9f95-63392ef0f0d4
ms.date: 12/05/2018
ms.keywords: SSIZETMult, SSIZETMult function [Windows Shell], intsafe/SSIZETMult, shell.SSIZETMult
req.header: intsafe.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps \| UWP apps]
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - SSIZETMult
 - intsafe/SSIZETMult
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - intsafe.h
api_name:
 - SSIZETMult
---

# SSIZETMult function


## -description

Multiplies one SSIZE_T value by another.

## -parameters

### -param Multiplicand [in]

The number to be multiplied.

### -param Multiplier [in]

The number by which to multiply <i>Multiplicand</i>.

### -param pResult [out]

When this function returns successfully, points to the product of <i>Multiplicand</i> times <i>Multiplier</i>.

## -returns

If this function succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

