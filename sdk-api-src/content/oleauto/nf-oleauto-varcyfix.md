---
UID: NF:oleauto.VarCyFix
title: VarCyFix function (oleauto.h)
description: Retrieves the integer portion of a variant of type currency. (VarCyFix)
helpviewer_keywords: ["VarCyFix","VarCyFix function [Automation]","_oa96_VarCyFix","automat.varcyfix","oleauto/VarCyFix"]
old-location: automat\varcyfix.htm
tech.root: automat
ms.assetid: b688530b-e911-4f48-8dab-bb1ca1c6e718
ms.date: 12/05/2018
ms.keywords: VarCyFix, VarCyFix function [Automation], _oa96_VarCyFix, automat.varcyfix, oleauto/VarCyFix
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
 - VarCyFix
 - oleauto/VarCyFix
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
 - VarCyFix
---

# VarCyFix function


## -description

Retrieves the integer portion of a variant of type currency.

## -parameters

### -param cyIn [in]

The currency variant.

### -param pcyResult [out]

The resulting variant. If the variant is negative, then the first negative integer greater than or equal to the variant is returned.

## -returns

If this function succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

