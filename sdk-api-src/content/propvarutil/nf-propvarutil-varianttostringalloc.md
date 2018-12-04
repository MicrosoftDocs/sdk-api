---
UID: NF:propvarutil.VariantToStringAlloc
title: VariantToStringAlloc function
author: windows-sdk-content
description: Extracts the variant value of a variant structure to a newly-allocated string. If no value can be extracted, then a default value is assigned.
old-location: properties\VariantToStringAlloc.htm
tech.root: properties
ms.assetid: 9cd4433c-d8ad-43ef-bdb9-9c1b8d8bea01
ms.author: windowssdkdev
ms.date: 11/16/2018
ms.keywords: VariantToStringAlloc, VariantToStringAlloc function [Windows Properties], _shell_VariantToStringAlloc, properties.VariantToStringAlloc, propvarutil/VariantToStringAlloc, shell.VariantToStringAlloc
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
 - VariantToStringAlloc
product: Windows
targetos: Windows
req.typenames: 
req.redist: Windows Desktop Search (WDS) 3.0
---

# VariantToStringAlloc function


## -description


Extracts the variant value of a variant structure to a newly-allocated string. If no value can be extracted, then a default value is assigned.


## -parameters




### -param varIn [in]

Type: <b>REFVARIANT</b>

Reference to a source variant structure.


### -param ppszBuf [out]

Type: <b>PWSTR</b>

Pointer to the extracted property value if one exists; otherwise, empty.


## -returns



Type: <b>HRESULT</b>

If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



