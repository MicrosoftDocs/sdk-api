---
UID: NF:propvarutil.VariantGetInt32Elem
title: VariantGetInt32Elem function
author: windows-sdk-content
description: Extracts a single Int32 element from a variant structure.
old-location: properties\VariantGetInt32Elem.htm
tech.root: properties
ms.assetid: de67face-9284-4e0a-8ea7-d4b6e7c037fc
ms.author: windowssdkdev
ms.date: 09/07/2018
ms.keywords: VariantGetInt32Elem, VariantGetInt32Elem function [Windows Properties], _shell_VariantGetInt32Elem, properties.VariantGetInt32Elem, propvarutil/VariantGetInt32Elem, shell.VariantGetInt32Elem
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: propvarutil.h
req.include-header: 
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
req.lib: Propsys.lib
req.dll: Propsys.dll (version 6.0 or later)
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Propsys.dll
api_name:
 - VariantGetInt32Elem
product: Windows
targetos: Windows
req.typenames: 
req.redist: Windows Desktop Search (WDS) 3.0
---

# VariantGetInt32Elem function


## -description


Extracts a single <b>Int32</b> element from a variant structure.


## -parameters




### -param var [in]

Type: <b>REFVARIANT</b>

Reference to a source variant structure.


### -param iElem [in]

Type: <b>ULONG</b>

Specifies vector or array index; otherwise, value must be 0.


### -param pnVal [out]

Type: <b>LONG*</b>

Pointer to the extracted element value.


## -returns



Type: <b>HRESULT</b>

If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



