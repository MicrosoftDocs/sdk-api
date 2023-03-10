---
UID: NF:intsafe.ShortToDWordPtr
title: ShortToDWordPtr function (intsafe.h)
description: Converts a value of type SHORT to a value of type DWORD_PTR.
helpviewer_keywords: ["ShortToDWordPtr","ShortToDWordPtr function [Windows Shell]","intsafe/ShortToDWordPtr","shell.ShortToDWordPtr"]
old-location: shell\ShortToDWordPtr.htm
tech.root: shell
ms.assetid: e5d0bb74-adde-48c7-b2df-1ba86d528db1
ms.date: 12/05/2018
ms.keywords: ShortToDWordPtr, ShortToDWordPtr function [Windows Shell], intsafe/ShortToDWordPtr, shell.ShortToDWordPtr
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
 - ShortToDWordPtr
 - intsafe/ShortToDWordPtr
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
 - ShortToDWordPtr
---

# ShortToDWordPtr function


## -description

Converts a value of type <b>SHORT</b> to a value of type <b>DWORD_PTR</b>.

## -parameters

### -param sOperand [in]

The value to convert.

### -param pdwResult [out]

The converted value.

## -returns

If this function succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

