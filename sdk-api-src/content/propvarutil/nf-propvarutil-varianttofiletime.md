---
UID: NF:propvarutil.VariantToFileTime
title: VariantToFileTime function (propvarutil.h)
description: Extracts a FILETIME structure from a variant structure.
helpviewer_keywords: ["PSTF_LOCAL","PSTF_UTC","VariantToFileTime","VariantToFileTime function [Windows Properties]","_shell_VariantToFileTime","properties.VariantToFileTime","propvarutil/VariantToFileTime","shell.VariantToFileTime"]
old-location: properties\VariantToFileTime.htm
tech.root: properties
ms.assetid: e3094bd1-e641-43d8-8bc5-926c8d5a6ebe
ms.date: 12/05/2018
ms.keywords: PSTF_LOCAL, PSTF_UTC, VariantToFileTime, VariantToFileTime function [Windows Properties], _shell_VariantToFileTime, properties.VariantToFileTime, propvarutil/VariantToFileTime, shell.VariantToFileTime
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
targetos: Windows
req.typenames: 
req.redist: Windows Desktop Search (WDS) 3.0
ms.custom: 19H1
f1_keywords:
 - VariantToFileTime
 - propvarutil/VariantToFileTime
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Propsys.dll
api_name:
 - VariantToFileTime
---

# VariantToFileTime function


## -description

Extracts a <a href="/windows/desktop/api/minwinbase/ns-minwinbase-filetime">FILETIME</a> structure from a variant structure.

## -parameters

### -param varIn [in]

Type: <b>REFVARIANT</b>

Reference to a source variant structure.

### -param stfOut [in]

Type: <b>PSTIME_FLAGS</b>

Specifies one of the following time flags:



#### PSTF_UTC (0)

Indicates coordinated universal time.



#### PSTF_LOCAL (1)

Indicates local time.

### -param pftOut [out]

Type: <b>FILETIME*</b>

Pointer to the extracted <a href="/windows/desktop/api/minwinbase/ns-minwinbase-filetime">FILETIME</a> structure.

## -returns

Type: <b>HRESULT</b>

If this function succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

<i>stfOut</i> flags override any property description flags.