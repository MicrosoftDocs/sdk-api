---
UID: NF:oleauto.SafeArrayGetDim
title: SafeArrayGetDim function (oleauto.h)
description: Gets the number of dimensions in the array.
helpviewer_keywords: ["SafeArrayGetDim","SafeArrayGetDim function [Automation]","_oa96_SafeArrayGetDim","automat.safearraygetdim","oleauto/SafeArrayGetDim"]
old-location: automat\safearraygetdim.htm
tech.root: automat
ms.assetid: bc52b23b-d323-478c-881f-d2a31a3289c5
ms.date: 12/05/2018
ms.keywords: SafeArrayGetDim, SafeArrayGetDim function [Automation], _oa96_SafeArrayGetDim, automat.safearraygetdim, oleauto/SafeArrayGetDim
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
 - SafeArrayGetDim
 - oleauto/SafeArrayGetDim
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
 - SafeArrayGetDim
---

# SafeArrayGetDim function


## -description

Gets the number of dimensions in the array.

## -parameters

### -param psa [in]

An array descriptor created by <a href="/previous-versions/windows/desktop/api/oleauto/nf-oleauto-safearraycreate">SafeArrayCreate</a>.

## -returns

The number of dimensions in the array.