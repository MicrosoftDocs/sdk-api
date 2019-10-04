---
UID: NF:propvarutil.VariantToInt32
title: VariantToInt32 function (propvarutil.h)
author: windows-sdk-content
description: Extracts an Int32 property value of a variant structure. If no value can be extracted, then a default value is assigned.
old-location: properties\VariantToInt32.htm
tech.root: properties
ms.assetid: 6d2a4b8f-2ec5-4ffd-80b0-6615fdfb2379
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: VariantToInt32, VariantToInt32 function [Windows Properties], _shell_VariantToInt32, properties.VariantToInt32, propvarutil/VariantToInt32, shell.VariantToInt32
ms.topic: function
f1_keywords: 
 - "propvarutil/VariantToInt32"
dev_langs:
 - c++
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
 - VariantToInt32
targetos: Windows
req.typenames: 
req.redist: Windows Desktop Search (WDS) 3.0
ms.custom: 19H1
---

# VariantToInt32 function


## -description


Extracts an <b>Int32</b> property value of a variant structure. If no value can be extracted, then a default value is assigned.


## -parameters




### -param varIn [in]

Type: <b>REFVARIANT</b>

Reference to a source variant structure.


### -param plRet [out]

Type: <b>LONG*</b>

Pointer to the extracted property value if one exists; otherwise, 0.


## -returns



Type: <b>HRESULT</b>

If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



