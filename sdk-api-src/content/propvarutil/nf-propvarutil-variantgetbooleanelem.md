---
UID: NF:propvarutil.VariantGetBooleanElem
title: VariantGetBooleanElem function (propvarutil.h)
author: windows-sdk-content
description: Extracts a single Boolean element from a variant structure.
old-location: properties\VariantGetBooleanElem.htm
tech.root: properties
ms.assetid: d21ad8cc-5919-4582-a593-64bd98a82a89
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: VariantGetBooleanElem, VariantGetBooleanElem function [Windows Properties], _shell_VariantGetBooleanElem, properties.VariantGetBooleanElem, propvarutil/VariantGetBooleanElem, shell.VariantGetBooleanElem
ms.topic: function
f1_keywords: 
 - "propvarutil/VariantGetBooleanElem"
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
 - VariantGetBooleanElem
targetos: Windows
req.typenames: 
req.redist: Windows Desktop Search (WDS) 3.0
ms.custom: 19H1
---

# VariantGetBooleanElem function


## -description


Extracts a single Boolean element from a variant structure.


## -parameters




### -param var [in]

Type: <b>REFVARIANT</b>

Reference to a source variant structure.


### -param iElem [in]

Type: <b>ULONG</b>

Specifies vector or array index; otherwise, value must be 0.


### -param pfVal [out]

Type: <b>BOOL*</b>

Pointer to the extracted element value.


## -returns



Type: <b>HRESULT</b>

If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



