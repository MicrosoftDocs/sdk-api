---
UID: NF:oleauto.VarCyMul
title: VarCyMul function (oleauto.h)
author: windows-sdk-content
description: Multiplies two variants of type currency.
old-location: automat\varcymul.htm
tech.root: automat
ms.assetid: a7cc06b2-5a19-4ffe-b055-4756a0d305ef
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: VarCyMul, VarCyMul function [Automation], _oa96_VarCyMul, automat.varcymul, oleauto/VarCyMul
ms.topic: function
f1_keywords: 
 - "oleauto/VarCyMul"
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - OleAut32.dll
api_name:
 - VarCyMul
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# VarCyMul function


## -description


Multiplies two variants of type currency.


## -parameters




### -param cyLeft [in]

The first variant


### -param cyRight [in]

The second variant.


### -param pcyResult [out]

The resulting variant.


## -returns



If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



If any of the fields of <i>cyLeft</i> or <i>cyRight</i> is left uninitialized, it may default to a large value causing DISP_E_OVERFLOW.



