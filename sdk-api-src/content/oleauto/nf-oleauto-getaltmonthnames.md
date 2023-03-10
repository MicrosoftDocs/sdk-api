---
UID: NF:oleauto.GetAltMonthNames
title: GetAltMonthNames function (oleauto.h)
description: Retrieves the secondary (alternate) month names.
helpviewer_keywords: ["GetAltMonthNames","GetAltMonthNames function [Automation]","_oa96_GetAltMonthNames","automat.getaltmonthnames","oleauto/GetAltMonthNames"]
old-location: automat\getaltmonthnames.htm
tech.root: automat
ms.assetid: dfde73f2-edb9-4ab9-9394-d859e61a6db8
ms.date: 12/05/2018
ms.keywords: GetAltMonthNames, GetAltMonthNames function [Automation], _oa96_GetAltMonthNames, automat.getaltmonthnames, oleauto/GetAltMonthNames
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
 - GetAltMonthNames
 - oleauto/GetAltMonthNames
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
 - GetAltMonthNames
---

# GetAltMonthNames function


## -description

Retrieves the secondary (alternate) month names.

## -parameters

### -param lcid [in]

The locale identifier to be used in retrieving the alternate month names.

### -param prgp [out]

An array of pointers to strings containing the alternate month names.

## -returns

The function returns TRUE on success and FALSE otherwise.

## -remarks

Useful for Hijri, Polish and Russian alternate month names.

