---
UID: NF:propvarutil.VariantGetDoubleElem
title: VariantGetDoubleElem function
author: windows-sdk-content
description: Extracts one double element from a variant structure.
old-location: properties\VariantGetDoubleElem.htm
tech.root: properties
ms.assetid: cc6cb3a0-ba39-4088-8d72-082f6a4e39d3
ms.author: windowssdkdev
ms.date: 10/19/2018
ms.keywords: VariantGetDoubleElem, VariantGetDoubleElem function [Windows Properties], _shell_VariantGetDoubleElem, properties.VariantGetDoubleElem, propvarutil/VariantGetDoubleElem, shell.VariantGetDoubleElem
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
 - VariantGetDoubleElem
product: Windows
targetos: Windows
req.typenames: 
req.redist: Windows Desktop Search (WDS) 3.0
---

# VariantGetDoubleElem function


## -description


Extracts one <b>double</b> element from a variant structure.


## -parameters




### -param var [in]

Type: <b>REFVARIANT</b>

Reference to a source variant structure.


### -param iElem [in]

Type: <b>ULONG</b>

Specifies vector or array index; otherwise, value must be 0.


### -param pnVal [out]

Type: <b>DOUBLE*</b>

Pointer to the extracted element value.


## -returns



Type: <b>HRESULT</b>

If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



