---
UID: NF:propvarutil.VariantToUInt16
title: VariantToUInt16 function
author: windows-sdk-content
description: Extracts an unsigned Int16 property value of a variant structure. If no value can be extracted, then a default value is assigned by this function.
old-location: properties\VariantToUInt16.htm
old-project: properties
ms.assetid: aa88be72-9ea5-4668-a0c5-1ca5320bda00
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: VariantToUInt16, VariantToUInt16 function [Windows Properties], _shell_VariantToUInt16, properties.VariantToUInt16, propvarutil/VariantToUInt16, shell.VariantToUInt16
ms.prod: windows
ms.technology: windows-sdk
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
 - VariantToUInt16
product: Windows
targetos: Windows
req.lib: Propsys.lib
req.dll: Propsys.dll (version 6.0 or later)
req.irql: 
req.product: ADAM
---

# VariantToUInt16 function


## -description


Extracts an unsigned <b>Int16</b> property value of a variant structure. If no value can be extracted, then a default value is assigned by this function.


## -parameters




### -param varIn [in]

Type: <b>REFVARIANT</b>

Reference to a source variant structure.


### -param puiRet [out]

Type: <b>USHORT*</b>

Pointer to the extracted property value if one exists; otherwise, 0.


## -returns



Type: <b>HRESULT</b>

If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



