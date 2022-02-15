---
UID: NF:intsafe.SSIZETSub
title: SSIZETSub function (intsafe.h)
description: Subtracts one SSIZE_T value from another.
helpviewer_keywords: ["SSIZETSub","SSIZETSub function [Windows Shell]","intsafe/SSIZETSub","shell.SSIZETSub"]
old-location: shell\SSIZETSub.htm
tech.root: shell
ms.assetid: 8c7ca2cb-3753-4d65-9179-5c8e1782c7ff
ms.date: 12/05/2018
ms.keywords: SSIZETSub, SSIZETSub function [Windows Shell], intsafe/SSIZETSub, shell.SSIZETSub
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
 - SSIZETSub
 - intsafe/SSIZETSub
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
 - SSIZETSub
---

# SSIZETSub function


## -description

Subtracts one SSIZE_T value from another.

## -parameters

### -param Minuend [in]

The value from which <i>Subtrahend</i> will be subtracted.

### -param Subtrahend [in]

The value to subtract from <i>Minuend</i>.

### -param pResult [out]

When this function returns successfully, points to the difference between <i>Minuend</i> and <i>Subtrahend</i>.

## -returns

If this function succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

