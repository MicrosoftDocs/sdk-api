---
UID: NF:oleauto.VarDecInt
title: VarDecInt function (oleauto.h)
description: Retrieves the integer portion of a variant of type decimal. (VarDecInt)
helpviewer_keywords: ["VarDecInt","VarDecInt function [Automation]","_oa96_VarDecInt","automat.vardecint","oleauto/VarDecInt"]
old-location: automat\vardecint.htm
tech.root: automat
ms.assetid: 65ac2bad-26f4-43b0-b90d-9a44131dbe6f
ms.date: 12/05/2018
ms.keywords: VarDecInt, VarDecInt function [Automation], _oa96_VarDecInt, automat.vardecint, oleauto/VarDecInt
req.header: oleauto.h
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
req.lib: OleAut32.lib
req.dll: OleAut32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - VarDecInt
 - oleauto/VarDecInt
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - OleAut32.dll
api_name:
 - VarDecInt
---

# VarDecInt function


## -description

Retrieves the integer portion of a variant of type decimal.

## -parameters

### -param pdecIn [in]

The decimal variant.

### -param pdecResult [out]

The resulting variant. If the variant is negative, then the first negative integer less than or equal to the variant is returned.

## -returns

If this function succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

