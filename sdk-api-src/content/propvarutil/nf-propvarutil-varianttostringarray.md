---
UID: NF:propvarutil.VariantToStringArray
title: VariantToStringArray function
author: windows-sdk-content
description: Extracts data from a vector structure into a String array.
old-location: properties\VariantToStringArray.htm
old-project: properties
ms.assetid: d19b12ad-408c-4502-ad59-49386784bd69
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: VariantToStringArray, VariantToStringArray function [Windows Properties], _shell_VariantToStringArray, properties.VariantToStringArray, propvarutil/VariantToStringArray, shell.VariantToStringArray
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: propvarutil.h
req.include-header: 
req.redist: Windows Desktop Search (WDS) 3.0
req.target-type: Windows
req.target-min-winverclnt: Windows XP with SP2, Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2003 with SP1 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: PROPVAR_COMPARE_UNIT
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Propsys.dll
api_name:
 - VariantToStringArray
product: Windows
targetos: Windows
req.lib: Propsys.lib
req.dll: Propsys.dll (version 6.0 or later)
req.irql: 
req.product: ADAM
---

# VariantToStringArray function


## -description


Extracts data from a vector structure into a String array.


## -parameters




### -param var [in]

Type: <b>REFVARIANT</b>

Reference to a source variant structure.


### -param prgsz [out]

Type: <b>PWSTR*</b>

Pointer to the string data extracted from source variant structure.


### -param crgsz [in]

Type: <b>ULONG</b>

Specifies string array size.


### -param pcElem [out]

Type: <b>ULONG*</b>

Pointer to the count of string elements extracted from source variant structure.


## -returns



Type: <b>HRESULT</b>

If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



